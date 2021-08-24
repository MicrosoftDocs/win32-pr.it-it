---
title: Installazione e rimozione del decompressore e del decompressore
description: Installazione e rimozione del decompressore e del decompressore
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- gestione compressione video(VCM), installazione di dispositivi
- VCM (Video Compression Manager),installazione di dispositivi
- Funzione ICInstall
- Funzione ICRemove
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a34f1818f9a60226c0f3cead8186ae3fa163ebe1782c0c83e7cfb5b633c1b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144983"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Installazione e rimozione del decompressore e del decompressore

Un'applicazione può usare i decompressori e i decompressori già installati in un sistema che esegue microsoft Windows sistema operativo. Un'applicazione può anche installare le applicazioni e i decompressori per usi generali o speciali. La maggior parte delle applicazioni non dovrà installare o rimuovere le applicazioni o i decompressori perché in genere vengono installate da un programma di installazione. Un'applicazione potrebbe tuttavia installare direttamente un oggetto o installare una funzione come una funzione.

Un'applicazione può installare unprimere o un decompressore (o una funzione usata come un oggetto o un decompressore) usando la [**funzione ICInstall.**](/windows/desktop/api/Vfw/nf-vfw-icinstall) Questa funzione crea una voce nel Registro di sistema che identifica l'oggetto o il decompressore. L'applicazione o un'altra applicazione può eseguire ricerche nel Registro di sistema per determinare se il sistema contiene un oggetto o un decompressore adatto ai relativi dati. Usare **ICInstall per** installare tutti i driver di compressione e decompressione.

Un'applicazione può individuare e aprire un'applicazione installata o un decompressore usando le [**funzioni ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) [**e ICOpen.**](/windows/desktop/api/Vfw/nf-vfw-icopen) Quando un'applicazione completa l'uso di un'applicazione con un oggetto o un decompressore, la chiude usando la [**funzione ICClose.**](/windows/desktop/api/Vfw/nf-vfw-icclose)

Un'applicazione può rimuovere la voce del Registro di sistema per un oggetto o un decompressore installato usando la [**funzione ICRemove.**](/windows/desktop/api/Vfw/nf-vfw-icremove) Questa funzione rimuove la voce del Registro di sistema di un piccolo o decompressore che non è attualmente caricato in memoria.

Un'applicazione può limitare l'uso di un piccolo o decompressore installando, aprendo, chiudendo e rimuovendo l'applicazione.

In alternativa, per usare una funzione internamente come oggetto o decompressore senza installarla nel Registro di sistema, un'applicazione può usare la [**funzione ICOpenFunction.**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) Questa funzione richiede che l'applicazione chiamante abbia l'indirizzo della funzione da usare come oggetto o decompressore. Quando l'applicazione termina di usare la funzione , deve chiuderla usando **ICClose**. Poiché la funzione non è stata installata, l'applicazione non deve rimuovere la funzione dal Registro di sistema.

La struttura interna di una funzione usata come dispositivo di compressione o decompressore deve essere la stessa della funzione del punto di ingresso [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) usata dai driver installabili. Per altre informazioni sulla funzione del punto di ingresso **DriverProc,** vedere [Installable Drivers](installable-drivers.md).

> [!Note]  
> Un'applicazione che installa una funzione come piccolo o decompressore deve rimuovere la funzione prima che l'applicazione venga chiusa in modo che altre applicazioni non tetino di usare la funzione. Quando si rimuove una funzione, l'applicazione deve identificarla con il codice di quattro caratteri usato per installarla.

 

 

 