---
description: Il metodo GetCurrentDir restituisce un percorso assoluto alla directory attualmente selezionata.
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: 'Metodo ISCardFileAccess:: GetCurrentDir'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: a779dca10a94250bf4b500585b8b50238b0267dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234011"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a><span data-ttu-id="0f347-103">Metodo ISCardFileAccess:: GetCurrentDir</span><span class="sxs-lookup"><span data-stu-id="0f347-103">ISCardFileAccess::GetCurrentDir method</span></span>

<span data-ttu-id="0f347-104">\[Il metodo **GetCurrentDir** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="0f347-104">\[The **GetCurrentDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0f347-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0f347-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0f347-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0f347-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0f347-107">Il metodo **GetCurrentDir** restituisce un percorso assoluto alla directory attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="0f347-107">The **GetCurrentDir** method returns an absolute path to the currently selected directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f347-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f347-108">Syntax</span></span>


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a><span data-ttu-id="0f347-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f347-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f347-110">*pbstrPathSpec* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0f347-110">*pbstrPathSpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f347-111">Puntatore a un BSTR che conterrà il percorso.</span><span class="sxs-lookup"><span data-stu-id="0f347-111">Pointer to a BSTR that will contain the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f347-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f347-112">Return value</span></span>

<span data-ttu-id="0f347-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="0f347-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0f347-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0f347-114">Return code</span></span>                                                                                   | <span data-ttu-id="0f347-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f347-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0f347-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f347-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0f347-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="0f347-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0f347-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0f347-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0f347-119">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="0f347-119">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0f347-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0f347-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0f347-121">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="0f347-121">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0f347-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0f347-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0f347-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0f347-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0f347-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f347-124">Remarks</span></span>

<span data-ttu-id="0f347-125">Per modificare la directory corrente, chiamare [**ChangeDir**](iscardfileaccess-changedir.md).</span><span class="sxs-lookup"><span data-stu-id="0f347-125">To change the current directory, call [**ChangeDir**](iscardfileaccess-changedir.md).</span></span>

<span data-ttu-id="0f347-126">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="0f347-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="0f347-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0f347-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0f347-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0f347-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f347-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f347-129">Requirements</span></span>



| <span data-ttu-id="0f347-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f347-130">Requirement</span></span> | <span data-ttu-id="0f347-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0f347-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f347-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f347-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0f347-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0f347-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0f347-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f347-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0f347-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f347-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0f347-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0f347-136">End of client support</span></span><br/>    | <span data-ttu-id="0f347-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f347-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0f347-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0f347-138">End of server support</span></span><br/>    | <span data-ttu-id="0f347-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f347-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0f347-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f347-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f347-141">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="0f347-141">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)
</dt> <dt>

[<span data-ttu-id="0f347-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="0f347-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
