---
title: Visualizza scriptFile
description: L'attributo scriptFile specifica i nomi file dei file JScript associati.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- Visualizza Media Player Windows scriptFile
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330886"
---
# <a name="viewscriptfile"></a><span data-ttu-id="51b17-104">Visualizza scriptFile</span><span class="sxs-lookup"><span data-stu-id="51b17-104">VIEW.scriptFile</span></span>

<span data-ttu-id="51b17-105">L'attributo **scriptFile** specifica i nomi file dei file JScript associati.</span><span class="sxs-lookup"><span data-stu-id="51b17-105">The **scriptFile** attribute specifies the file names of accompanying JScript files.</span></span>

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a><span data-ttu-id="51b17-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="51b17-106">Possible Values</span></span>

<span data-ttu-id="51b17-107">Questo attributo è una **stringa** di sola scrittura senza valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="51b17-107">This attribute is a write-only **String** with no default value.</span></span> <span data-ttu-id="51b17-108">I nomi file di più file JScript sono delimitati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="51b17-108">The file names of multiple JScript files are delimited with semicolons.</span></span> <span data-ttu-id="51b17-109">Gli spazi iniziali e successivi e i punti e virgola non devono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="51b17-109">Leading and following spaces and semicolons should not be present.</span></span>

## <a name="remarks"></a><span data-ttu-id="51b17-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="51b17-110">Remarks</span></span>

<span data-ttu-id="51b17-111">Il codice nei file specificati può essere utilizzato da qualsiasi gestore eventi nella vista.</span><span class="sxs-lookup"><span data-stu-id="51b17-111">The code in the specified files can be used by any event handler in the View.</span></span> <span data-ttu-id="51b17-112">Il codice usato dai gestori eventi in più visualizzazioni può essere inserito in un file con lo stesso nome del file di definizione dell'interfaccia, ma con un'estensione js anziché un'estensione WMS.</span><span class="sxs-lookup"><span data-stu-id="51b17-112">Code that is used by event handlers in multiple Views can be placed in a file with the same name as the skin definition file but with a .js extension instead of a .wms extension.</span></span> <span data-ttu-id="51b17-113">Questo file viene caricato automaticamente e non deve essere specificato nel file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="51b17-113">This file is loaded automatically and need not be specified in the skin definition file.</span></span>

## <a name="examples"></a><span data-ttu-id="51b17-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="51b17-114">Examples</span></span>


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a><span data-ttu-id="51b17-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51b17-115">Requirements</span></span>



| <span data-ttu-id="51b17-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="51b17-116">Requirement</span></span> | <span data-ttu-id="51b17-117">Valore</span><span class="sxs-lookup"><span data-stu-id="51b17-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="51b17-118">Versione</span><span class="sxs-lookup"><span data-stu-id="51b17-118">Version</span></span><br/> | <span data-ttu-id="51b17-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="51b17-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51b17-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51b17-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b17-121">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="51b17-121">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





