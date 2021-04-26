---
description: Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un elemento wsdl:import in un file WSDL.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: Elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995878"
---
# <a name="excludeimport-element"></a><span data-ttu-id="08b98-103">Elemento excludeImport</span><span class="sxs-lookup"><span data-stu-id="08b98-103">excludeImport element</span></span>

<span data-ttu-id="08b98-104">Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un \<wsdl:import> elemento in un file WSDL.</span><span class="sxs-lookup"><span data-stu-id="08b98-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="08b98-105">Può essere usato per evitare che WsdCodeGen importi destinazioni note, ad esempio le specifiche WS-Addressing e WS-Eventing, anche se si fa riferimento a queste destinazioni nel wsdl.</span><span class="sxs-lookup"><span data-stu-id="08b98-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="08b98-106">Il valore di questo elemento deve essere impostato nello spazio dei nomi denominato \<wsdl:import> nell'elemento da escludere.</span><span class="sxs-lookup"><span data-stu-id="08b98-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="08b98-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="08b98-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="08b98-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="08b98-108">Attributes</span></span>

<span data-ttu-id="08b98-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="08b98-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="08b98-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="08b98-110">Child elements</span></span>

<span data-ttu-id="08b98-111">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="08b98-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="08b98-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="08b98-112">Parent elements</span></span>



| <span data-ttu-id="08b98-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="08b98-113">Element</span></span>                         | <span data-ttu-id="08b98-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08b98-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="08b98-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="08b98-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="08b98-116">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="08b98-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="08b98-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="08b98-117">Element information</span></span>



| <span data-ttu-id="08b98-118">Label</span><span class="sxs-lookup"><span data-stu-id="08b98-118">Label</span></span> | <span data-ttu-id="08b98-119">Valore</span><span class="sxs-lookup"><span data-stu-id="08b98-119">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="08b98-120">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08b98-120">Minimum supported system</span></span><br/> | <span data-ttu-id="08b98-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08b98-121">Windows Vista</span></span> |
| <span data-ttu-id="08b98-122">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="08b98-122">Can be empty</span></span>                        | <span data-ttu-id="08b98-123">Sì</span><span class="sxs-lookup"><span data-stu-id="08b98-123">Yes</span></span>           |



 

 




