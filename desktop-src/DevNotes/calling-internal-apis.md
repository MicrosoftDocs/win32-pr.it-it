---
description: Il file di intestazione Winternl. h espone i prototipi delle API Windows interne. Non esiste alcuna libreria di importazione associata, quindi gli sviluppatori devono usare il collegamento dinamico in fase di esecuzione per chiamare le funzioni descritte in questo file di intestazione.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Chiamata di API interne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966082"
---
# <a name="calling-internal-apis"></a>Chiamata di API interne

Il file di intestazione Winternl. h espone i prototipi delle API Windows interne. Non esiste alcuna libreria di importazione associata, quindi gli sviluppatori devono usare il collegamento dinamico in fase di esecuzione per chiamare le funzioni descritte in questo file di intestazione.

Le funzioni e le strutture in Winternl. h sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows alla successiva e possibilmente anche tra i Service Pack per ogni versione. Per mantenere la compatibilità dell'applicazione, è consigliabile usare invece le funzioni pubbliche equivalenti. Ulteriori informazioni sono disponibili nel file di intestazione Winternl. h e nella documentazione per ogni funzione.

Se si usano queste funzioni, è possibile accedervi tramite il collegamento dinamico in fase di esecuzione usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). In questo modo il codice può rispondere normalmente se la funzione è stata modificata o rimossa dal sistema operativo. Le modifiche alla firma, tuttavia, potrebbero non essere rilevabili.

 

 
