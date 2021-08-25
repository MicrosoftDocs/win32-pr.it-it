---
description: Le funzioni seguenti vengono fornite solo in una versione generica senza &\# 0034; Un&\# 0034; o &\# 0034; W&\# suffisso 0034;.
ms.assetid: 0e51b7a6-53a0-4e92-9bed-f8e4f8ffd5a1
title: Funzioni senza versioni Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a5b2444aa32a6ad5b7825c17b31ea66eaacf91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472897"
---
# <a name="functions-without-unicode-versions"></a>Funzioni senza versioni Unicode

Le funzioni seguenti vengono fornite solo in una versione generica senza suffisso "A" o "W".




| Funzione TAPI | Commenti | 
|---------------|----------|
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineaccept"><strong>lineAccept</strong></a> | Si presuppone che la memoria a cui <em>punta lpsUserUserInfo</em> contenga dati binari per il trasferimento end-to-end. L'applicazione deve fornire i dati in un formato pronto per la trasmissione. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference"><strong>lineAddToConference</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineagentspecific"><strong>lineAgentSpecific</strong></a> | La memoria a cui punta <em>lpParams</em> è privata tra l'applicazione e il gestore dell'agente. L'applicazione deve fornire dati nel formato specificato nella definizione dell'estensione del gestore agenti. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineanswer"><strong>lineAnswer</strong></a> | Si presuppone che la memoria a cui <em>punta lpsUserUserInfo</em> contenga dati binari per il trasferimento end-to-end. L'applicazione deve fornire i dati in un formato pronto per la trasmissione. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineclose"><strong>lineClose</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linecompletecall"><strong>lineCompleteCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer"><strong>lineCompleteTransfer</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider"><strong>lineConfigProvider</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall"><strong>lineDeallocateCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedevspecific"><strong>lineDevSpecific</strong></a> | La memoria a cui punta <em>lpParams</em> è privata tra l'applicazione e il provider di servizi. L'applicazione deve fornire dati nel formato specificato nella definizione dell'estensione del provider di servizi. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature"><strong>lineDevSpecificFeature</strong></a> | La memoria a cui punta <em>lpParams</em> è privata tra l'applicazione e il provider di servizi. L'applicazione deve fornire dati nel formato specificato nella definizione dell'estensione del provider di servizi. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linedrop"><strong>lineDrop</strong></a> | Si presuppone che la memoria a cui <em>punta lpsUserUserInfo</em> contenga dati binari per il trasferimento end-to-end. L'applicazione deve fornire i dati in un formato pronto per la trasmissione. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegeneratetone"><strong>lineGenerateTone</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus"><strong>lineGetCallStatus</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls"><strong>lineGetConfRelatedCalls</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls"><strong>lineGetNewCalls</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetmessage"><strong>lineGetMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetnumrings"><strong>lineGetNumRings</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages"><strong>lineGetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linehold"><strong>lineHold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitordigits"><strong>lineMonitorDigits</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitormedia"><strong>lineMonitorMedia</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linemonitortones"><strong>lineMonitorTones</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion"><strong>lineNegotiateAPIVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion"><strong>lineNegotiateExtVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineproxymessage"><strong>lineProxyMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse"><strong>lineProxyResponse</strong></a> | I campi nella <a href="/windows/win32/api/tapi/ns-tapi-lineproxyrequest"><strong>struttura LINEPROXYREQUEST</strong></a> sono sempre Unicode. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient"><strong>lineRegisterRequestRecipient</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo"><strong>lineReleaseUserUserInfo</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference"><strong>lineRemoveFromConference</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider"><strong>lineRemoveProvider</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesecurecall"><strong>lineSecureCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo"><strong>lineSendUserUserInfo</strong></a> | Si presuppone che la memoria a cui <em>punta lpsUserUserInfo</em> contenga dati binari per il trasferimento end-to-end. L'applicazione deve fornire i dati in un formato pronto per la trasmissione. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity"><strong>lineSetAgentActivity</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup"><strong>lineSetAgentGroup</strong></a> | <blockquote>[!Note]<br />I nomi dei gruppi vengono ignorati.</blockquote><br /> | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetagentstate"><strong>lineSetAgentState</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetappspecific"><strong>lineSetAppSpecific</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcalldata"><strong>lineSetCallData</strong></a> | La memoria a cui <em>punta lpCallData</em> è in un formato specificato dall'applicazione o da un gruppo di applicazioni che cooperano. Il formato dei dati non è in ambito TAPI e non viene convertito da TAPI. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallparams"><strong>lineSetCallParams</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege"><strong>lineSetCallPrivilege</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice"><strong>lineSetCallQualityOfService</strong></a> | Il formato dei dati nella parte specifica del provider della struttura QOS non è in ambito TAPI e non viene convertito da TAPI. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment"><strong>lineSetCallTreatment</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetcurrentlocation"><strong>lineSetCurrentLocation</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus"><strong>lineSetLineDevStatus</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol"><strong>lineSetMediaControl</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetmediamode"><strong>lineSetMediaMode</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetnumrings"><strong>lineSetNumRings</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages"><strong>lineSetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-linesetterminal"><strong>lineSetTerminal</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineshutdown"><strong>lineShutdown</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineswaphold"><strong>lineSwapHold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall"><strong>lineUncompleteCall</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-lineunhold"><strong>lineUnhold</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneclose"><strong>phoneClose</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonedevspecific"><strong>phoneDevSpecific</strong></a> | La memoria a cui punta <em>lpParams</em> è privata tra l'applicazione e il provider di servizi. L'applicazione deve fornire dati nel formato specificato nella definizione dell'estensione del provider di servizi. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetdata"><strong>phoneGetData</strong></a> | La memoria a cui punta <em>lpData</em> è privata tra l'applicazione e il provider di servizi. L'applicazione deve elaborare i dati nel formato specificato nella definizione del provider di servizi. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay"><strong>phoneGetDisplay</strong></a> | La memoria a cui punta <em>lpDisplay</em> è privata tra l'applicazione e il provider di servizi. L'applicazione deve elaborare i dati nel formato specificato nella definizione del provider di servizi. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetgain"><strong>phoneGetGain</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch"><strong>phoneGetHookSwitch</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetlamp"><strong>phoneGetLamp</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetmessage"><strong>phoneGetMessage</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetring"><strong>phoneGetRing</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages"><strong>phoneGetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonegetvolume"><strong>phoneGetVolume</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion"><strong>phoneNegotiateAPIVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion"><strong>phoneNegotiateExtVersion</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneopen"><strong>phoneOpen</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetdata"><strong>phoneSetData</strong></a> | La memoria a cui punta <em>lpParams</em> è privata tra l'applicazione e il provider di servizi. L'applicazione deve fornire dati nel formato specificato nella definizione del provider di servizi. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay"><strong>phoneSetDisplay</strong></a> | La memoria a cui punta <em>lpDisplay</em> è privata tra l'applicazione e il provider di servizi. L'applicazione deve fornire dati nel formato specificato nella definizione del provider di servizi. | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetgain"><strong>phoneSetGain</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch"><strong>phoneSetHookSwitch</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetlamp"><strong>phoneSetLamp</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetring"><strong>phoneSetRing</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages"><strong>phoneSetStatusMessages</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phonesetvolume"><strong>phoneSetVolume</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-phoneshutdown"><strong>phoneShutdown</strong></a> |  | 
| <a href="/windows/desktop/api/Tapi/nf-tapi-tapirequestdrop"><strong>tapiRequestDrop</strong></a> | Questa funzione è obsoleta e non è disponibile per le applicazioni. | 
| <a href="tapirequestmediacall.md"><strong>tapiRequestMediaCall</strong></a> | Questa funzione è obsoleta e non è disponibile per le applicazioni. | 




 

 

 




