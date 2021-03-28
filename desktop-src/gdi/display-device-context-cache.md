---
description: Il sistema mantiene una cache dei contesti di dispositivo di visualizzazione usati per i contesti di dispositivo comuni, padre e finestra.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Visualizza la cache del contesto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994085"
---
# <a name="display-device-context-cache"></a><span data-ttu-id="8c4c4-103">Visualizza la cache del contesto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="8c4c4-103">Display Device Context Cache</span></span>

<span data-ttu-id="8c4c4-104">Il sistema mantiene una cache dei contesti di dispositivo di visualizzazione usati per i contesti di dispositivo comuni, padre e finestra.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-104">The system maintains a cache of display device contexts that it uses for common, parent, and window device contexts.</span></span> <span data-ttu-id="8c4c4-105">Il sistema Recupera un contesto di dispositivo dalla cache ogni volta che un'applicazione chiama la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ; il sistema restituisce il controller di dominio alla cache quando l'applicazione chiama successivamente la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) o [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="8c4c4-105">The system retrieves a device context from the cache whenever an application calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function; the system returns the DC to the cache when the application subsequently calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) or [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) function.</span></span>

<span data-ttu-id="8c4c4-106">Non esiste un limite predeterminato per la quantità di contesti di dispositivo che una cache può contenere. Se non ne è disponibile alcuno, il sistema crea un nuovo contesto di dispositivo di visualizzazione per la cache.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-106">There is no predetermined limit on the amount of device contexts that a cache can hold; the system creates a new display device context for the cache if none is available.</span></span> <span data-ttu-id="8c4c4-107">Dato questo, un'applicazione può avere più di cinque contesti di dispositivo attivi dalla cache alla volta.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-107">Given this, an application can have more than five active device contexts from the cache at a time.</span></span> <span data-ttu-id="8c4c4-108">Tuttavia, l'applicazione deve continuare a rilasciare questi contesti di dispositivo dopo l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-108">However, the application must continue to release these device contexts after use.</span></span> <span data-ttu-id="8c4c4-109">Poiché i nuovi contesti di dispositivo di visualizzazione per la cache vengono allocati nello spazio dell'heap dell'applicazione, non è possibile rilasciare i contesti di dispositivo, al fine di utilizzare tutto lo spazio dell'heap disponibile.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-109">Because new display device contexts for the cache are allocated in the application's heap space, failing to release the device contexts eventually consumes all available heap space.</span></span> <span data-ttu-id="8c4c4-110">Il sistema indica questo errore restituendo un errore quando non è possibile allocare spazio per il nuovo contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-110">The system indicates this failure by returning an error when it cannot allocate space for the new device context.</span></span> <span data-ttu-id="8c4c4-111">Anche altre funzioni non correlate alla cache possono restituire errori.</span><span class="sxs-lookup"><span data-stu-id="8c4c4-111">Other functions unrelated to the cache may also return errors.</span></span>

 

 



