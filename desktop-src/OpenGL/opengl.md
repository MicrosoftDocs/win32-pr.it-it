---
title: OpenGL
description: Come interfaccia software per l'hardware grafico, OpenGL esegue il rendering di oggetti multidimensionali in un framebuffer.
ms.assetid: ddd7c8d0-f1d1-4d16-bd0c-99cee3d733c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bec69473f937d4dfff9c496d291e8070ffadef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474046"
---
# <a name="opengl"></a><span data-ttu-id="8d0bc-103">OpenGL</span><span class="sxs-lookup"><span data-stu-id="8d0bc-103">OpenGL</span></span>

## <a name="purpose"></a><span data-ttu-id="8d0bc-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="8d0bc-104">Purpose</span></span>

<span data-ttu-id="8d0bc-105">Come interfaccia software per l'hardware grafico, OpenGL esegue il rendering di oggetti multidimensionali in un framebuffer.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-105">As a software interface for graphics hardware, OpenGL renders multidimensional objects into a framebuffer.</span></span> <span data-ttu-id="8d0bc-106">L'implementazione Microsoft di OpenGL per il sistema operativo Windows è un software grafico standard del settore che consente ai programmatori di creare immagini a colori tridimensionali ancora e animate.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-106">The Microsoft implementation of OpenGL for the Windows operating system is industry-standard graphics software with which programmers can create high-quality still and animated three-dimensional color images.</span></span> <span data-ttu-id="8d0bc-107">La versione di OpenGL descritta in questa sezione è 1,1.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-107">The version of OpenGL described in this section is 1.1.</span></span>

<span data-ttu-id="8d0bc-108">Per informazioni su OpenGL ES in esecuzione in Windows, vedere [angolo per Windows Store](https://github.com/microsoft/angle/wiki).</span><span class="sxs-lookup"><span data-stu-id="8d0bc-108">For information about OpenGL ES running on Windows, see [ANGLE for Windows Store](https://github.com/microsoft/angle/wiki).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8d0bc-109">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="8d0bc-109">Where applicable</span></span>

<span data-ttu-id="8d0bc-110">OpenGL è progettato per la compatibilità tra l'hardware e i sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-110">OpenGL is built for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="8d0bc-111">Questa architettura consente di trasferire facilmente i programmi OpenGL da un sistema a un altro.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-111">This architecture makes it easy to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="8d0bc-112">Sebbene ogni sistema operativo abbia requisiti specifici, il codice OpenGL in molti programmi può essere usato così com'è.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-112">While each operating system has unique requirements, the OpenGL code in many programs can be used as is.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8d0bc-113">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="8d0bc-113">Developer audience</span></span>

<span data-ttu-id="8d0bc-114">Progettato per l'uso da parte dei programmatori C/C++, OpenGL richiede una certa familiarità con l'interfaccia utente grafica di Windows e con l'architettura basata su messaggi.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-114">Designed for use by C/C++ programmers, OpenGL requires familiarity with the Windows graphical user interface as well as message-driven architecture.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8d0bc-115">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="8d0bc-115">Run-time requirements</span></span>

<span data-ttu-id="8d0bc-116">Per ulteriori informazioni sui sistemi operativi necessari per una particolare funzione, vedere la sezione requisiti della documentazione relativa alla funzione.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-116">For more information on which operating systems are required for a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8d0bc-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8d0bc-117">In this section</span></span>



| <span data-ttu-id="8d0bc-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="8d0bc-118">Topic</span></span>                                             | <span data-ttu-id="8d0bc-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d0bc-119">Description</span></span>                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d0bc-120">Overview</span><span class="sxs-lookup"><span data-stu-id="8d0bc-120">Overview</span></span>](basic-opengl-operation.md)<br/> | <span data-ttu-id="8d0bc-121">Informazioni generali sul funzionamento di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-121">General information about how OpenGL works.</span></span><br/>                             |
| [<span data-ttu-id="8d0bc-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8d0bc-122">Reference</span></span>](opengl-reference.md)<br/>      | <span data-ttu-id="8d0bc-123">Documentazione di funzioni, strutture e altri elementi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-123">Documentation of functions, structures, and other programming elements.</span></span><br/> |
| [<span data-ttu-id="8d0bc-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="8d0bc-124">Samples</span></span>](a-porting-sample.md)<br/>        | <span data-ttu-id="8d0bc-125">Esempi di codice OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8d0bc-125">Examples of OpenGL code.</span></span><br/>                                                |



 

## <a name="related-topics"></a><span data-ttu-id="8d0bc-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d0bc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d0bc-127">Grafica e giochi DirectX</span><span class="sxs-lookup"><span data-stu-id="8d0bc-127">DirectX Graphics and Gaming</span></span>](/windows/desktop/directx)
</dt> <dt>

<span data-ttu-id="8d0bc-128">[Immagine ancora](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d0bc-128">[Still Image](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8d0bc-129">[Sistema di colori Windows (WCS)](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d0bc-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8d0bc-130">GDI Windows</span><span class="sxs-lookup"><span data-stu-id="8d0bc-130">Windows GDI</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> <dt>

[<span data-ttu-id="8d0bc-131">Acquisizione di immagini Windows</span><span class="sxs-lookup"><span data-stu-id="8d0bc-131">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="8d0bc-132">Multimedia di Windows</span><span class="sxs-lookup"><span data-stu-id="8d0bc-132">Windows Multimedia</span></span>](/windows/desktop/Multimedia/windows-multimedia-start-page)
</dt> <dt>

<span data-ttu-id="8d0bc-133">[API Windows](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d0bc-133">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>
</dt> </dl>

 

