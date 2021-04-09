---
description: Per determinare il tipo di evento del dispositivo durante l'elaborazione di un \_ messaggio WM DEVICECHANGE, esaminare il parametro wParam.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Tipi di evento del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ece6b810ba4d1310638bbfbdcdcaa7f67f79d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049185"
---
# <a name="device-event-types"></a>Tipi di evento del dispositivo

Per determinare il tipo di evento del dispositivo durante l'elaborazione di un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) , esaminare il parametro *wParam* . Il valore di *wParam* determina il significato dei dati specifici dell'evento nel parametro *lParam* . In generale, i dati specifici dell'evento identificano il dispositivo e forniscono dettagli aggiuntivi sull'evento. Il formato di questi dati dipende dal tipo di dispositivo, ma i primi byte hanno sempre lo stesso formato della struttura HDR per [**la \_ trasmissione \_ dello sviluppatore**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Per determinare il formato dei dati, controllare il membro **\_ DeviceType di dbch** .

Il sistema trasmette un evento del dispositivo di tipo [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) (ovvero un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT \_ DEVICEARRIVAL) ogni volta che un dispositivo è stato inserito ed è disponibile per l'uso. Le applicazioni in genere controllano il tipo di dispositivo e iniziano a usare immediatamente il dispositivo, se appropriato.

Il sistema trasmette un evento del dispositivo [ \_ DEVICEQUERYREMOVE DBT](dbt-devicequeryremove.md) per richiedere l'autorizzazione per la rimozione di un dispositivo. Per determinare se è necessario il dispositivo, un'applicazione può visualizzare una finestra di dialogo per richiedere istruzioni all'utente. Se un'applicazione determina la necessità del dispositivo, può negare questa richiesta e annullare la rimozione restituendo la query di trasmissione \_ \_ Deny. Se l'applicazione non richiede il dispositivo, deve restituire **true**. Il sistema invia immediatamente un messaggio [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) se un'applicazione o un driver ha annullato una richiesta precedente per rimuovere un dispositivo.

Il sistema trasmette un evento del dispositivo [ \_ DEVICEREMOVEPENDING di DBT](dbt-deviceremovepending.md) come ultimo avviso prima della rimozione di un dispositivo. A questo punto, l'applicazione non può annullare la rimozione, quindi se usa il dispositivo deve prepararsi per la rimozione per evitare la perdita di dati. Questa operazione è particolarmente importante quando viene rimossa una connessione di rete. L'applicazione deve determinare se uno dei relativi file o pipe aperti è presente in tale connessione. Questa operazione può essere eseguita confrontando l'identificatore di risorsa di rete nei dati specifici dell'evento del messaggio con gli identificatori di risorsa ottenuti in precedenza per i file e le pipe. Il sistema trasmette un evento [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) Device quando un dispositivo è stato rimosso e non è più disponibile.

Il sistema trasmette un evento [DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md) Device per richiedere l'autorizzazione per modificare la configurazione corrente (dock o Undock). Qualsiasi applicazione può restituire la \_ query broadcast \_ Deny per negare la richiesta e annullare la modifica. Se un'applicazione nega la richiesta, il sistema invia un messaggio [DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md) . Se la configurazione corrente è cambiata, a causa di un ancoraggio o di Undock, il sistema invia un messaggio [DBT \_ CONFIGCHANGED](dbt-configchanged.md) .

Il sistema trasmette un evento del dispositivo [ \_ DEVICETYPESPECIFIC di DBT](dbt-devicetypespecific.md) ogni volta che si verifica un evento specifico del dispositivo.

I driver possono creare tipi di evento personalizzati. Gli eventi personalizzati vengono inviati solo all'applicazione che ha eseguito la registrazione per la notifica degli eventi del dispositivo su un dispositivo specifico e possono essere avviati solo dai driver in modalità kernel. Per ulteriori informazioni, vedere [DBT \_ CUSTOMEVENT](dbt-customevent.md).

 

 



