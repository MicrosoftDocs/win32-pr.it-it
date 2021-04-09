---
description: 'Impedisce la generazione di istruzioni Import per destinazioni specificate denominate in un <elemento WSDL: Import> in un file WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880642"
---
# <a name="excludeimport-element"></a><span data-ttu-id="f6ab1-103">elemento excludeImport</span><span class="sxs-lookup"><span data-stu-id="f6ab1-103">excludeImport element</span></span>

<span data-ttu-id="f6ab1-104">Impedisce la generazione di istruzioni Import per destinazioni specificate denominate in un <elemento WSDL: Import> in un file WSDL.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-104">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="f6ab1-105">Questa operazione può essere utilizzata per impedire a WsdCodeGen di importare destinazioni note, ad esempio le specifiche WS-Addressing e WS-Eventing, anche se in WSDL viene fatto riferimento a tali destinazioni.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="f6ab1-106">Il valore di questo elemento deve essere impostato sullo spazio dei nomi denominato nell'elemento <WSDL: Import> da escludere.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-106">The value of this element must be set to the namespace named in the <wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="f6ab1-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f6ab1-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="f6ab1-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="f6ab1-108">Attributes</span></span>

<span data-ttu-id="f6ab1-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f6ab1-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f6ab1-110">Child elements</span></span>

<span data-ttu-id="f6ab1-111">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f6ab1-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f6ab1-112">Parent elements</span></span>



| <span data-ttu-id="f6ab1-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6ab1-113">Element</span></span>                         | <span data-ttu-id="f6ab1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6ab1-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f6ab1-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="f6ab1-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="f6ab1-116">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="f6ab1-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="f6ab1-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f6ab1-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f6ab1-118">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6ab1-118">Minimum supported system</span></span><br/> | <span data-ttu-id="f6ab1-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6ab1-119">Windows Vista</span></span> |
| <span data-ttu-id="f6ab1-120">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f6ab1-120">Can be empty</span></span>                        | <span data-ttu-id="f6ab1-121">Sì</span><span class="sxs-lookup"><span data-stu-id="f6ab1-121">Yes</span></span>           |



 

 




