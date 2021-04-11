---
description: Crea l'interfaccia specificata.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'Metodo ISCardManage:: CreateInterface'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232834"
---
# <a name="iscardmanagecreateinterface-method"></a><span data-ttu-id="83d5b-103">Metodo ISCardManage:: CreateInterface</span><span class="sxs-lookup"><span data-stu-id="83d5b-103">ISCardManage::CreateInterface method</span></span>

<span data-ttu-id="83d5b-104">\[Il metodo **CreateInterface** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="83d5b-104">\[The **CreateInterface** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="83d5b-105">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="83d5b-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="83d5b-106">Il metodo **CreateInterface** crea l'interfaccia specificata.</span><span class="sxs-lookup"><span data-stu-id="83d5b-106">The **CreateInterface** method creates the specified interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d5b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83d5b-107">Syntax</span></span>


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a><span data-ttu-id="83d5b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="83d5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83d5b-109">*pguidInterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83d5b-109">*pguidInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5b-110">Valore GUID dell'interfaccia da creare.</span><span class="sxs-lookup"><span data-stu-id="83d5b-110">The GUID value of the interface to create.</span></span>

</dd> <dt>

<span data-ttu-id="83d5b-111">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83d5b-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5b-112">Nome dell'interfaccia da creare se il GUID non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="83d5b-112">The name of the interface to create if the GUID is unavailable.</span></span> <span data-ttu-id="83d5b-113">I valori standard sono "CryptoProvider".</span><span class="sxs-lookup"><span data-stu-id="83d5b-113">Standard values are "CryptoProvider".</span></span>

</dd> <dt>

<span data-ttu-id="83d5b-114">*pUserData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83d5b-114">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5b-115">Puntatore a dati specifici dell'utente da utilizzare nella creazione di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="83d5b-115">Pointer to user-specific data to use in the creation of an interface.</span></span>

</dd> <dt>

<span data-ttu-id="83d5b-116">*ppInterface* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="83d5b-116">*ppInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5b-117">Puntatore all'interfaccia restituita.</span><span class="sxs-lookup"><span data-stu-id="83d5b-117">Pointer to the returned interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83d5b-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83d5b-118">Return value</span></span>

<span data-ttu-id="83d5b-119">I possibili valori restituiti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="83d5b-119">The possible return values are the following:</span></span>



| <span data-ttu-id="83d5b-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="83d5b-120">Return code</span></span>                                                                                   | <span data-ttu-id="83d5b-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83d5b-121">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83d5b-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83d5b-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="83d5b-123">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="83d5b-123">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="83d5b-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="83d5b-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="83d5b-125">Uno dei parametri specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="83d5b-125">One of the supplied parameters are not valid.</span></span><br/>                                         |
| <dl> <span data-ttu-id="83d5b-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="83d5b-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="83d5b-127">Un puntatore errato è stato passato nel parametro *pguidInterface* o *pUserData* .</span><span class="sxs-lookup"><span data-stu-id="83d5b-127">A bad pointer was passed in either the *pguidInterface* or the *pUserData* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="83d5b-128"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="83d5b-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="83d5b-129">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="83d5b-129">Out of memory.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="83d5b-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="83d5b-130">Remarks</span></span>

<span data-ttu-id="83d5b-131">Per un elenco di tutti i metodi definiti dall'interfaccia [**ISCardManage**](iscardmanage.md) , vedere **ISCardManage**.</span><span class="sxs-lookup"><span data-stu-id="83d5b-131">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see **ISCardManage**.</span></span>

<span data-ttu-id="83d5b-132">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="83d5b-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="83d5b-133">Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="83d5b-133">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83d5b-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83d5b-134">Requirements</span></span>



| <span data-ttu-id="83d5b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="83d5b-135">Requirement</span></span> | <span data-ttu-id="83d5b-136">Valore</span><span class="sxs-lookup"><span data-stu-id="83d5b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83d5b-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83d5b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="83d5b-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="83d5b-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="83d5b-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83d5b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="83d5b-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83d5b-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="83d5b-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="83d5b-141">End of client support</span></span><br/>    | <span data-ttu-id="83d5b-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="83d5b-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="83d5b-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="83d5b-143">End of server support</span></span><br/>    | <span data-ttu-id="83d5b-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="83d5b-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="83d5b-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83d5b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d5b-146">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="83d5b-146">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
