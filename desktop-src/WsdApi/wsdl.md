---
description: Specifica un file WSDL da elaborare per le informazioni sul contratto.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento WSDL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231655"
---
# <a name="wsdl-element"></a><span data-ttu-id="f64eb-103">elemento WSDL</span><span class="sxs-lookup"><span data-stu-id="f64eb-103">wsdl element</span></span>

<span data-ttu-id="f64eb-104">Specifica un file WSDL da elaborare per le informazioni sul contratto.</span><span class="sxs-lookup"><span data-stu-id="f64eb-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="f64eb-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f64eb-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="f64eb-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="f64eb-106">Attributes</span></span>

<span data-ttu-id="f64eb-107">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="f64eb-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f64eb-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f64eb-108">Child elements</span></span>



| <span data-ttu-id="f64eb-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f64eb-109">Element</span></span>                                           | <span data-ttu-id="f64eb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f64eb-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f64eb-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="f64eb-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="f64eb-112">Impedisce la generazione di istruzioni Import per destinazioni specificate denominate in un <elemento WSDL: Import> in un file WSDL.</span><span class="sxs-lookup"><span data-stu-id="f64eb-112">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="f64eb-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="f64eb-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="f64eb-114">Specifica il percorso di download per un <WSDL: Import> direttiva che non specifica in modo esplicito una posizione.</span><span class="sxs-lookup"><span data-stu-id="f64eb-114">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="f64eb-115">**percorso**</span><span class="sxs-lookup"><span data-stu-id="f64eb-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="f64eb-116">File e percorso del file di input WSDL.</span><span class="sxs-lookup"><span data-stu-id="f64eb-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="f64eb-117">Sequenza di elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f64eb-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="f64eb-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f64eb-118">Parent elements</span></span>



| <span data-ttu-id="f64eb-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="f64eb-119">Element</span></span>                                     | <span data-ttu-id="f64eb-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f64eb-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f64eb-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="f64eb-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="f64eb-122">Elemento radice di un file di script XML del generatore di codice WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="f64eb-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f64eb-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f64eb-123">Remarks</span></span>

<span data-ttu-id="f64eb-124">Qualsiasi elemento [**importHint**](importhint.md) o [**excludeImport**](excludeimport.md) visualizzato dopo l'elemento [**path**](path.md) in un file di configurazione XML verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f64eb-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="f64eb-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f64eb-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f64eb-126">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f64eb-126">Minimum supported system</span></span><br/> | <span data-ttu-id="f64eb-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f64eb-127">Windows Vista</span></span> |
| <span data-ttu-id="f64eb-128">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f64eb-128">Can be empty</span></span>                        | <span data-ttu-id="f64eb-129">No</span><span class="sxs-lookup"><span data-stu-id="f64eb-129">No</span></span>            |



 

 




