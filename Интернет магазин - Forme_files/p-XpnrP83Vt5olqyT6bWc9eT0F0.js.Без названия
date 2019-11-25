;window.CloudflareApps=window.CloudflareApps||{};CloudflareApps.siteId="0cccca5455fe2f2514c100284882387b";CloudflareApps.installs=CloudflareApps.installs||{};;(function(){'use strict'
CloudflareApps.internal=CloudflareApps.internal||{}
var errors=[]
CloudflareApps.internal.placementErrors=errors
var errorHashes={}
function noteError(options){var hash=options.selector+'::'+options.type+'::'+(options.installId||'')
if(errorHashes[hash]){return}
errorHashes[hash]=true
errors.push(options)}
var initializedSelectors={}
var currentInit=false
CloudflareApps.internal.markSelectors=function markSelectors(){if(!currentInit){check()
currentInit=true
setTimeout(function(){currentInit=false})}}
function check(){var installs=window.CloudflareApps.installs
for(var installId in installs){if(!installs.hasOwnProperty(installId)){continue}
var selectors=installs[installId].selectors
if(!selectors){continue}
for(var key in selectors){if(!selectors.hasOwnProperty(key)){continue}
var hash=installId+'::'+key
if(initializedSelectors[hash]){continue}
var els=document.querySelectorAll(selectors[key])
if(els&&els.length>1){noteError({type:'init:too-many',option:key,selector:selectors[key],installId:installId})
initializedSelectors[hash]=true
continue}else if(!els||!els.length){continue}
initializedSelectors[hash]=true
els[0].setAttribute('cfapps-selector',selectors[key])}}}
CloudflareApps.querySelector=function querySelector(selector){if(selector==='body'||selector==='head'){return document[selector]}
CloudflareApps.internal.markSelectors()
var els=document.querySelectorAll('[cfapps-selector="'+selector+'"]')
if(!els||!els.length){noteError({type:'select:not-found:by-attribute',selector:selector})
els=document.querySelectorAll(selector)
if(!els||!els.length){noteError({type:'select:not-found:by-query',selector:selector})
return null}else if(els.length>1){noteError({type:'select:too-many:by-query',selector:selector})}
return els[0]}
if(els.length>1){noteError({type:'select:too-many:by-attribute',selector:selector})}
return els[0]}}());(function(){'use strict'
var prevEls={}
CloudflareApps.createElement=function createElement(options,prevEl){options=options||{}
CloudflareApps.internal.markSelectors()
try{if(prevEl&&prevEl.parentNode){var replacedEl
if(prevEl.cfAppsElementId){replacedEl=prevEls[prevEl.cfAppsElementId]}
if(replacedEl){prevEl.parentNode.replaceChild(replacedEl,prevEl)
delete prevEls[prevEl.cfAppsElementId]}else{prevEl.parentNode.removeChild(prevEl)}}
var element=document.createElement('cloudflare-app')
var container
if(options.pages&&options.pages.URLPatterns&&!CloudflareApps.matchPage(options.pages.URLPatterns)){return element}
try{container=CloudflareApps.querySelector(options.selector)}catch(e){}
if(!container){return element}
if(!container.parentNode&&(options.method==='after'||options.method==='before'||options.method==='replace')){return element}
if(container===document.body){if(options.method==='after'){options.method='append'}else if(options.method==='before'){options.method='prepend'}}
switch(options.method){case'prepend':if(container.firstChild){container.insertBefore(element,container.firstChild)
break}
case'append':container.appendChild(element)
break
case'after':if(container.nextSibling){container.parentNode.insertBefore(element,container.nextSibling)}else{container.parentNode.appendChild(element)}
break
case'before':container.parentNode.insertBefore(element,container)
break
case'replace':try{var id=element.cfAppsElementId=Math.random().toString(36)
prevEls[id]=container}catch(e){}
container.parentNode.replaceChild(element,container)}
return element}catch(e){if(typeof console!=='undefined'&&typeof console.error!=='undefined'){console.error('Error creating Cloudflare Apps element',e)}}}}());(function(){'use strict'
CloudflareApps.matchPage=function matchPage(patterns){if(!patterns||!patterns.length){return true}
var loc=document.location.host+document.location.pathname
if(window.CloudflareApps&&CloudflareApps.proxy&&CloudflareApps.proxy.originalURL){var url=CloudflareApps.proxy.originalURL.parsed
loc=url.host+url.path}
for(var i=0;i<patterns.length;i++){var re=new RegExp(patterns[i],'i')
if(re.test(loc)){return true}}
return false}}());CloudflareApps.installs["DlIUlr5y3yHd"]={appId:"0n-Tbk3FbOG8",scope:{}};;CloudflareApps.installs["DlIUlr5y3yHd"].options={};;CloudflareApps.installs["MTuu29eQc6fW"]={appId:"b9dwZce78j9q",scope:{}};;CloudflareApps.installs["MTuu29eQc6fW"].options={"account":{"accountId":"j7olWQezrlpX","service":"chatra","userId":"9PjCnt2BPMaJkv94i"},"advanced":{"devices":"all","enabled":true,"groupId":"","language":"ru","zIndex":1000000},"button":{"bgColor":"#008080","position":"br","size":57,"style":"tab","textColor":"#ffffff","useChatraSettings":false},"window":{"agentBubbleBg":"#c0c0c0","clientBubbleBg":"#d4f2fc","height":415,"width":317}};;CloudflareApps.installs["Yy2CodLVQtb0"]={appId:"cYeUeoS56VXt",scope:{}};;CloudflareApps.installs["Yy2CodLVQtb0"].options={"account":{"accountId":"PUryrBg1GCtv","service":"privy","userId":"C703B5ADFF3A4D5B13FE374F"}};;CloudflareApps.installs["Yy2CodLVQtb0"].product={"id":"privy-free"};;if(CloudflareApps.matchPage(CloudflareApps.installs['MTuu29eQc6fW'].URLPatterns)){(function(){var demoChatraId="MTuu29eQc6fW"=='preview'?'hX8ihkAcyHK93ue99':void 0;var demoGroupId="MTuu29eQc6fW"=='preview'?'BKjdxwGNFhDE4DJ2r':void 0;var currentChatraId;function convertOptions(options,isDemo){var useChatraButtonSettings=options.button.useChatraSettings&&!isDemo;if(!options.button)options.button={};if(!options.window)options.window={};if(!options.advanced)options.advanced={};var result={chatWidth:parseInt(options.window.width)||void 0,chatHeight:parseInt(options.window.height)||void 0,zIndex:options.advanced.zIndex!==null?options.advanced.zIndex:void 0,mobileOnly:options.advanced.devices=='mob',disabledOnMobile:options.advanced.devices=='notMob',language:options.advanced.language||(isDemo?'en':void 0)};if(isDemo||options.advanced.groupId){result.groupId=isDemo?demoGroupId:options.advanced.groupId;}
if(!useChatraButtonSettings){result.buttonStyle=options.button.style||void 0;result.buttonSize=parseInt(options.button.size)||void 0;result.buttonPosition=options.button.position||void 0;}
result.colors={};if(!useChatraButtonSettings&&options.button.textColor)result.colors.buttonText=options.button.textColor;if(!useChatraButtonSettings&&options.button.bgColor)result.colors.buttonBg=options.button.bgColor;if(options.window.bgColor)result.colors.chatBg=options.window.bgColor;if(options.window.clientBubbleBg)result.colors.clientBubbleBg=options.window.clientBubbleBg;if(options.window.agentBubbleBg)result.colors.agentBubbleBg=options.window.agentBubbleBg;return result;}
function initialize(options){var chatraId=(options.account||{}).userId;window.ChatraSetup=convertOptions(options,!chatraId);currentChatraId=chatraId;window.ChatraID=chatraId||demoChatraId;window.ChatraProtocol='https:';var s=document.createElement('script');window.Chatra=window.Chatra||function(){(window.Chatra.q=window.Chatra.q||[]).push(arguments);};s.async=true;s.src='https://call.chatra.io/chatra.js';if(document.head)document.head.appendChild(s);}
window.CloudflareApps.installs['MTuu29eQc6fW'].scope.setOptions=function(options){var newChatraId=(options.account||{}).userId;var newChatraSetup=convertOptions(options,!newChatraId);if(newChatraId!=currentChatraId){currentChatraId=newChatraId;window.ChatraID=newChatraId||demoChatraId;window.ChatraSetup=newChatraSetup;Chatra('restart');}
else if(window.ChatraSetup.buttonStyle!=newChatraSetup.buttonStyle){window.ChatraSetup=newChatraSetup;Chatra('restart');Chatra('minimizeWidget');}
else if(window.ChatraSetup.mobileOnly!=newChatraSetup.mobileOnly||window.ChatraSetup.disabledOnMobile!=newChatraSetup.disabledOnMobile||window.ChatraSetup.language!=newChatraSetup.language){var isExpanded=Chatra._chatExpanded;window.ChatraSetup=newChatraSetup;Chatra('restart');if(isExpanded)Chatra('expandWidget');}
else{var chatButtonChanged=false;var chatWindowChanged=false;if(window.ChatraSetup.buttonSize!=newChatraSetup.buttonSize){Chatra('setButtonSize',newChatraSetup.buttonSize);chatButtonChanged=true;}
if(window.ChatraSetup.buttonPosition!=newChatraSetup.buttonPosition){Chatra('setButtonPosition',newChatraSetup.buttonPosition);chatButtonChanged=true;}
if(window.ChatraSetup.chatWidth!=newChatraSetup.chatWidth){Chatra('setChatWidth',newChatraSetup.chatWidth);chatWindowChanged=true;}
if(window.ChatraSetup.chatHeight!=newChatraSetup.chatHeight){Chatra('setChatHeight',newChatraSetup.chatHeight);chatWindowChanged=true;}
if(window.ChatraSetup.zIndex!=newChatraSetup.zIndex)
Chatra('setZIndex',newChatraSetup.zIndex);if(window.ChatraSetup.groupId!=newChatraSetup.groupId)
Chatra('setGroupId',newChatraSetup.groupId?newChatraSetup.groupId:null);if(window.ChatraSetup.colors.buttonText!=newChatraSetup.colors.buttonText||window.ChatraSetup.colors.buttonBg!=newChatraSetup.colors.buttonBg){Chatra('setColors',newChatraSetup.colors);chatButtonChanged=true;}
else if(window.ChatraSetup.colors.chatBg!=newChatraSetup.colors.chatBg||window.ChatraSetup.colors.clientBubbleBg!=newChatraSetup.colors.clientBubbleBg||window.ChatraSetup.colors.agentBubbleBg!=newChatraSetup.colors.agentBubbleBg){Chatra('setColors',newChatraSetup.colors);chatWindowChanged=true;}
if(chatButtonChanged&&!chatWindowChanged&&Chatra._chatExpanded)Chatra('minimizeWidget');else if(chatWindowChanged&&!chatButtonChanged&&!Chatra._chatExpanded)Chatra('expandWidget');window.ChatraSetup=newChatraSetup;}};initialize(CloudflareApps.installs['MTuu29eQc6fW'].options);})();};if(CloudflareApps.matchPage(CloudflareApps.installs['Yy2CodLVQtb0'].URLPatterns)){(function(){"use strict";var options=CloudflareApps.installs['Yy2CodLVQtb0'].options;if(!options.account){options.account={userId:"D04C76659DA92C684276FAD6"};}
window._d_site=options.account.userId;window.Privy=window.Privy||function(){(window.Privy.q=window.Privy.q||[]).push(arguments)};var script=document.createElement('script');script.async=1;script.src='https://widget.privy.com/assets/widget.js';var elem=document.getElementsByTagName('script')[0];elem.parentNode.insertBefore(script,elem);})();}(function(){var script = document.createElement('script');script.src = '/cdn-cgi/apps/body/MwuBMq60Yy6lcbLgLl3Zjz3-u5I.js';document.head.appendChild(script);})();