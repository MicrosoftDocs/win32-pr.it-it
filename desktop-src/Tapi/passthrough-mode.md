---
description: Quando una chiamata è attiva in LINEBEARERMODE \_ PassThrough, il provider di servizi fornisce accesso diretto all'hardware collegato per il controllo da parte dell'applicazione.
ms.assetid: 75e31241-c782-4d50-9590-cf68c0505add
title: Modalità passthrough
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985e1caf666fcb3278bacf5c5cfe9d8a4e847dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308600"
---
# <a name="passthrough-mode"></a>Modalità passthrough

Quando una chiamata è attiva in **LINEBEARERMODE \_ PassThrough**, il provider di servizi fornisce accesso diretto all'hardware collegato per il controllo da parte dell'applicazione. Le applicazioni possono utilizzare questa modalità per un controllo diretto temporaneo sui modem asincroni, a cui si accede tramite le [funzioni di comunicazione](/windows/desktop/DevIO/communications-functions), allo scopo di configurare o utilizzare funzionalità speciali non altrimenti supportate dal provider di servizi, ad esempio facsimile (classe 1, 2 e così via). Questa modalità di connessione è supportata dal provider di servizi Universal Modem driver (Unimodem).

I provider di servizi che supportano **LINEBEARERMODE \_ PassThrough** lo indicano nel membro **dwBearerModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) . Quando è indicato il **\_ pass-through LINEBEARERMODE** , il provider di servizi Unimodem includerà anche nell'area **devSpecific** della struttura **LINEDEVCAPS** la chiave del registro di sistema usata per accedere ai dati sul modem associato al dispositivo a linee, nel formato seguente:

``` syntax
struct {
    DWORD dwContents;   // Set to 1 (indicates containing key).
    DWORD dwKeyOffset;  // Offset to key from start of this
                        // structure (not from start of
                        // LINEDEVCAPS structure).
                        // 8 in this case. 
    BYTE rgby[...];     // Place that contains null-terminated
                        // registry key. 
}
```

Ad esempio:

``` syntax
    00000001 00000008 74737953 435c6d65  ........System\C
    65727275 6f43746e 6f72746e 7465536c  urrentControlSet
    7265535c 65636976 6c435c73 5c737361  urrentControlSet
    65646f4d 30305c6d xx003030 xxxxxxxx  Modem\0000.
```

Questa chiave del registro di sistema può quindi essere aperta usando la funzione [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) .

La modalità passthrough viene richiamata più spesso tramite la funzione [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , impostando il bit **\_ PassThrough LINEBEARERMODE** nel membro **dwBearerMode** della struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) a cui punta il parametro *lpCallParams* . Al termine di questa operazione, il provider di servizi apre la porta seriale al modem e inserisce immediatamente la chiamata in **LINECALLSTATE \_ connessa**. L'applicazione può quindi usare la funzione [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) con la classe Device "comm/DataModel" per ottenere un handle di file aperto per la lettura e la scrittura nella porta di comunicazione.

La modalità passthrough può essere richiamata anche in risposta a una chiamata in ingresso. In genere, le applicazioni richiamano la modalità passthrough mentre la chiamata si trova nell' **\_ offerta LINECALLSTATE**, prima della risposta alla chiamata. Anziché chiamare [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer), l'applicazione chiama [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams)passando il **pass- \_ through LINEBEARERMODE** come parametro *dwBearerMode* . Al termine di questa operazione, come per [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), la chiamata viene immediatamente posizionata in **LINECALLSTATE \_ connessa** dal provider di servizi e l'applicazione può ottenere un handle per la porta aperta usando [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). La funzione **lineSetCallParams** può essere chiamata quando la chiamata si trova in **LINECALLSTATE \_ offering**, **LINECALLSTATE \_ accepted** o **LINECALLSTATE \_ Connected**.

La modalità passthrough viene normalmente terminata chiamando [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) sull'handle di chiamata ottenuto da [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o il primo messaggio [**\_ CALLSTATE di riga**](line-callstate.md) , se la chiamata è una chiamata in ingresso. Il provider di servizi chiuderà la porta e ripristinerà lo stato predefinito del modem. L'applicazione deve chiamare [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) sull'handle ricevuto da [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

La modalità passthrough può anche essere terminata chiamando [**lineSetCallParams**](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) con il parametro *DwBearerMode* impostato su **LINEBEARERMODE \_ Voice**. È probabile che il tipo di supporto (Mode) impostato da [**lineSetMediaMode**](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode) sia attivo. Se **LINEMEDIAMODE \_ DataModel** è attivo, il provider di servizi assume la funzione di chiamata come se si trattasse di una chiamata al modem dati già in corso; se [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) viene chiamato successivamente, il provider di servizi emetterà i comandi del modem appropriati o le modifiche dello stato dell'interfaccia per eliminare una chiamata dati.

> [!Note]  
> Se la modalità passthrough viene terminata mentre è in corso la chiamata, il provider di servizi TAPI (TSP) per la riga potrebbe ripristinare lo stato predefinito delle impostazioni del modem. UniModel è un esempio di un TSP che ripristina sempre le impostazioni del modem quando termina la modalità passthrough. Per questo motivo, non è possibile usare la modalità passthrough come metodo per configurare il dispositivo. La modalità passthrough deve essere utilizzata solo per le attività distinte che possono essere considerate complete quando il passthrough viene terminato. Esempi di attività che possono usare la modalità passthrough includono l'invio di un fax o la riproduzione di dati Wave/audio tramite un protocollo modem proprietario.

 

 

 
