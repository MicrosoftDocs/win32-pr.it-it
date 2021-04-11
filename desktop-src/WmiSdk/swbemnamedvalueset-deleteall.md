---
description: Il metodo DeleteAll dell'oggetto SWbemNamedValueSet rimuove tutti i valori denominati dalla raccolta, quindi li svuota.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet. DeleteAll (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232020"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a><span data-ttu-id="0d239-103">SWbemNamedValueSet. DeleteAll, metodo</span><span class="sxs-lookup"><span data-stu-id="0d239-103">SWbemNamedValueSet.DeleteAll method</span></span>

<span data-ttu-id="0d239-104">Il metodo **DeleteAll** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) rimuove tutti i valori denominati dalla raccolta, quindi li svuota.</span><span class="sxs-lookup"><span data-stu-id="0d239-104">The **DeleteAll** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object removes all named values from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d239-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d239-105">Syntax</span></span>


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="0d239-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d239-106">Parameters</span></span>

<span data-ttu-id="0d239-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0d239-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d239-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d239-108">Return value</span></span>

<span data-ttu-id="0d239-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0d239-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d239-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0d239-110">Error codes</span></span>

<span data-ttu-id="0d239-111">Al termine del metodo **DeleteAll** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0d239-111">Upon completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="0d239-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0d239-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0d239-113">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0d239-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d239-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d239-114">Requirements</span></span>



| <span data-ttu-id="0d239-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d239-115">Requirement</span></span> | <span data-ttu-id="0d239-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0d239-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d239-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d239-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d239-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d239-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d239-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d239-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d239-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d239-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d239-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d239-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d239-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d239-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d239-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0d239-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d239-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d239-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d239-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d239-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d239-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d239-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d239-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="0d239-127">CLSID</span></span><br/>                    | <span data-ttu-id="0d239-128">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="0d239-128">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="0d239-129">IID</span><span class="sxs-lookup"><span data-stu-id="0d239-129">IID</span></span><br/>                      | <span data-ttu-id="0d239-130">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="0d239-130">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="0d239-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d239-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d239-132">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="0d239-132">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> <dt>

[<span data-ttu-id="0d239-133">**SWbemNamedValueSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="0d239-133">**SWbemNamedValueSet.Remove**</span></span>](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




