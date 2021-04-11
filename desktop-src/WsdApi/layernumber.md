---
description: Definisce il numero del livello di codice da generare.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231815"
---
# <a name="layernumber-element"></a><span data-ttu-id="00117-103">elemento layerNumber</span><span class="sxs-lookup"><span data-stu-id="00117-103">layerNumber element</span></span>

<span data-ttu-id="00117-104">Definisce il numero del livello di codice da generare.</span><span class="sxs-lookup"><span data-stu-id="00117-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="00117-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="00117-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="00117-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="00117-106">Attributes</span></span>

<span data-ttu-id="00117-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="00117-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="00117-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="00117-108">Child elements</span></span>

<span data-ttu-id="00117-109">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="00117-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="00117-110">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="00117-110">Parent elements</span></span>



| <span data-ttu-id="00117-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="00117-111">Element</span></span>                                     | <span data-ttu-id="00117-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00117-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="00117-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="00117-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="00117-114">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="00117-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="00117-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="00117-115">Remarks</span></span>

<span data-ttu-id="00117-116">I numeri di livello vengono usati nelle tabelle di runtime per distinguere un livello di codice per un altro.</span><span class="sxs-lookup"><span data-stu-id="00117-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="00117-117">WSDAPI usa il codice generato con un numero di livello pari a 0.</span><span class="sxs-lookup"><span data-stu-id="00117-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="00117-118">In genere, questo valore sarà 1, a indicare che il codice generato è sovrapposto a WSDAPI e a nessun altro livello.</span><span class="sxs-lookup"><span data-stu-id="00117-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="00117-119">In alcuni casi, è possibile usare numeri più alti.</span><span class="sxs-lookup"><span data-stu-id="00117-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="00117-120">Se, ad esempio, un'azienda produce codice per una classe di dispositivi (livello 1), è possibile che un particolare fornitore di hardware desideri aggiungere un livello aggiuntivo con numero 2.</span><span class="sxs-lookup"><span data-stu-id="00117-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="00117-121">I valori validi, tranne nel caso di WSDAPI, sono maggiori di 0 e minori di 16.</span><span class="sxs-lookup"><span data-stu-id="00117-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="00117-122">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="00117-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="00117-123">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00117-123">Minimum supported system</span></span><br/> | <span data-ttu-id="00117-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00117-124">Windows Vista</span></span> |
| <span data-ttu-id="00117-125">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="00117-125">Can be empty</span></span>                        | <span data-ttu-id="00117-126">Sì</span><span class="sxs-lookup"><span data-stu-id="00117-126">Yes</span></span>           |



 

 




