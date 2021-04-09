---
description: In questa sezione viene descritto come utilizzare l'API documento XPS per eseguire attività di programmazione.
ms.assetid: 05b3d7b6-7628-4a5f-87b7-9d51ead51c79
title: Uso dell'API Document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8870c64bfa8fe478fb71174703c82a96e3723c53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968340"
---
# <a name="using-xps-document-api"></a><span data-ttu-id="f2081-103">Uso dell'API Document XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-103">Using XPS Document API</span></span>

<span data-ttu-id="f2081-104">In questa sezione viene descritto come utilizzare l' [API documento XPS](documents-xps.md) per eseguire attività di programmazione.</span><span class="sxs-lookup"><span data-stu-id="f2081-104">This section describes how to use the [XPS Document API](documents-xps.md) to perform programming tasks.</span></span>

<span data-ttu-id="f2081-105">Per esempi relativi all'uso dell' [API Document XPS](documents-xps.md) in un programma, vedere la sezione [attività di programmazione dell'API documento XPS](#xps-document-api-programming-tasks) .</span><span class="sxs-lookup"><span data-stu-id="f2081-105">For examples of how to use the [XPS Document API](documents-xps.md) in a program, see the [XPS Document API Programming Tasks](#xps-document-api-programming-tasks) section.</span></span>

<span data-ttu-id="f2081-106">Per informazioni sull'utilizzo del modello a oggetti XPS e su come viene implementato dall' [API Document XPS](documents-xps.md), vedere [informazioni sull'API documenti XPS](about-xps-document-api.md).</span><span class="sxs-lookup"><span data-stu-id="f2081-106">For information about how to use the XPS Object Model and how it is implemented by the [XPS Document API](documents-xps.md), see [About XPS Document API](about-xps-document-api.md).</span></span>

## <a name="getting-started-with-the-xps-document-api"></a><span data-ttu-id="f2081-107">Introduzione con l'API Document XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-107">Getting Started with the XPS Document API</span></span>

<span data-ttu-id="f2081-108">Prima di iniziare a usare l'API Document XPS, assicurarsi di avere familiarità con gli argomenti di programmazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2081-108">Before you start using the XPS Document API, make sure that you are familiar with the following programming topics:</span></span><dl>

[<span data-ttu-id="f2081-109">Programmazione COM</span><span class="sxs-lookup"><span data-stu-id="f2081-109">COM Programming</span></span>](/windows/desktop/com/component-object-model--com--portal)  
[<span data-ttu-id="f2081-110">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="f2081-110">Error Handling in COM</span></span>](/windows/desktop/com/error-handling-in-com)  
</dl>

<span data-ttu-id="f2081-111">Quando si utilizza l'API documenti XPS, è possibile utilizzare anche le tecnologie seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2081-111">When using the XPS Document API, you might also want to use the following technologies:</span></span><dl>

[<span data-ttu-id="f2081-112">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="f2081-112">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)  
[<span data-ttu-id="f2081-113">API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-113">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)  
[<span data-ttu-id="f2081-114">API di firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-114">XPS Digital Signature API</span></span>](xps-digital-signatures.md)  
</dl>

## <a name="xps-document-api-programming-tasks"></a><span data-ttu-id="f2081-115">Attività di programmazione dell'API documento XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-115">XPS Document API Programming Tasks</span></span>

<span data-ttu-id="f2081-116">Negli argomenti di questa sezione viene descritto come utilizzare l' [API documento XPS](documents-xps.md) in un programma e viene illustrato come eseguire alcune attività di programmazione comuni.</span><span class="sxs-lookup"><span data-stu-id="f2081-116">The topics in this section describe how to use the [XPS Document API](documents-xps.md) in a program and demonstrate how to perform some common programming tasks.</span></span>

<span data-ttu-id="f2081-117">L'API Document XPS usa le raccolte per lavorare con gruppi di interfacce.</span><span class="sxs-lookup"><span data-stu-id="f2081-117">The XPS Document API uses collections to work with groups of interfaces.</span></span> <span data-ttu-id="f2081-118">L' [uso delle interfacce di raccolta XPS om](working-with-xps-object-model-collection-interfaces.md) descrive come programmare con queste raccolte.</span><span class="sxs-lookup"><span data-stu-id="f2081-118">[Working with XPS OM Collection Interfaces](working-with-xps-object-model-collection-interfaces.md) describes how to program with these collections.</span></span>

<span data-ttu-id="f2081-119">Le [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md) includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f2081-119">The [Common XPS Document Programming Tasks](common-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="f2081-120">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-120">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="f2081-121">Creazione di un OM XPS vuoto</span><span class="sxs-lookup"><span data-stu-id="f2081-121">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="f2081-122">Leggere un documento XPS in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-122">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="f2081-123">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="f2081-123">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="f2081-124">Scrivere testo in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-124">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="f2081-125">Creare grafica in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-125">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="f2081-126">Inserire immagini in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-126">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="f2081-127">Scrivere un OM XPS in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-127">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="f2081-128">Stampare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-128">Print an XPS OM</span></span>](print-an-xps-om.md)  
  
</dl>

<span data-ttu-id="f2081-129">Le [attività avanzate di programmazione dei documenti XPS](advanced-xps-document-tasks.md) includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f2081-129">The [Advanced XPS Document Programming Tasks](advanced-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="f2081-130">Unisci documenti XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-130">Merge XPS Documents</span></span>](merging-xps-documents.md)  
[<span data-ttu-id="f2081-131">Elaborazione di documenti XPS in un filtro XPSDrv</span><span class="sxs-lookup"><span data-stu-id="f2081-131">Processing XPS Documents in an XPSDrv Filter</span></span>](processing-xps-documents-in-an-xpsdrv-filter.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="f2081-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2081-132">Related topics</span></span>

<dl> <span data-ttu-id="f2081-133"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f2081-133"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f2081-134">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="f2081-134">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="f2081-135">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="f2081-135">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
