---
description: Il servizio di ordinamento dei thread controlla l'esecuzione di uno o più thread client. Garantisce che ogni thread client venga eseguito una sola volta durante il periodo specificato e in ordine relativo.
ms.assetid: 5c37873a-ced4-447e-a6e1-55cfa8ab24b4
title: Servizio di ordinamento thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b3cd12b26124b47d506585425388a4542a70df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311952"
---
# <a name="thread-ordering-service"></a>Servizio di ordinamento thread

Il *servizio di ordinamento dei thread* controlla l'esecuzione di uno o più thread client. Garantisce che ogni thread client venga eseguito una sola volta durante il periodo specificato e in ordine relativo.

**Windows Server 2003 e Windows XP:** Il servizio di ordinamento dei thread è disponibile a partire da Windows Vista e Windows Server 2008.

Il servizio di ordinamento dei thread è disattivato per impostazione predefinita e deve essere avviato dall'utente. Mentre il servizio di ordinamento dei thread è in esecuzione, viene attivato ogni 5 secondi per verificare se è presente una nuova richiesta, anche se il sistema è inattivo. In questo modo si impedisce che il sistema venga sospeso per più di 5 secondi, causando un maggiore consumo di energia. Se l'efficienza energetica è cruciale per l'applicazione, è preferibile non usare il servizio di ordinamento dei thread e consentire invece all'utilità di pianificazione di sistema di gestire l'esecuzione dei thread.

Ogni thread del client appartiene a un *gruppo di ordini di thread*. Il *thread padre* crea uno o più gruppi di ordinamento dei thread chiamando la funzione [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup) . Il thread padre usa questa funzione per specificare il periodo per il gruppo di ordinamento dei thread e un intervallo di timeout.

Thread client aggiuntivi chiamano la funzione [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup) per partecipare a un gruppo di ordinamento thread esistente. Questi thread indicano se devono essere un predecessore o un successore al thread padre nell'ordine di esecuzione. Ogni thread del client dovrebbe completare una determinata quantità di elaborazione ogni periodo. Tutti i thread all'interno del gruppo devono completare l'esecuzione entro il periodo più l'intervallo di timeout.

I thread di un gruppo di ordinamento dei thread racchiudono il codice di elaborazione all'interno di un ciclo controllato dalla funzione [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) . In primo luogo, i thread precedenti vengono eseguiti uno alla volta nell'ordine in cui sono stati aggiunti al gruppo, mentre i thread padre e successore sono bloccati nelle chiamate a **AvRtWaitOnThreadOrderingGroup**. Quando ogni thread precedente termina con l'elaborazione, il controllo dell'esecuzione torna all'inizio del ciclo di elaborazione e il thread chiama di nuovo **AvRtWaitOnThreadOrderingGroup** per bloccarsi fino al successivo turno. Dopo che tutti i thread precedenti hanno chiamato questa funzione, il servizio di ordinamento dei thread può pianificare il thread padre. Infine, quando il thread padre termina l'elaborazione e chiama di nuovo **AvRtWaitOnThreadOrderingGroup** , il servizio di ordinamento dei thread può pianificare i thread successivi uno alla volta nell'ordine in cui sono stati aggiunti al gruppo. Se tutti i thread completano l'esecuzione prima del termine di un periodo, tutti i thread restano in attesa fino a quando il resto del periodo non scade prima che venga eseguita di nuovo.

Quando il client non deve più essere eseguito come parte del gruppo di ordinamento dei thread, chiama la funzione [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup) per rimuovere se stessa dal gruppo. Si noti che il thread padre non deve rimuovere se stesso da un gruppo di ordinamento dei thread. Se un thread non completa l'esecuzione prima della scadenza del periodo più l'intervallo di timeout, viene eliminato dal gruppo.

Il thread padre chiama la funzione [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup) per eliminare il gruppo di ordinamento dei thread. Anche il gruppo di ordinamento dei thread viene eliminato definitivamente se il thread padre non completa l'esecuzione prima del periodo più lungo dell'intervallo di timeout. Quando il gruppo di ordinamento dei thread viene eliminato definitivamente, le chiamate a [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) dai thread di tale gruppo hanno esito negativo o si verifica il timeout.

 

 



