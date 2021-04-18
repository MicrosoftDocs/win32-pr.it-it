---
description: Crea un'interfaccia ISCardFileAccess.
ms.assetid: 06a5948f-c7bd-49bf-9032-f40f3d0d330c
title: 'Metodo ISCardManage:: CreateFileAccess'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3eb1f544e05959cc33119091268e1c7fe6266547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317061"
---
# <a name="iscardmanagecreatefileaccess-method"></a><span data-ttu-id="c9f1a-103">Metodo ISCardManage:: CreateFileAccess</span><span class="sxs-lookup"><span data-stu-id="c9f1a-103">ISCardManage::CreateFileAccess method</span></span>

<span data-ttu-id="c9f1a-104">\[Il metodo **CreateFileAccess** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-104">\[The **CreateFileAccess** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c9f1a-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c9f1a-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="c9f1a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c9f1a-107">Il metodo **CreateFileAccess** crea un'interfaccia [**ISCardFileAccess**](iscardfileaccess.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f1a-107">The **CreateFileAccess** method creates an [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f1a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9f1a-108">Syntax</span></span>


```C++
HRESULT CreateFileAccess(
  [out] ISCardFileAccess **ppISCardFileAccess
);
```



## <a name="parameters"></a><span data-ttu-id="c9f1a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9f1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f1a-110">*ppISCardFileAccess* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9f1a-110">*ppISCardFileAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f1a-111">Puntatore restituito all'interfaccia [**ISCardFileAccess**](iscardfileaccess.md) creata.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-111">Returned pointer to the created [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9f1a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9f1a-112">Return value</span></span>

<span data-ttu-id="c9f1a-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c9f1a-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c9f1a-114">Return code</span></span>                                                                                   | <span data-ttu-id="c9f1a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9f1a-115">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="c9f1a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f1a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c9f1a-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-117">Operation completed successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="c9f1a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f1a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c9f1a-119">Il parametro *ppISCardFileAccess* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-119">The *ppISCardFileAccess* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c9f1a-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f1a-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c9f1a-121">Un puntatore errato è stato passato in *ppISCardFileAccess*.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-121">A bad pointer was passed in *ppISCardFileAccess*.</span></span><br/> |
| <dl> <span data-ttu-id="c9f1a-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f1a-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c9f1a-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-123">Out of memory.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="c9f1a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9f1a-124">Remarks</span></span>

<span data-ttu-id="c9f1a-125">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="c9f1a-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="c9f1a-126">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c9f1a-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c9f1a-127">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c9f1a-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f1a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9f1a-128">Requirements</span></span>



| <span data-ttu-id="c9f1a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9f1a-129">Requirement</span></span> | <span data-ttu-id="c9f1a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c9f1a-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9f1a-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9f1a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f1a-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9f1a-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c9f1a-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9f1a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f1a-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9f1a-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c9f1a-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c9f1a-135">End of client support</span></span><br/>    | <span data-ttu-id="c9f1a-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9f1a-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c9f1a-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c9f1a-137">End of server support</span></span><br/>    | <span data-ttu-id="c9f1a-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9f1a-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c9f1a-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9f1a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f1a-140">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="c9f1a-140">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="c9f1a-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="c9f1a-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
