---
description: La proprietà delle impostazioni locali dell'oggetto SWbemObjectPath contiene le impostazioni locali del percorso dell'oggetto.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. locale (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314564"
---
# <a name="swbemobjectpathlocale-property"></a><span data-ttu-id="bfdfd-103">Proprietà SWbemObjectPath. locale</span><span class="sxs-lookup"><span data-stu-id="bfdfd-103">SWbemObjectPath.Locale property</span></span>

<span data-ttu-id="bfdfd-104">La proprietà delle **impostazioni locali** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) contiene le impostazioni locali del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bfdfd-104">The **Locale** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the locale of object path.</span></span>

<span data-ttu-id="bfdfd-105">Quando la proprietà **SWbemObjectPath. locale** fa parte di un oggetto [**SWbemObjectPath**](swbemobjectpath.md) autonomo, è di lettura/scrittura e può essere usata per impostare il componente delle impostazioni locali del moniker.</span><span class="sxs-lookup"><span data-stu-id="bfdfd-105">When the **SWbemObjectPath.Locale** property is part of a standalone [**SWbemObjectPath**](swbemobjectpath.md) object, it is read/write and can be used to set the locale component of the moniker.</span></span>

<span data-ttu-id="bfdfd-106">Quando si accede alla proprietà **SWbemObjectPath. locale** come parte di una proprietà [**SWbemObject. Path \_**](swbemobject-path-.md) , è di sola lettura e restituisce il valore delle impostazioni locali utilizzate nell'associazione allo spazio dei nomi da cui è stato ottenuto l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bfdfd-106">When the **SWbemObjectPath.Locale** property is accessed as part of a [**SWbemObject.Path\_**](swbemobject-path-.md) property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.</span></span>

<span data-ttu-id="bfdfd-107">Per gli identificatori delle impostazioni locali Microsoft, il formato della stringa è "MS \_ xxxx", dove xxxx è una stringa in formato esadecimale che indica il valore LCID.</span><span class="sxs-lookup"><span data-stu-id="bfdfd-107">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="bfdfd-108">Ad esempio, l'identificatore delle impostazioni locali per l'inglese americano è "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="bfdfd-108">For example, the American English locale identifier is "MS\_409".</span></span>

<span data-ttu-id="bfdfd-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bfdfd-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bfdfd-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bfdfd-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfdfd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfdfd-111">Syntax</span></span>


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a><span data-ttu-id="bfdfd-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bfdfd-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="bfdfd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfdfd-113">Requirements</span></span>



| <span data-ttu-id="bfdfd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfdfd-114">Requirement</span></span> | <span data-ttu-id="bfdfd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bfdfd-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdfd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfdfd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bfdfd-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfdfd-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfdfd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfdfd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bfdfd-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfdfd-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfdfd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfdfd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfdfd-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfdfd-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfdfd-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bfdfd-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfdfd-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bfdfd-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bfdfd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bfdfd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfdfd-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfdfd-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfdfd-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="bfdfd-126">CLSID</span></span><br/>                    | <span data-ttu-id="bfdfd-127">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="bfdfd-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="bfdfd-128">IID</span><span class="sxs-lookup"><span data-stu-id="bfdfd-128">IID</span></span><br/>                      | <span data-ttu-id="bfdfd-129">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="bfdfd-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




