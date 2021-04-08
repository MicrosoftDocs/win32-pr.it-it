---
description: I blocchi opportunistici vengono richiesti aprendo prima un file con le autorizzazioni e i flag appropriati all'applicazione per l'apertura del file. Tutti i file per i quali verranno richiesti blocchi opportunistici devono essere aperti per operazioni sovrapposte (asincrone).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Come richiedere un blocco opportunistico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884882"
---
# <a name="how-to-request-an-opportunistic-lock"></a>Come richiedere un blocco opportunistico

Le applicazioni client richiedono direttamente blocchi opportunistici solo quando il blocco è destinato a un file nel server locale. Quando si accede a file su server remoti, è il redirector di rete e non l'applicazione client che richiede il blocco opportunistico dal server remoto.

I blocchi opportunistici vengono richiesti aprendo prima un file con le autorizzazioni e i flag appropriati all'applicazione per l'apertura del file. Tutti i file per i quali verranno richiesti blocchi opportunistici devono essere aperti per operazioni sovrapposte (asincrone). Dopo l'apertura dei file per un'operazione sovrapposta, utilizzare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con il codice di controllo appropriato per richiedere un blocco opportunistico. Per un elenco delle operazioni di blocco opportunistiche, vedere [operazioni di blocco opportunistiche](opportunistic-lock-operations.md).

Alle applicazioni viene notificato che un blocco opportunistico viene rotto utilizzando il membro **hEvent** della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associata al file. Le applicazioni possono anche usare funzioni quali [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) e [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted). L'applicazione è responsabile dell'associazione del file corretto al blocco opportunistico rotto.

Per ulteriori informazioni sulla notifica, vedere [sincronizzazione](/windows/desktop/Sync/synchronization).

 

 
