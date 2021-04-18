---
title: Sistema colori Windows
description: Gli schemi di gestione colori sono implementati nei sistemi operativi Microsoft Windows per migliorare il rendering del contenuto dei colori in tutte le forme di comunicazione digitale. Lo schema di gestione dei colori usato a partire da Windows 2000, Windows XP e Windows Server 2003 è denominato MCI (Image Color Management) 2,0. Lo schema di gestione colori usato a partire da Windows Vista è denominato Windows Color System (WCS) 1,0. Lo schema di gestione dei colori WCS 1,0 è un superset di API e funzionalità di ICM 2,0.
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ccb84caa4ff10ab4c97115b9759730cd0ef26
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320900"
---
# <a name="windows-color-system"></a><span data-ttu-id="cf80d-105">Sistema colori Windows</span><span class="sxs-lookup"><span data-stu-id="cf80d-105">Windows Color System</span></span>

## <a name="purpose"></a><span data-ttu-id="cf80d-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="cf80d-106">Purpose</span></span>

<span data-ttu-id="cf80d-107">Gli schemi di gestione colori sono implementati nei sistemi operativi Microsoft Windows per migliorare il rendering del contenuto dei colori in tutte le forme di comunicazione digitale.</span><span class="sxs-lookup"><span data-stu-id="cf80d-107">Color management schemes are implemented in Microsoft Windows operating systems to improve the rendering of color content in all forms of digital communication.</span></span>

<span data-ttu-id="cf80d-108">Lo schema di gestione dei colori usato a partire da Windows 2000, Windows XP e Windows Server 2003 è denominato MCI (Image Color Management) 2,0.</span><span class="sxs-lookup"><span data-stu-id="cf80d-108">The color management scheme that's used starting with Windows 2000, Windows XP, and Windows Server 2003 is called Image Color Management (ICM) 2.0.</span></span> <span data-ttu-id="cf80d-109">Lo schema di gestione colori usato a partire da Windows Vista è denominato Windows Color System (WCS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="cf80d-109">The color management scheme that's used starting with Windows Vista is called Windows Color System (WCS) 1.0.</span></span> <span data-ttu-id="cf80d-110">Lo schema di gestione dei colori WCS 1,0 è un superset di API e funzionalità di ICM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cf80d-110">The WCS 1.0 color management scheme is a superset of ICM 2.0 APIs and functionality.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="cf80d-111">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="cf80d-111">Where applicable</span></span>

<span data-ttu-id="cf80d-112">ICM può essere usato in tutte le applicazioni in Windows 2000 e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="cf80d-112">ICM can be used in all applications on Windows 2000 and later operating systems.</span></span> <span data-ttu-id="cf80d-113">Il servizio WCS può essere usato in tutte le applicazioni in Windows Vista e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="cf80d-113">WCS can be used in all applications on Windows Vista and later operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cf80d-114">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="cf80d-114">Developer audience</span></span>

<span data-ttu-id="cf80d-115">L'API WCS è progettata per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="cf80d-115">The WCS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="cf80d-116">Sono necessari familiarità con l'interfaccia utente grafica di Windows, l'architettura basata su messaggi e una conoscenza approfondita dei concetti relativi alla gestione dei colori.</span><span class="sxs-lookup"><span data-stu-id="cf80d-116">Familiarity with the Windows graphical user interface, message-driven architecture, and a working knowledge of color management concepts are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cf80d-117">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="cf80d-117">Run-time requirements</span></span>

<span data-ttu-id="cf80d-118">Le applicazioni che usano l'API ICM richiedono Windows 2000 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="cf80d-118">Applications that use the ICM API require Windows 2000 or later.</span></span> <span data-ttu-id="cf80d-119">Le applicazioni che usano l'API WCS richiedono Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cf80d-119">Applications that use the WCS API require Windows Vista or later.</span></span> <span data-ttu-id="cf80d-120">Per informazioni specifiche sulla fase di esecuzione in una funzione, vedere la sezione requisiti della pagina di riferimento per tale funzione.</span><span class="sxs-lookup"><span data-stu-id="cf80d-120">For specific run-time information on a function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cf80d-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cf80d-121">In this section</span></span>

-   [<span data-ttu-id="cf80d-122">Considerazioni sulla sicurezza: sistema colori Windows</span><span class="sxs-lookup"><span data-stu-id="cf80d-122">Security Considerations: Windows Color System</span></span>](security-considerations--windows-color-system.md)
-   [<span data-ttu-id="cf80d-123">Concetti di base sulla gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="cf80d-123">Basic color management concepts</span></span>](basic-color-management-concepts.md)
-   [<span data-ttu-id="cf80d-124">Schemi e algoritmi del sistema di colori Windows</span><span class="sxs-lookup"><span data-stu-id="cf80d-124">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
-   [<span data-ttu-id="cf80d-125">Informazioni su Windows Color System versione 1,0</span><span class="sxs-lookup"><span data-stu-id="cf80d-125">About Windows Color System Version 1.0</span></span>](about-windows-color-system-version-1-0.md)
-   [<span data-ttu-id="cf80d-126">Uso di WCS 1,0</span><span class="sxs-lookup"><span data-stu-id="cf80d-126">Using WCS 1.0</span></span>](using-wcs-1-0.md)
-   [<span data-ttu-id="cf80d-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cf80d-127">Reference</span></span>](reference.md)
-   [<span data-ttu-id="cf80d-128">Glossario 1,0 di WCS</span><span class="sxs-lookup"><span data-stu-id="cf80d-128">WCS 1.0 Glossary</span></span>](wcs-1-0-glossary.md)

## <a name="related-topics"></a><span data-ttu-id="cf80d-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf80d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf80d-130">OpenGL</span><span class="sxs-lookup"><span data-stu-id="cf80d-130">OpenGL</span></span>](../opengl/introduction-to-opengl.md)
</dt> <dt>

[<span data-ttu-id="cf80d-131">Multimedia di Windows</span><span class="sxs-lookup"><span data-stu-id="cf80d-131">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> <dt>

[<span data-ttu-id="cf80d-132">GDI Windows</span><span class="sxs-lookup"><span data-stu-id="cf80d-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> </dl>

 

 