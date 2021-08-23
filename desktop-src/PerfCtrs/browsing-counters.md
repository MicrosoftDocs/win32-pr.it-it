---
description: Per visualizzare una finestra di dialogo che elenca gli oggetti prestazioni e i contatori definiti nel computer, chiamare la funzione PdhBrowseCounters.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Esplorazione dei contatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63278e0a531ec882bad6e102c89f6db0e0946a0d2a0a14b8736e7ee3aef6a8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011409"
---
# <a name="browsing-counters"></a>Esplorazione dei contatori

Per visualizzare una finestra di dialogo che elenca gli oggetti prestazioni e i contatori definiti nel computer, chiamare la [**funzione PdhBrowseCounters.**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) La finestra di dialogo consente all'utente di esplorare e selezionare i contatori delle prestazioni. Usare la struttura [**PDH \_ BROWSE \_ DLG \_ CONFIG**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) per specificare la configurazione della finestra di dialogo. Ad esempio, è possibile configurare la finestra di dialogo per restituire una o più selezioni.

In input, il **membro szReturnPathBuffer** contiene l'oggetto prestazioni e il contatore predefiniti selezionati nella finestra di dialogo. Nell'output, il buffer contiene l'oggetto prestazioni e il contatore selezionati dall'utente. È anche possibile usare il **membro pCallBack** per specificare una funzione di callback per elaborare i nomi dei contatori restituiti dalla finestra di dialogo.

Si noti che questa finestra di dialogo può restituire PDH DIALOG CANCELLED se \_ \_ **bSingleCounterPerDialog** è **FALSE** e l'utente fa clic sul pulsante Chiudi, quindi la gestione degli errori deve tenere conto di questo.

Per un esempio che usa la [**funzione PdhBrowseCounters,**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) vedere [Esplorazione dei contatori delle prestazioni](browsing-performance-counters.md).

Per recuperare un elenco di oggetti prestazioni nel computer, è anche possibile chiamare la [**funzione PdhEnumObjects.**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) Per recuperare un elenco di contatori e istanze per un oggetto prestazioni, chiamare la [**funzione PdhEnumObjectItems.**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) È anche possibile usare queste funzioni per identificare gli oggetti prestazioni e i contatori contenuti in un file di log. Le chiamate ripetute a **PdhEnumObjectItems** restituiranno lo stesso elenco di contatori e istanze finché non si chiama **PdhEnumObjects** per aggiornare prima l'elenco di oggetti prestazioni. Per un esempio che enumera oggetti e contatori, vedere [Enumerazione di oggetti processo](enumerating-process-objects.md).

## <a name="selecting-the-data-source"></a>Selezione dell'origine dati

È possibile usare [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) in combinazione con [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) per richiedere all'utente di selezionare se l'origine dati è in tempo reale o da un file di log e, se si tratta di un file di log, il nome. Se non si vuole visualizzare la finestra di dialogo dell'origine dati, è possibile chiamare **PdhSelectDataSource** per visualizzare solo il catalogo del browser di file. A tale scopo, specificare PDH FLAGS FILE BROWSER SOLO come secondo parametro della chiamata \_ \_ a \_ \_ **PdhSelectDataSource**.

 

 



