---
description: Specifica un file WSDL da elaborare per le informazioni sul contratto.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcb96e063a289e16d5e459b59cb8808a763618a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380735"
---
# <a name="wsdl-element"></a><span data-ttu-id="4db1b-103">elemento wsdl</span><span class="sxs-lookup"><span data-stu-id="4db1b-103">wsdl element</span></span>

<span data-ttu-id="4db1b-104">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="4db1b-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="4db1b-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4db1b-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="4db1b-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="4db1b-106">Attributes</span></span>

<span data-ttu-id="4db1b-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="4db1b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4db1b-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4db1b-108">Child elements</span></span>



| <span data-ttu-id="4db1b-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4db1b-109">Element</span></span>                                           | <span data-ttu-id="4db1b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4db1b-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4db1b-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="4db1b-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="4db1b-112">Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un \<wsdl:import> elemento in un file WSDL.</span><span class="sxs-lookup"><span data-stu-id="4db1b-112">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="4db1b-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="4db1b-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="4db1b-114">Specifica il percorso di download per una \<wsdl:import> direttiva che non specifica in modo esplicito un percorso.</span><span class="sxs-lookup"><span data-stu-id="4db1b-114">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="4db1b-115">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="4db1b-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="4db1b-116">File e percorso del file di input WSDL.</span><span class="sxs-lookup"><span data-stu-id="4db1b-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="4db1b-117">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4db1b-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="4db1b-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="4db1b-118">Parent elements</span></span>



| <span data-ttu-id="4db1b-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="4db1b-119">Element</span></span>                                     | <span data-ttu-id="4db1b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4db1b-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="4db1b-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="4db1b-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="4db1b-122">Elemento radice di un file script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="4db1b-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4db1b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4db1b-123">Remarks</span></span>

<span data-ttu-id="4db1b-124">Tutti [**gli elementi importHint**](importhint.md) [**o excludeImport**](excludeimport.md) visualizzati dopo [**l'elemento path**](path.md) in un file di configurazione XML verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="4db1b-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="4db1b-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4db1b-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4db1b-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4db1b-126">Minimum supported system</span></span><br/> | <span data-ttu-id="4db1b-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4db1b-127">Windows Vista</span></span> |
| <span data-ttu-id="4db1b-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="4db1b-128">Can be empty</span></span>                        | <span data-ttu-id="4db1b-129">No</span><span class="sxs-lookup"><span data-stu-id="4db1b-129">No</span></span>            |



 

 




