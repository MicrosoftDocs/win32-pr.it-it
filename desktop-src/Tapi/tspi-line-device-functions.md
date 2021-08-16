---
description: Questa sezione contiene un elenco alfabetico delle funzioni dei dispositivi di linea disponibili nella spi di telefonia.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Funzioni della periferica di linea TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52282154e99ca4e400f6b2d5f32d00a19d62cfe98f0b789d4ee24b9a240293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403711"
---
# <a name="tspi-line-device-functions"></a>Funzioni della periferica di linea TSPI

Questa sezione contiene un elenco alfabetico delle funzioni dei dispositivi di linea disponibili nella spi di telefonia. Le informazioni per ogni funzione includono quanto segue:

-   Istruzione dello scopo della funzione.
-   Sintassi corretta per la funzione.
-   Descrizione dei parametri della funzione, inclusi gli stati di chiamata validi.
-   Descrizione del valore restituito della funzione.
-   Sezione Osservazioni che può includere uno o tutti gli stati di chiamata seguenti: un elenco degli stati di chiamata validi all'immissione della funzione e transizioni di stato di chiamata tipiche al termine della richiesta. una descrizione dei membri delle strutture di dati di grandi dimensioni che devono essere compilati dal provider di servizi e dei membri che devono mantenere intatti i relativi valori; e confronto con una funzione corrispondente all'interno di TAPI.
-   Riferimenti ad altre funzioni, messaggi o strutture di dati.
    > [!Note]  
    > Gli stati effettivi in cui è possibile eseguire una funzione possono essere limitati dalle funzionalità del provider di servizi. I provider di servizi devono impostare il membro **dwCallFeatures** nella struttura [**LINECALLSTATUS,**](/windows/win32/api/tapi/ns-tapi-linecallstatus) il membro **dwAddressFeatures** nella struttura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) e il membro **dwLineFeatures** nella struttura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) per indicare alle applicazioni se in quel momento è consentita o meno una funzione.

     

Questa sezione contiene le funzioni del dispositivo linea TSPI seguenti:

-   [**Riga \_ TSPIAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**Riga \_ TSPIAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**Riga \_ TSPIAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**Riga \_ TSPIBlindTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**Riga \_ TSPIChiudi**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**Riga \_ TSPICloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**Riga \_ TSPICloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**Riga \_ TSPICompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**Riga \_ TSPICompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**Riga \_ TSPIConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**LineConfigDialog TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**Riga \_ TSPICreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**\_LineDial TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**LineDrop TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [Riga \_ TSPIDropNoOwner](tspi-linedropnoowner.md)
-   [Riga \_ TSPIDropOnClose](tspi-linedroponclose.md)
-   [**Riga \_ TSPIForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**Riga \_ TSPIGatherDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**Riga \_ TSPIGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**Riga \_ TSPIGenerateTone**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**Riga \_ TSPIGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**Riga \_ TSPIGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**Riga \_ TSPIGetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**TSPI \_ lineGetCallIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**Riga \_ TSPIGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**Riga \_ TSPIGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**Riga \_ TSPIGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**Riga \_ TSPIGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**TSPI \_ lineGetExtensionID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**Riga \_ TSPIGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**Riga \_ TSPIGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**LineHold TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**Riga \_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ lineMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**Riga \_ TSPIMonitorMedia**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**TSPI \_ lineMonitorTones**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**Riga \_ TSPIMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**Riga \_ TSPINegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**Riga \_ TSPINegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**Riga \_ TSPIApri**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**LinePark \_ TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**Riga \_ TSPIPrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**\_LineRedirect TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**TSPI \_ lineReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**Riga \_ TSPIRemoveFromConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**TSPI \_ lineSecureCall**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**Riga \_ TSPISelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**Riga \_ TSPISendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**TSPI \_ lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI \_ lineSetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**\_LineSetCallParams TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**TSPI \_ lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI \_ lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [Riga \_ TSPISetCurrentLocation](tspi-linesetcurrentlocation.md)
-   [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**TSPI \_ lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI \_ lineSetMediaControl**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**LineSetMediaMode TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**Riga \_ TSPISetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**Riga \_ TSPISetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**Riga \_ TSPISwapHold**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**Riga \_ TSPIUncompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**Riga \_ TSPIUnhold**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
