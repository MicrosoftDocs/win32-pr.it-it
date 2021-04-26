---
description: Definisce il numero del livello di codice da generare.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: Elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995488"
---
# <a name="layernumber-element"></a><span data-ttu-id="170ce-103">Elemento layerNumber</span><span class="sxs-lookup"><span data-stu-id="170ce-103">layerNumber element</span></span>

<span data-ttu-id="170ce-104">Definisce il numero del livello di codice da generare.</span><span class="sxs-lookup"><span data-stu-id="170ce-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="170ce-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="170ce-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="170ce-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="170ce-106">Attributes</span></span>

<span data-ttu-id="170ce-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="170ce-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="170ce-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="170ce-108">Child elements</span></span>

<span data-ttu-id="170ce-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="170ce-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="170ce-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="170ce-110">Parent elements</span></span>



| <span data-ttu-id="170ce-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="170ce-111">Element</span></span>                                     | <span data-ttu-id="170ce-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="170ce-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="170ce-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="170ce-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="170ce-114">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="170ce-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="170ce-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="170ce-115">Remarks</span></span>

<span data-ttu-id="170ce-116">I numeri di livello vengono usati nelle tabelle di runtime per distinguere un livello di codice per un altro.</span><span class="sxs-lookup"><span data-stu-id="170ce-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="170ce-117">WSDAPI usa codice generato con un numero di livello 0.</span><span class="sxs-lookup"><span data-stu-id="170ce-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="170ce-118">In genere, questo valore sarà 1, a indicare che il codice generato è a livelli su WSDAPI e nessun altro livello.</span><span class="sxs-lookup"><span data-stu-id="170ce-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="170ce-119">In alcuni casi, è possibile usare numeri più elevati.</span><span class="sxs-lookup"><span data-stu-id="170ce-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="170ce-120">Ad esempio, se una società produce codice per una classe di dispositivo (livello 1 numerato), un fornitore di hardware specifico potrebbe voler aggiungere un ulteriore livello numerato livello 2.</span><span class="sxs-lookup"><span data-stu-id="170ce-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="170ce-121">I valori validi, tranne nel caso di WSDAPI, sono maggiori di 0 e minori di 16.</span><span class="sxs-lookup"><span data-stu-id="170ce-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="170ce-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="170ce-122">Element information</span></span>



| <span data-ttu-id="170ce-123">Label</span><span class="sxs-lookup"><span data-stu-id="170ce-123">Label</span></span> | <span data-ttu-id="170ce-124">Valore</span><span class="sxs-lookup"><span data-stu-id="170ce-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="170ce-125">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="170ce-125">Minimum supported system</span></span><br/> | <span data-ttu-id="170ce-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="170ce-126">Windows Vista</span></span> |
| <span data-ttu-id="170ce-127">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="170ce-127">Can be empty</span></span>                        | <span data-ttu-id="170ce-128">Sì</span><span class="sxs-lookup"><span data-stu-id="170ce-128">Yes</span></span>           |



 

 




