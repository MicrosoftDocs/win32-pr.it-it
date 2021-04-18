---
description: Il metodo DeleteAll dell'oggetto SWbemPrivilegeSet rimuove tutti i privilegi dalla raccolta, quindi li svuota.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: Metodo SWbemPrivilegeSet. DeleteAll (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316982"
---
# <a name="swbemprivilegesetdeleteall-method"></a><span data-ttu-id="0a05b-103">SWbemPrivilegeSet. DeleteAll, metodo</span><span class="sxs-lookup"><span data-stu-id="0a05b-103">SWbemPrivilegeSet.DeleteAll method</span></span>

<span data-ttu-id="0a05b-104">Il metodo **DeleteAll** dell'oggetto [**SWbemPrivilegeSet**](swbemprivilegeset.md) rimuove tutti i privilegi dalla raccolta, quindi li svuota.</span><span class="sxs-lookup"><span data-stu-id="0a05b-104">The **DeleteAll** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object removes all privileges from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a05b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a05b-105">Syntax</span></span>


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="0a05b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a05b-106">Parameters</span></span>

<span data-ttu-id="0a05b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0a05b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a05b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a05b-108">Return value</span></span>

<span data-ttu-id="0a05b-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0a05b-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a05b-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0a05b-110">Error codes</span></span>

<span data-ttu-id="0a05b-111">Al termine del metodo **DeleteAll** , l'oggetto **Err** può contenere il codice di errore riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0a05b-111">Upon the completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="0a05b-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0a05b-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0a05b-113">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0a05b-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a05b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a05b-114">Requirements</span></span>



| <span data-ttu-id="0a05b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a05b-115">Requirement</span></span> | <span data-ttu-id="0a05b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0a05b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a05b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a05b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a05b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a05b-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a05b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a05b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a05b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a05b-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a05b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a05b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a05b-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a05b-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a05b-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0a05b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a05b-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0a05b-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0a05b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0a05b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a05b-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a05b-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a05b-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="0a05b-127">CLSID</span></span><br/>                    | <span data-ttu-id="0a05b-128">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="0a05b-128">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="0a05b-129">IID</span><span class="sxs-lookup"><span data-stu-id="0a05b-129">IID</span></span><br/>                      | <span data-ttu-id="0a05b-130">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="0a05b-130">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="0a05b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a05b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a05b-132">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="0a05b-132">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="0a05b-133">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="0a05b-133">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="0a05b-134">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="0a05b-134">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




