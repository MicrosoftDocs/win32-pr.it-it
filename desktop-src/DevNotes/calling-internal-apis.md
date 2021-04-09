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
# <a name="calling-internal-apis"></a><span data-ttu-id="dcf4c-104">Chiamata di API interne</span><span class="sxs-lookup"><span data-stu-id="dcf4c-104">Calling Internal APIs</span></span>

<span data-ttu-id="dcf4c-105">Il file di intestazione Winternl. h espone i prototipi delle API Windows interne.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-105">The Winternl.h header file exposes prototypes of internal Windows APIs.</span></span> <span data-ttu-id="dcf4c-106">Non esiste alcuna libreria di importazione associata, quindi gli sviluppatori devono usare il collegamento dinamico in fase di esecuzione per chiamare le funzioni descritte in questo file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-106">There is no associated import library, so developers must use run-time dynamic linking to call the functions described in this header file.</span></span>

<span data-ttu-id="dcf4c-107">Le funzioni e le strutture in Winternl. h sono interne al sistema operativo e sono soggette a modifiche da una versione di Windows alla successiva e possibilmente anche tra i Service Pack per ogni versione.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-107">The functions and structures in Winternl.h are internal to the operating system and subject to change from one release of Windows to the next, and possibly even between service packs for each release.</span></span> <span data-ttu-id="dcf4c-108">Per mantenere la compatibilità dell'applicazione, è consigliabile usare invece le funzioni pubbliche equivalenti.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-108">To maintain the compatibility of your application, you should use the equivalent public functions instead.</span></span> <span data-ttu-id="dcf4c-109">Ulteriori informazioni sono disponibili nel file di intestazione Winternl. h e nella documentazione per ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-109">Further information is available in the header file, Winternl.h, and the documentation for each function.</span></span>

<span data-ttu-id="dcf4c-110">Se si usano queste funzioni, è possibile accedervi tramite il collegamento dinamico in fase di esecuzione usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="dcf4c-110">If you do use these functions, you can access them through run-time dynamic linking using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="dcf4c-111">In questo modo il codice può rispondere normalmente se la funzione è stata modificata o rimossa dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-111">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="dcf4c-112">Le modifiche alla firma, tuttavia, potrebbero non essere rilevabili.</span><span class="sxs-lookup"><span data-stu-id="dcf4c-112">Signature changes, however, may not be detectable.</span></span>

 

 
