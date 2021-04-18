---
description: La funzione CreateTimerQueue ha provocato crea una coda per i timer.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Code timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312745"
---
# <a name="timer-queues"></a>Code timer

La funzione [**CreateTimerQueue ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) crea una coda per i timer. I timer in questa coda, detti timer della *coda del timer*, sono oggetti leggeri che consentono di specificare una funzione di callback da chiamare quando arriva il tempo di scadenza specificato. L'operazione Wait viene eseguita da un thread nel [pool di thread](../procthread/thread-pooling.md).

Per aggiungere un timer alla coda, chiamare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) . Per aggiornare un timer della coda del timer, chiamare la funzione [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) . È possibile specificare una funzione di callback che deve essere eseguita da un thread di lavoro dal pool di thread quando il timer scade.

Per annullare un timer in sospeso, chiamare la funzione [**DeleteTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) . Al termine della coda di timer, chiamare la funzione [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) per eliminare la coda del timer. Eventuali timer in sospeso nella coda vengono annullati ed eliminati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle code timer](using-timer-queues.md)
</dt> </dl>

 

 
