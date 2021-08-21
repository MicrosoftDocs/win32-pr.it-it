---
title: Spazio di indirizzi virtuali (Guida per programmatori per i Windows a 64 bit)
description: Per impostazione predefinita, le applicazioni basate Windows Microsoft a 64 bit hanno uno spazio degli indirizzi in modalità utente di diversi terabyte.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guida alla programmazione a 64 bit Windows programmazione a 64 bit Windows programmazione , spazio di indirizzi virtuali
- spazio indirizzi virtuale programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2e673befb66c45501558effb37f3d04ee1a99199010f8cca89abb2cb31c6d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113371"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Spazio di indirizzi virtuali (Guida per programmatori per i Windows a 64 bit)

Per impostazione predefinita, le applicazioni basate Windows Microsoft a 64 bit hanno uno spazio degli indirizzi in modalità utente di diversi terabyte. Per valori precisi, vedere [Limiti di memoria per Windows e Windows Server.](/windows/desktop/Memory/memory-limits-for-windows-releases) Tuttavia, le applicazioni possono specificare che il sistema deve allocare tutta la memoria per l'applicazione al di sotto di 2 gigabyte. Questa funzionalità è utile per le applicazioni a 64 bit se si verificano le condizioni seguenti:

-   È sufficiente uno spazio indirizzi di 2 GB.
-   Il codice presenta molti avvisi di troncamento del puntatore.
-   Puntatori e interi sono liberamente misti.
-   Il codice ha il polimorfismo usando tipi di dati a 32 bit.

Tutti i puntatori sono ancora puntatori a 64 bit, ma il sistema garantisce che ogni allocazione di memoria si verifichi al di sotto del limite di 2 GB, in modo che se l'applicazione tronca un puntatore, non vengono persi dati significativi. I puntatori possono essere troncati a valori a 32 bit, quindi estesi a valori a 64 bit tramite l'estensione del segno o l'estensione zero.

Per specificare questa limitazione di memoria, usare l'opzione del linker **/LARGEADDRESSAWARE:NO.** Si noti **che /LARGEADDRESSAWARE:NO** viene ignorato per un file binario ARM64. Tenere tuttavia presente che possono verificarsi problemi quando si usa questa opzione. Se si compila una DLL che utilizza questa opzione e la DLL viene chiamata da un'applicazione che non utilizza questa opzione, la DLL potrebbe troncare un puntatore a 64 bit i cui 32 bit superiori sono significativi. Ciò può causare un errore dell'applicazione senza alcun avviso.

 

 
