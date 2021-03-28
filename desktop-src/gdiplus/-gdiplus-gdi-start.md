---
description: Windows GDI+ è un'API basata su classi per i programmatori C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129067"
---
# <a name="gdi"></a><span data-ttu-id="6472b-103">GDI+</span><span class="sxs-lookup"><span data-stu-id="6472b-103">GDI+</span></span>

## <a name="purpose"></a><span data-ttu-id="6472b-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="6472b-104">Purpose</span></span>

<span data-ttu-id="6472b-105">Windows GDI+ è un'API basata su classi per i programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="6472b-105">Windows GDI+ is a class-based API for C/C++ programmers.</span></span> <span data-ttu-id="6472b-106">Consente alle applicazioni di utilizzare grafica e testo formattato sia sullo schermo video che sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="6472b-106">It enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="6472b-107">Le applicazioni basate sull'API Microsoft Win32 non accedono direttamente all'hardware grafico.</span><span class="sxs-lookup"><span data-stu-id="6472b-107">Applications based on the Microsoft Win32 API do not access graphics hardware directly.</span></span> <span data-ttu-id="6472b-108">Diversamente, GDI+ interagisce con i driver di dispositivo per conto delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6472b-108">Instead, GDI+ interacts with device drivers on behalf of applications.</span></span> <span data-ttu-id="6472b-109">GDI+ è supportato anche da Win64 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6472b-109">GDI+ is also supported by Microsoft Win64.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6472b-110">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="6472b-110">Where applicable</span></span>

<span data-ttu-id="6472b-111">Le funzioni e le classi GDI+ non sono supportate per l'uso in un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="6472b-111">GDI+ functions and classes are not supported for use within a Windows service.</span></span> <span data-ttu-id="6472b-112">Il tentativo di utilizzare queste funzioni e classi da un servizio Windows può produrre problemi imprevisti, ad esempio le prestazioni del servizio diminuite e gli errori o le eccezioni in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6472b-112">Attempting to use these functions and classes from a Windows service may produce unexpected problems, such as diminished service performance and run-time exceptions or errors.</span></span>

> [!Note]  
> <span data-ttu-id="6472b-113">Quando si usa l'API GDI+, non è mai necessario consentire all'applicazione di scaricare tipi di carattere arbitrari da origini non attendibili.</span><span class="sxs-lookup"><span data-stu-id="6472b-113">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="6472b-114">Il sistema operativo richiede privilegi elevati per assicurarsi che tutti i tipi di carattere installati siano attendibili.</span><span class="sxs-lookup"><span data-stu-id="6472b-114">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6472b-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="6472b-115">Developer audience</span></span>

<span data-ttu-id="6472b-116">L'interfaccia basata su classi C++ GDI+ è progettata per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="6472b-116">The GDI+ C++ class-based interface is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="6472b-117">È necessaria una certa familiarità con l'interfaccia utente grafica di Windows e l'architettura basata su messaggi.</span><span class="sxs-lookup"><span data-stu-id="6472b-117">Familiarity with the Windows graphical user interface and message-driven architecture is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6472b-118">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="6472b-118">Run-time requirements</span></span>

<span data-ttu-id="6472b-119">GDI+ può essere utilizzato in tutte le applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="6472b-119">GDI+ can be used in all Windows-based applications.</span></span> <span data-ttu-id="6472b-120">GDI+ è stato introdotto in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6472b-120">GDI+ was introduced in Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6472b-121">Per informazioni sui sistemi operativi necessari per usare una classe o un metodo specifico, vedere la sezione altre informazioni della documentazione relativa alla classe o al metodo.</span><span class="sxs-lookup"><span data-stu-id="6472b-121">For information about which operating systems are required to use a particular class or method, see the More Information section of the documentation for the class or method.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6472b-122">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6472b-122">In this section</span></span>

| <span data-ttu-id="6472b-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="6472b-123">Topic</span></span>                                                    | <span data-ttu-id="6472b-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6472b-124">Description</span></span>                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="6472b-125">Overview</span><span class="sxs-lookup"><span data-stu-id="6472b-125">Overview</span></span>](-gdiplus-about-gdi--about.md)<br/>     | <span data-ttu-id="6472b-126">Informazioni generali su GDI+.</span><span class="sxs-lookup"><span data-stu-id="6472b-126">General information about GDI+.</span></span><br/>            |
| [<span data-ttu-id="6472b-127">Usando</span><span class="sxs-lookup"><span data-stu-id="6472b-127">Using</span></span>](-gdiplus-using-gdi--use.md)<br/>          | <span data-ttu-id="6472b-128">Attività ed esempi con GDI+.</span><span class="sxs-lookup"><span data-stu-id="6472b-128">Tasks and examples using GDI+.</span></span><br/>             |
| [<span data-ttu-id="6472b-129">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6472b-129">Reference</span></span>](-gdiplus-class-gdi-reference.md)<br/> | <span data-ttu-id="6472b-130">Documentazione dell'API basata su classi di GDI+ C++.</span><span class="sxs-lookup"><span data-stu-id="6472b-130">Documentation of GDI+ C++ class-based API.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="6472b-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6472b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6472b-132">GDI Windows</span><span class="sxs-lookup"><span data-stu-id="6472b-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> <dt>

<span data-ttu-id="6472b-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="6472b-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="6472b-134">Acquisizione di immagini Windows</span><span class="sxs-lookup"><span data-stu-id="6472b-134">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="6472b-135">OpenGL</span><span class="sxs-lookup"><span data-stu-id="6472b-135">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="6472b-136">Multimedia di Windows</span><span class="sxs-lookup"><span data-stu-id="6472b-136">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
