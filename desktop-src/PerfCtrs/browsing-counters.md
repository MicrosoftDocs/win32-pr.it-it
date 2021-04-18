---
description: Per visualizzare una finestra di dialogo in cui sono elencati gli oggetti e i contatori delle prestazioni definiti nel computer, chiamare la funzione PdhBrowseCounters.
ms.assetid: f2fac1d3-f643-43c9-a445-112015baecdd
title: Esplorazione dei contatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4bae5ce5ae7a21ae247cf66515f7386b8d0265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312189"
---
# <a name="browsing-counters"></a>Esplorazione dei contatori

Per visualizzare una finestra di dialogo in cui sono elencati gli oggetti e i contatori delle prestazioni definiti nel computer, chiamare la funzione [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) . La finestra di dialogo consente all'utente di esplorare e selezionare i contatori delle prestazioni. Usare la struttura [**di \_ \_ \_ configurazione PDH browse DLG**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a) per specificare la configurazione della finestra di dialogo. Ad esempio, è possibile configurare la finestra di dialogo per restituire una selezione o più selezioni.

In input il membro **szReturnPathBuffer** contiene l'oggetto prestazioni predefinito e il contatore selezionato nella finestra di dialogo. Nell'output, il buffer contiene l'oggetto prestazioni e il contatore selezionato dall'utente. È anche possibile usare il membro **pCallback** per specificare una funzione di callback per elaborare i nomi dei contatori restituiti dalla finestra di dialogo.

Si noti che questa finestra di dialogo può restituire la \_ finestra di dialogo PDH \_ annullata se **bSingleCounterPerDialog** è **false** e l'utente fa clic sul pulsante Chiudi, quindi la gestione degli errori avrebbe dovuto tenere conto di questa situazione.

Per un esempio in cui viene usata la funzione [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) , vedere [esplorazione dei contatori delle prestazioni](browsing-performance-counters.md).

Per recuperare un elenco di oggetti prestazioni nel computer, è anche possibile chiamare la funzione [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) . Per recuperare un elenco di contatori e istanze per un oggetto prestazione, chiamare la funzione [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) . È inoltre possibile utilizzare queste funzioni per identificare gli oggetti e i contatori delle prestazioni contenuti in un file di log. Le chiamate ripetute a **PdhEnumObjectItems** restituiranno lo stesso elenco di contatori e istanze fino a quando non si chiama **PdhEnumObjects** per aggiornare prima l'elenco di oggetti prestazione. Per un esempio in cui vengono enumerati gli oggetti e i contatori, vedere [enumerazione di oggetti processo](enumerating-process-objects.md).

## <a name="selecting-the-data-source"></a>Selezione dell'origine dati

È possibile utilizzare [**PdhSelectDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhselectdatasourcea) insieme a [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) per richiedere all'utente di specificare se l'origine dati è in tempo reale o da un file di log e, se si tratta di un file di log, il relativo nome. Se non si desidera che venga visualizzata la finestra di dialogo dell'origine dati, è possibile chiamare **PdhSelectDataSource** per visualizzare solo il catalogo di file browser. A tale scopo, specificare PDH \_ flags \_ file \_ browser \_ solo come secondo parametro della chiamata a **PdhSelectDataSource**.

 

 



