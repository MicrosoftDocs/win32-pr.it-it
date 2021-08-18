---
description: La funzione CreateTimerQueue crea una coda per i timer.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Code timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16e0ae30e02ad9fbc8889c0d7b1094895ebec27c3db8b67acf509ee02e9da85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885879"
---
# <a name="timer-queues"></a>Code timer

La [**funzione CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) crea una coda per i timer. I timer in questa coda, noti come *timer* della coda timer, sono oggetti leggeri che consentono di specificare una funzione di callback da chiamare quando arriva l'ora di scadenza specificata. L'operazione di attesa viene eseguita da un thread nel [pool di thread](../procthread/thread-pooling.md).

Per aggiungere un timer alla coda, chiamare la [**funzione CreateTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) Per aggiornare un timer della coda timer, chiamare la [**funzione ChangeTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) È possibile specificare una funzione di callback che deve essere eseguita da un thread di lavoro dal pool di thread alla scadenza del timer.

Per annullare un timer in sospeso, chiamare [**la funzione DeleteTimerQueueTimer.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) Al termine della coda di timer, chiamare la funzione [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) per eliminare la coda dei timer. Tutti i timer in sospeso nella coda vengono annullati ed eliminati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle code timer](using-timer-queues.md)
</dt> </dl>

 

 
