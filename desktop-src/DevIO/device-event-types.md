---
description: Per determinare il tipo di evento del dispositivo durante l'elaborazione di un messaggio \_ DEVICECHANGE WM, esaminare il parametro wParam.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Tipi di evento del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4d807cd7524d1906e86113c546306e08051ea80770900d42c1233364430e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636641"
---
# <a name="device-event-types"></a>Tipi di evento del dispositivo

Per determinare il tipo di evento del dispositivo durante [**l'elaborazione di un messaggio \_ DEVICECHANGE WM,**](wm-devicechange.md) esaminare il *parametro wParam.* Il valore *di wParam* determina il significato dei dati specifici dell'evento nel *parametro lParam.* In generale, i dati specifici dell'evento identificano il dispositivo e forniscono dettagli aggiuntivi sull'evento. Il formato di questi dati dipende dal tipo di dispositivo, ma i primi byte hanno sempre lo stesso formato della struttura [**DEV \_ BROADCAST \_ HDR.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) Per determinare il formato dei dati, controllare il **membro dbch \_ devicetype.**

Il sistema trasmette un evento del dispositivo di tipo [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) (ovvero un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) con *wParam* impostato su DBT DEVICEARRIVAL) ogni volta che un dispositivo è stato inserito ed è disponibile per \_ l'uso. Le applicazioni controllano in genere il tipo di dispositivo e iniziano a usare il dispositivo immediatamente, se appropriato.

Il sistema trasmette un evento [del dispositivo DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) per richiedere l'autorizzazione per rimuovere un dispositivo. Per determinare se è necessario il dispositivo, un'applicazione può visualizzare una finestra di dialogo per richiedere istruzioni all'utente. Se un'applicazione determina che è necessario il dispositivo, può negare questa richiesta e annullare la rimozione restituindo BROADCAST \_ QUERY \_ DENY. Se l'applicazione non richiede il dispositivo, deve restituire **TRUE.** Il sistema invia immediatamente un [messaggio DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) se un'applicazione o un driver ha annullato una richiesta precedente di rimozione di un dispositivo.

Il sistema trasmette un evento del dispositivo [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) come ultimo avviso prima della rimozione di un dispositivo. A questo punto, l'applicazione non può annullare la rimozione, quindi se usa il dispositivo deve prepararsi per la rimozione per evitare la perdita di dati. Ciò è particolarmente importante quando viene rimossa una connessione di rete. L'applicazione deve determinare se uno dei relativi file aperti o pipe si verifica in tale connessione. A tale scopo, confrontare l'identificatore di risorsa di rete nei dati specifici dell'evento del messaggio con gli identificatori di risorsa ottenuti in precedenza per i file e le pipe. Il sistema trasmette un evento del dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) quando un dispositivo è stato rimosso e non è più disponibile.

Il sistema trasmette un evento del dispositivo [DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md) per richiedere l'autorizzazione per modificare la configurazione corrente (ancoramento o disanco). Qualsiasi applicazione può restituire BROADCAST \_ QUERY DENY per negare la richiesta e annullare la \_ modifica. Se un'applicazione nega la richiesta, il sistema invia un [messaggio DBT \_ CONFIGCHANGECANCELED.](dbt-configchangecanceled.md) Se la configurazione corrente è stata modificata, a causa di un'ancoraggio o di un'operazione di annullamento, il sistema invia un [messaggio DBT \_ CONFIGCHANGED.](dbt-configchanged.md)

Il sistema trasmette un evento del dispositivo [DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md) ogni volta che si verifica un evento specifico del dispositivo.

I driver possono creare tipi di evento personalizzati. Gli eventi personalizzati vengono inviati solo all'applicazione registrata per la notifica degli eventi del dispositivo in un dispositivo specifico e possono essere avviati solo da driver in modalità kernel. Per altre informazioni, vedere [DBT \_ CUSTOMEVENT](dbt-customevent.md).

 

 



