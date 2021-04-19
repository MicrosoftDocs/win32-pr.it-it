---
description: Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un elemento wsdl:import in un file WSDL.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: ExcludeImport - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380775"
---
# <a name="excludeimport-element"></a><span data-ttu-id="cc600-103">ExcludeImport - elemento</span><span class="sxs-lookup"><span data-stu-id="cc600-103">excludeImport element</span></span>

<span data-ttu-id="cc600-104">Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un \<wsdl:import> elemento in un file WSDL.</span><span class="sxs-lookup"><span data-stu-id="cc600-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="cc600-105">Può essere usato per evitare che WsdCodeGen importi destinazioni note, ad esempio le specifiche WS-Addressing e WS-Eventing, anche se si fa riferimento a queste destinazioni nel wsdl.</span><span class="sxs-lookup"><span data-stu-id="cc600-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="cc600-106">Il valore di questo elemento deve essere impostato nello spazio dei nomi denominato \<wsdl:import> nell'elemento da escludere.</span><span class="sxs-lookup"><span data-stu-id="cc600-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="cc600-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="cc600-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="cc600-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="cc600-108">Attributes</span></span>

<span data-ttu-id="cc600-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="cc600-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cc600-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="cc600-110">Child elements</span></span>

<span data-ttu-id="cc600-111">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="cc600-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cc600-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="cc600-112">Parent elements</span></span>



| <span data-ttu-id="cc600-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc600-113">Element</span></span>                         | <span data-ttu-id="cc600-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc600-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="cc600-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="cc600-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="cc600-116">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="cc600-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="cc600-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="cc600-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="cc600-118">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc600-118">Minimum supported system</span></span><br/> | <span data-ttu-id="cc600-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc600-119">Windows Vista</span></span> |
| <span data-ttu-id="cc600-120">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="cc600-120">Can be empty</span></span>                        | <span data-ttu-id="cc600-121">Sì</span><span class="sxs-lookup"><span data-stu-id="cc600-121">Yes</span></span>           |



 

 




