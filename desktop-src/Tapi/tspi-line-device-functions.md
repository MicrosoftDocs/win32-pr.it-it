---
description: Questa sezione contiene un elenco alfabetico delle funzioni del dispositivo line disponibili nella telefonia SPI.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Funzioni della periferica di linea TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882330"
---
# <a name="tspi-line-device-functions"></a>Funzioni della periferica di linea TSPI

Questa sezione contiene un elenco alfabetico delle funzioni del dispositivo line disponibili nella telefonia SPI. Le informazioni per ogni funzione includono quanto segue:

-   Istruzione dello scopo della funzione.
-   Sintassi corretta per la funzione.
-   Descrizione dei parametri della funzione, inclusi gli Stati di chiamata validi.
-   Descrizione del valore restituito della funzione.
-   Una sezione note che può includere uno o tutti gli elementi seguenti: un elenco degli Stati di chiamata validi all'immissione della funzione e le transizioni tipiche dello stato di chiamata al completamento della richiesta. Descrizione dei membri delle strutture di dati di grandi dimensioni che devono essere compilati dal provider di servizi e di quali membri devono essere conservati intatti. e confronto con una funzione corrispondente all'interno di TAPI.
-   Riferimenti ad altre funzioni, messaggi o strutture di dati.
    > [!Note]  
    > Gli Stati effettivi in cui è possibile eseguire una funzione possono essere limitati dalle funzionalità del provider di servizi. I provider di servizi devono impostare il membro **dwCallFeatures** nella struttura [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) , il membro **dwAddressFeatures** nella struttura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) e il membro **dwLineFeatures** nella struttura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) per indicare alle applicazioni se una funzione è consentita o meno in quel momento.

     

Questa sezione contiene le funzioni del dispositivo line TSPI seguenti:

-   [**\_LINEACCEPT TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**\_LINEADDTOCONFERENCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**\_LINEANSWER TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**\_LINEBLINDTRANSFER TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**\_LINECLOSE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**\_LINECLOSECALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**\_LINECLOSEMSPINSTANCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**\_LINECOMPLETECALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**\_LINECOMPLETETRANSFER TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**\_LINECONDITIONALMEDIADETECTION TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**\_LINECONFIGDIALOG TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**\_LINECONFIGDIALOGEDIT TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**\_LINECREATEMSPINSTANCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**\_LINEDEVSPECIFIC TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**\_LINEDEVSPECIFICFEATURE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**\_LINEDIAL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**\_LINEDROP TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [\_LINEDROPNOOWNER TSPI](tspi-linedropnoowner.md)
-   [\_LINEDROPONCLOSE TSPI](tspi-linedroponclose.md)
-   [**\_LINEFORWARD TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**\_LINEGATHERDIGITS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**\_LINEGENERATEDIGITS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**\_LINEGENERATETONE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**\_LINEGETADDRESSCAPS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**\_LINEGETADDRESSID TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**\_LINEGETADDRESSSTATUS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**\_LINEGETCALLADDRESSID TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**\_LINEGETCALLHUBTRACKING TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**\_LINEGETCALLIDS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**\_LINEGETCALLINFO TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**\_LINEGETCALLSTATUS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**\_LINEGETDEVCAPS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**\_LINEGETDEVCONFIG TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**\_LINEGETEXTENSIONID TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**\_LINEGETICON TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**\_LINEGETID TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**\_LINEGETLINEDEVSTATUS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**\_LINEGETNUMADDRESSIDS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**\_LINEHOLD TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**\_LINEMAKECALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**\_LINEMONITORDIGITS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**\_LINEMONITORMEDIA TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**\_LINEMONITORTONES TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**\_LINEMSPIDENTIFY TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**\_LINENEGOTIATEEXTVERSION TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**\_LINENEGOTIATETSPIVERSION TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**\_LINEOPEN TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**\_LINEPARK TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**\_LINEPICKUP TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**\_LINEPREPAREADDTOCONFERENCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**\_LINERECEIVEMSPDATA TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**\_LINEREDIRECT TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**\_LINERELEASEUSERUSERINFO TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**\_LINEREMOVEFROMCONFERENCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**\_LINESECURECALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**\_LINESELECTEXTVERSION TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**\_LINESENDUSERUSERINFO TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**\_LINESETAPPSPECIFIC TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**\_LINESETCALLDATA TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**\_LINESETCALLHUBTRACKING TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**\_LINESETCALLPARAMS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**\_LINESETCALLQUALITYOFSERVICE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**\_LINESETCALLTREATMENT TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [\_LINESETCURRENTLOCATION TSPI](tspi-linesetcurrentlocation.md)
-   [**\_LINESETDEFAULTMEDIADETECTION TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**\_LINESETDEVCONFIG TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**\_LINESETLINEDEVSTATUS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**\_LINESETMEDIACONTROL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**\_LINESETMEDIAMODE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**\_LINESETSTATUSMESSAGES TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**\_LINESETTERMINAL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**\_LINESETUPCONFERENCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**\_LINESETUPTRANSFER TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**\_LINESWAPHOLD TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**\_LINEUNCOMPLETECALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**\_LINEUNHOLD TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**\_LINEUNPARK TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
