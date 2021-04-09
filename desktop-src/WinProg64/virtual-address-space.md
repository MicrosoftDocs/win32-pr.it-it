---
title: Spazio degli indirizzi virtuali (Guida per programmatori per Windows a 64 bit)
description: Per impostazione predefinita, le applicazioni basate su Microsoft Windows a 64 bit hanno uno spazio degli indirizzi in modalità utente di diversi terabyte.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guida per programmatori Windows a 64 bit-programmazione Windows a 64 bit, spazio degli indirizzi virtuali
- spazio degli indirizzi virtuali programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047666"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Spazio degli indirizzi virtuali (Guida per programmatori per Windows a 64 bit)

Per impostazione predefinita, le applicazioni basate su Microsoft Windows a 64 bit hanno uno spazio degli indirizzi in modalità utente di diversi terabyte. Per i valori esatti, vedere [limiti di memoria per le versioni di Windows e Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases). Tuttavia, le applicazioni possono specificare che il sistema deve allocare tutta la memoria per l'applicazione inferiore a 2 gigabyte. Questa funzionalità è utile per le applicazioni a 64 bit se vengono soddisfatte le condizioni seguenti:

-   È sufficiente uno spazio degli indirizzi di 2 GB.
-   Il codice presenta molti avvisi di troncamento del puntatore.
-   I puntatori e i numeri interi sono liberamente combinati.
-   Il codice ha un polimorfismo che usa tipi di dati a 32 bit.

Tutti i puntatori sono ancora puntatori a 64 bit, ma il sistema garantisce che ogni allocazione di memoria si verifichi al di sotto del limite di 2 GB, in modo che se l'applicazione tronca un puntatore, non viene perso alcun dato significativo. È possibile troncare i puntatori a valori a 32 bit, quindi estenderli a valori a 64 bit in base all'estensione del segno o all'estensione zero.

Per specificare questa limitazione della memoria, usare l'opzione **/LARGEADDRESSAWARE: No** linker. Si noti che **/LARGEADDRESSAWARE: No** viene ignorato per un file binario arm64. Tuttavia, tenere presente che possono verificarsi problemi quando si utilizza questa opzione. Se si compila una DLL che usa questa opzione e la DLL viene chiamata da un'applicazione che non usa questa opzione, la DLL potrebbe troncare un puntatore a 64 bit i cui 32 bit superiori sono significativi. Questo può causare un errore dell'applicazione senza alcun avviso.

 

 
