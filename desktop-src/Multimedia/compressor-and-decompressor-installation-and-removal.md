---
title: Installazione e rimozione di compressori e decompressori
description: Installazione e rimozione di compressori e decompressori
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- Gestione compressione video (VCM), installazione di compressatori
- VCM (Video Compression Manager), installazione dei commediatori
- ICInstall (funzione)
- ICRemove (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd65f0fc06dc1d5e90cb136f5cf4ea429c220d77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336903"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Installazione e rimozione di compressori e decompressori

Un'applicazione può usare i comprimeri e i decompressori già installati in un sistema che esegue il sistema operativo Microsoft Windows. Un'applicazione può inoltre installare i comprimeri e i decompressori per usi generali o speciali. Per la maggior parte delle applicazioni non sarà necessario installare o rimuovere i compressori o i decompressori perché vengono in genere installati da un programma di installazione. Un'applicazione può, tuttavia, installare direttamente un compressore o installare una funzione come compressore.

Un'applicazione può installare un compressore o un decompressore (o una funzione usata come compressore o decompressore) usando la funzione [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) . Questa funzione crea una voce nel registro di sistema che identifica il compressore o il decompressore. L'applicazione o un'altra applicazione può eseguire ricerche nel registro di sistema per determinare se il sistema contiene un compressore o un decompressore adatto ai propri dati. Usare **ICInstall** per installare tutti i driver di compressione e decompressione.

Un'applicazione è in grado di individuare e aprire un compressore o un decompressore installato utilizzando le funzioni [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) e [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . Quando un'applicazione termina usando un compressore o un decompressore, lo chiude usando la funzione [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) .

Un'applicazione può rimuovere la voce del registro di sistema per un compressore o un decompressore installato utilizzando la funzione [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove) . Questa funzione rimuove la voce del registro di sistema di un compressore o di un decompressore che non è attualmente caricato in memoria.

Un'applicazione può limitare l'uso di un compressore o di un decompressore mediante l'installazione, l'apertura, la chiusura e la rimozione.

In alternativa, per usare una funzione internamente come compressore o decompressore senza installarla nel registro di sistema, un'applicazione può usare la funzione [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) . Questa funzione richiede che l'applicazione chiamante disponga dell'indirizzo della funzione da usare come compressore o decompressore. Quando l'applicazione termina utilizzando la funzione, è necessario chiuderla utilizzando **ICClose**. Poiché la funzione non è stata installata, non è necessario che l'applicazione rimuova la funzione dal registro di sistema.

La struttura interna di una funzione usata come compressore o decompressore deve essere la stessa della funzione del punto di ingresso [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) usata dai driver installabili. Per ulteriori informazioni sulla funzione del punto di ingresso **DriverProc** , vedere [driver installabili](installable-drivers.md).

> [!Note]  
> Un'applicazione che installa una funzione come compressore o decompressore deve rimuovere la funzione prima che l'applicazione venga chiusa, in modo che le altre applicazioni non tentino di utilizzare la funzione. Quando si rimuove una funzione, l'applicazione deve identificarla con il codice di quattro caratteri usato per installarlo.

 

 

 