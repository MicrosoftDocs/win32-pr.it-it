---
description: Il Metodo SetAsSingleton dell'oggetto SWbemObjectPath impone al percorso di indirizzare un'istanza WMI singleton di una classe. Una classe singleton è una classe che non può mai avere più di un'istanza.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Metodo SWbemObjectPath. SetAsSingleton (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318509"
---
# <a name="swbemobjectpathsetassingleton-method"></a><span data-ttu-id="a5a08-104">SWbemObjectPath. SetAsSingleton, metodo</span><span class="sxs-lookup"><span data-stu-id="a5a08-104">SWbemObjectPath.SetAsSingleton method</span></span>

<span data-ttu-id="a5a08-105">Il metodo **SetAsSingleton** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) impone al percorso di indirizzare un'istanza WMI singleton di una classe.</span><span class="sxs-lookup"><span data-stu-id="a5a08-105">The **SetAsSingleton** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a singleton WMI instance of a class.</span></span> <span data-ttu-id="a5a08-106">Una classe singleton è una classe che non può mai avere più di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a5a08-106">A singleton class is a class that can never have more than one instance.</span></span>

<span data-ttu-id="a5a08-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a5a08-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span> <span data-ttu-id="a5a08-108">SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="a5a08-108">SWbemObjectPath</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a08-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5a08-109">Syntax</span></span>


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a><span data-ttu-id="a5a08-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5a08-110">Parameters</span></span>

<span data-ttu-id="a5a08-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a5a08-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5a08-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5a08-112">Return value</span></span>

<span data-ttu-id="a5a08-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a5a08-113">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5a08-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a5a08-114">Error codes</span></span>

<span data-ttu-id="a5a08-115">Al termine del metodo **SetAsSingleton** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="a5a08-115">Upon completion of the **SetAsSingleton** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="a5a08-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a5a08-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a5a08-117">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a5a08-117">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5a08-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5a08-118">Requirements</span></span>



| <span data-ttu-id="a5a08-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a08-119">Requirement</span></span> | <span data-ttu-id="a5a08-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a5a08-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a08-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5a08-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a08-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5a08-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5a08-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5a08-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a08-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5a08-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5a08-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5a08-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5a08-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5a08-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5a08-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a5a08-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5a08-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5a08-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a5a08-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a5a08-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5a08-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5a08-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a5a08-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="a5a08-131">CLSID</span></span><br/>                    | <span data-ttu-id="a5a08-132">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="a5a08-132">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="a5a08-133">IID</span><span class="sxs-lookup"><span data-stu-id="a5a08-133">IID</span></span><br/>                      | <span data-ttu-id="a5a08-134">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="a5a08-134">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




