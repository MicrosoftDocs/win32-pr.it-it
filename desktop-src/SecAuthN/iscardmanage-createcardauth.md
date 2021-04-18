---
description: Crea un'interfaccia ISCardAuth.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'Metodo ISCardManage:: CreateCardAuth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313729"
---
# <a name="iscardmanagecreatecardauth-method"></a><span data-ttu-id="bccfb-103">Metodo ISCardManage:: CreateCardAuth</span><span class="sxs-lookup"><span data-stu-id="bccfb-103">ISCardManage::CreateCardAuth method</span></span>

<span data-ttu-id="bccfb-104">\[Il metodo **CreateCardAuth** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bccfb-104">\[The **CreateCardAuth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bccfb-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bccfb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bccfb-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bccfb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bccfb-107">Il metodo **CreateCardAuth** crea un'interfaccia [**ISCardAuth**](iscardauth.md) .</span><span class="sxs-lookup"><span data-stu-id="bccfb-107">The **CreateCardAuth** method creates an [**ISCardAuth**](iscardauth.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bccfb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bccfb-108">Syntax</span></span>


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a><span data-ttu-id="bccfb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bccfb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bccfb-110">*ppISCardAuth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bccfb-110">*ppISCardAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bccfb-111">Puntatore restituito all'interfaccia creata.</span><span class="sxs-lookup"><span data-stu-id="bccfb-111">Returned pointer to the created interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bccfb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bccfb-112">Return value</span></span>

<span data-ttu-id="bccfb-113">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="bccfb-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="bccfb-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bccfb-114">Return code</span></span>                                                                                   | <span data-ttu-id="bccfb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bccfb-115">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="bccfb-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bccfb-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bccfb-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bccfb-117">Operation completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="bccfb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bccfb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bccfb-119">Il parametro *ppISCardAuth* non è valido.</span><span class="sxs-lookup"><span data-stu-id="bccfb-119">The *ppISCardAuth* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="bccfb-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="bccfb-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bccfb-121">Un puntatore errato è stato passato in *ppISCardAuth*.</span><span class="sxs-lookup"><span data-stu-id="bccfb-121">A bad pointer was passed in *ppISCardAuth*.</span></span><br/> |
| <dl> <span data-ttu-id="bccfb-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="bccfb-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bccfb-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="bccfb-123">Out of memory.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="bccfb-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="bccfb-124">Remarks</span></span>

<span data-ttu-id="bccfb-125">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="bccfb-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="bccfb-126">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bccfb-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bccfb-127">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bccfb-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bccfb-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bccfb-128">Requirements</span></span>



| <span data-ttu-id="bccfb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bccfb-129">Requirement</span></span> | <span data-ttu-id="bccfb-130">Valore</span><span class="sxs-lookup"><span data-stu-id="bccfb-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bccfb-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bccfb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bccfb-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bccfb-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bccfb-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bccfb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bccfb-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bccfb-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bccfb-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bccfb-135">End of client support</span></span><br/>    | <span data-ttu-id="bccfb-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bccfb-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="bccfb-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bccfb-137">End of server support</span></span><br/>    | <span data-ttu-id="bccfb-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bccfb-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="bccfb-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bccfb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bccfb-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="bccfb-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
