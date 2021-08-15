---
description: Il file di intestazione Winternl.h espone prototipi di API Windows interno. Non esiste alcuna libreria di importazione associata, pertanto gli sviluppatori devono usare il collegamento dinamico in fase di esecuzione per chiamare le funzioni descritte in questo file di intestazione.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Chiamata di API interne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c613b4f650709eb9764eff133c018be62768c58212b4dc7130149ce8b5173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956130"
---
# <a name="calling-internal-apis"></a>Chiamata di API interne

Il file di intestazione Winternl.h espone prototipi di API Windows interno. Non esiste alcuna libreria di importazione associata, pertanto gli sviluppatori devono usare il collegamento dinamico in fase di esecuzione per chiamare le funzioni descritte in questo file di intestazione.

Le funzioni e le strutture in Winternl.h sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows alla successiva e possibilmente anche tra service pack per ogni versione. Per mantenere la compatibilità dell'applicazione, è consigliabile usare le funzioni pubbliche equivalenti. Altre informazioni sono disponibili nel file di intestazione, Winternl.h, e nella documentazione per ogni funzione.

Se si usano queste funzioni, è possibile accedervi tramite il collegamento dinamico in fase di esecuzione usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). In questo modo il codice può rispondere correttamente se la funzione è stata modificata o rimossa dal sistema operativo. Le modifiche alla firma, tuttavia, potrebbero non essere rilevabili.

 

 
