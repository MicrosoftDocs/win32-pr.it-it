---
description: La tabella ComPlus contiene le informazioni necessarie per installare le applicazioni COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabella ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318294"
---
# <a name="complus-table"></a><span data-ttu-id="430fe-103">Tabella ComPlus</span><span class="sxs-lookup"><span data-stu-id="430fe-103">Complus Table</span></span>

<span data-ttu-id="430fe-104">La tabella ComPlus contiene le informazioni necessarie per installare le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="430fe-104">The Complus table contains information needed to install COM+ applications.</span></span>

<span data-ttu-id="430fe-105">La tabella ComPlus include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="430fe-105">The Complus table has the following columns.</span></span>



| <span data-ttu-id="430fe-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="430fe-106">Column</span></span>      | <span data-ttu-id="430fe-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="430fe-107">Type</span></span>                         | <span data-ttu-id="430fe-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="430fe-108">Key</span></span> | <span data-ttu-id="430fe-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="430fe-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="430fe-110">Componente\_</span><span class="sxs-lookup"><span data-stu-id="430fe-110">Component\_</span></span> | [<span data-ttu-id="430fe-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="430fe-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="430fe-112">S</span><span class="sxs-lookup"><span data-stu-id="430fe-112">Y</span></span>   | <span data-ttu-id="430fe-113">N</span><span class="sxs-lookup"><span data-stu-id="430fe-113">N</span></span>        |
| <span data-ttu-id="430fe-114">ExpType</span><span class="sxs-lookup"><span data-stu-id="430fe-114">ExpType</span></span>     | [<span data-ttu-id="430fe-115">Integer</span><span class="sxs-lookup"><span data-stu-id="430fe-115">Integer</span></span>](integer.md)       | <span data-ttu-id="430fe-116">N</span><span class="sxs-lookup"><span data-stu-id="430fe-116">N</span></span>   | <span data-ttu-id="430fe-117">S</span><span class="sxs-lookup"><span data-stu-id="430fe-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="430fe-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="430fe-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="430fe-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="430fe-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="430fe-120">Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="430fe-120">An external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="430fe-121">Si tratta del componente che contiene l'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="430fe-121">This is the component that contains the COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="430fe-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span><span class="sxs-lookup"><span data-stu-id="430fe-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span></span>
</dt> <dd>

<span data-ttu-id="430fe-123">Flag di esportazione utilizzati durante la generazione del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="430fe-123">Export flags used during the generation of the .msi file.</span></span> <span data-ttu-id="430fe-124">Per ulteriori informazioni, vedere la documentazione COM+ in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="430fe-124">For more information see the COM+ documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="430fe-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="430fe-125">Remarks</span></span>

<span data-ttu-id="430fe-126">Vedere l'azione [RegisterComPlus](registercomplus-action.md) e l' [azione UnregisterComPlus](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="430fe-126">See the [RegisterComPlus action](registercomplus-action.md) and [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

<span data-ttu-id="430fe-127">Vedere [installazione di un'applicazione com+ con la Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="430fe-127">See [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span></span>

## <a name="validation"></a><span data-ttu-id="430fe-128">Convalida</span><span class="sxs-lookup"><span data-stu-id="430fe-128">Validation</span></span>

<dl>

[<span data-ttu-id="430fe-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="430fe-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="430fe-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="430fe-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="430fe-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="430fe-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="430fe-132">ICE66</span><span class="sxs-lookup"><span data-stu-id="430fe-132">ICE66</span></span>](ice66.md)  
</dl>

 

 



