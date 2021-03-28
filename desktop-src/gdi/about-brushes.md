---
description: 'Esistono due tipi di pennelli: logico e fisico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Informazioni sui pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130366"
---
# <a name="about-brushes"></a><span data-ttu-id="61651-103">Informazioni sui pennelli</span><span class="sxs-lookup"><span data-stu-id="61651-103">About Brushes</span></span>

<span data-ttu-id="61651-104">Esistono due tipi di pennelli: logico e fisico.</span><span class="sxs-lookup"><span data-stu-id="61651-104">There are two types of brushes: logical and physical.</span></span> <span data-ttu-id="61651-105">Un *pennello logico* è una descrizione della bitmap ideale utilizzata da un'applicazione per disegnare forme.</span><span class="sxs-lookup"><span data-stu-id="61651-105">A *logical brush* is a description of the ideal bitmap that an application uses to paint shapes.</span></span> <span data-ttu-id="61651-106">Un *pennello fisico* è la bitmap effettiva creata da un driver di dispositivo in base alla definizione del pennello logico di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61651-106">A *physical brush* is the actual bitmap that a device driver creates based on an application's logical-brush definition.</span></span> <span data-ttu-id="61651-107">Per ulteriori informazioni sulle bitmap, vedere [bitmap](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="61651-107">For more information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

<span data-ttu-id="61651-108">Quando un'applicazione chiama una delle funzioni che creano un pennello, viene recuperato un handle che identifica un pennello logico.</span><span class="sxs-lookup"><span data-stu-id="61651-108">When an application calls one of the functions that creates a brush, it retrieves a handle that identifies a logical brush.</span></span> <span data-ttu-id="61651-109">Quando l'applicazione passa questo handle alla funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , il driver di dispositivo per la visualizzazione o la stampante corrispondente crea il pennello fisico.</span><span class="sxs-lookup"><span data-stu-id="61651-109">When the application passes this handle to the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function, the device driver for the corresponding display or printer creates the physical brush.</span></span>

<span data-ttu-id="61651-110">Negli argomenti seguenti vengono descritti i pennelli:</span><span class="sxs-lookup"><span data-stu-id="61651-110">The following topics describe brushes:</span></span>

-   [<span data-ttu-id="61651-111">Origine pennello</span><span class="sxs-lookup"><span data-stu-id="61651-111">Brush Origin</span></span>](brush-origin.md)
-   [<span data-ttu-id="61651-112">Tipi di pennelli logici</span><span class="sxs-lookup"><span data-stu-id="61651-112">Logical Brush Types</span></span>](logical-brush-types.md)
-   [<span data-ttu-id="61651-113">Modello di trasferimento del blocco</span><span class="sxs-lookup"><span data-stu-id="61651-113">Pattern Block Transfer</span></span>](pattern-block-transfer.md)
-   [<span data-ttu-id="61651-114">Funzioni pennello abilitate per ICM</span><span class="sxs-lookup"><span data-stu-id="61651-114">ICM-Enabled Brush Functions</span></span>](icm-enabled-brush-functions.md)

 

 



