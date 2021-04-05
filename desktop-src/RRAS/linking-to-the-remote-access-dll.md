---
title: Collegamento alla DLL di accesso remoto
description: Se un'applicazione è collegata in modo statico alla DLL RASAPI32, l'applicazione non verrà caricata se il servizio di accesso remoto non è installato.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872781"
---
# <a name="linking-to-the-remote-access-dll"></a><span data-ttu-id="60225-103">Collegamento alla DLL di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="60225-103">Linking to the Remote Access DLL</span></span>

<span data-ttu-id="60225-104">Se un'applicazione è collegata in modo statico alla DLL RASAPI32, l'applicazione non verrà caricata se il servizio di accesso remoto non è installato.</span><span class="sxs-lookup"><span data-stu-id="60225-104">If an application links statically to the RASAPI32 DLL, the application will fail to load if Remote Access Service is not installed.</span></span> <span data-ttu-id="60225-105">È possibile caricare un'applicazione RAS quando RAS non è installato utilizzando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare la dll e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere i puntatori alle funzioni RAS.</span><span class="sxs-lookup"><span data-stu-id="60225-105">A RAS application can load when RAS is not installed by using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load the DLL, and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain pointers to the RAS functions.</span></span>

<span data-ttu-id="60225-106">Le funzioni RAS si trovano in RASAPI32.DLL.</span><span class="sxs-lookup"><span data-stu-id="60225-106">The RAS functions are located in RASAPI32.DLL.</span></span> <span data-ttu-id="60225-107">La libreria di importazione per queste funzioni è RASAPI32. LIB.</span><span class="sxs-lookup"><span data-stu-id="60225-107">The import library for these functions is RASAPI32.LIB.</span></span> <span data-ttu-id="60225-108">Per utilizzare le funzioni RAS, i programmi devono includere i seguenti file:</span><span class="sxs-lookup"><span data-stu-id="60225-108">To use the RAS functions, your programs must include the following files:</span></span>



| <span data-ttu-id="60225-109">File</span><span class="sxs-lookup"><span data-stu-id="60225-109">File</span></span>       | <span data-ttu-id="60225-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60225-110">Description</span></span>                                                                 |
|------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="60225-111">Ras. H</span><span class="sxs-lookup"><span data-stu-id="60225-111">RAS.H</span></span>      | <span data-ttu-id="60225-112">Contiene i prototipi di funzione RAS, le costanti e le definizioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="60225-112">Contains the RAS function prototypes, constants, and structure definitions.</span></span> |
| <span data-ttu-id="60225-113">RASERROR. H</span><span class="sxs-lookup"><span data-stu-id="60225-113">RASERROR.H</span></span> | <span data-ttu-id="60225-114">Contiene i codici di errore RAS.</span><span class="sxs-lookup"><span data-stu-id="60225-114">Contains the RAS error codes.</span></span>                                               |



 

 

 