---
description: Richiede una verifica dell'utente.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Metodo ISCardVerify:: Verify'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311616"
---
# <a name="iscardverifyverify-method"></a><span data-ttu-id="d50ca-103">Metodo ISCardVerify:: Verify</span><span class="sxs-lookup"><span data-stu-id="d50ca-103">ISCardVerify::Verify method</span></span>

<span data-ttu-id="d50ca-104">\[Il metodo **Verify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d50ca-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d50ca-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d50ca-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d50ca-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d50ca-107">Il metodo **Verify** richiede una verifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d50ca-107">The **Verify** method requests a verification of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="d50ca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d50ca-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="d50ca-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d50ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d50ca-110">*PCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-110">*pCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-111">Contiene il codice da presentare alla [*Smart Card*](../secgloss/s-gly.md) nel processo di verifica del titolare della scheda (CHV).</span><span class="sxs-lookup"><span data-stu-id="d50ca-111">Contains the code to be presented to the [*smart card*](../secgloss/s-gly.md) in the CHV (card holder verification) process.</span></span>

</dd> <dt>

<span data-ttu-id="d50ca-112">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-113">Indica se il codice è globale o locale.</span><span class="sxs-lookup"><span data-stu-id="d50ca-113">Indicates whether the code is global or local.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="d50ca-114">**SC \_ FL \_ IHV \_ globale**</span><span class="sxs-lookup"><span data-stu-id="d50ca-114">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="d50ca-115">**SC \_ FL \_ IHV \_ locale**</span><span class="sxs-lookup"><span data-stu-id="d50ca-115">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="d50ca-116">*lRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-116">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d50ca-117">Riferimento specifico per smart card.</span><span class="sxs-lookup"><span data-stu-id="d50ca-117">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d50ca-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d50ca-118">Return value</span></span>

<span data-ttu-id="d50ca-119">Il metodo **Verify** restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d50ca-119">The **Verify** method returns one of the following values:</span></span>



| <span data-ttu-id="d50ca-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d50ca-120">Return code</span></span>                                                                                   | <span data-ttu-id="d50ca-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d50ca-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d50ca-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d50ca-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d50ca-123">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d50ca-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d50ca-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d50ca-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d50ca-125">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="d50ca-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="d50ca-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d50ca-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d50ca-127">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="d50ca-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="d50ca-128"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d50ca-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d50ca-129">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d50ca-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d50ca-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="d50ca-130">Remarks</span></span>

<span data-ttu-id="d50ca-131">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="d50ca-131">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="d50ca-132">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d50ca-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d50ca-133">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d50ca-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d50ca-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d50ca-134">Requirements</span></span>



| <span data-ttu-id="d50ca-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50ca-135">Requirement</span></span> | <span data-ttu-id="d50ca-136">Valore</span><span class="sxs-lookup"><span data-stu-id="d50ca-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d50ca-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d50ca-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d50ca-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d50ca-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d50ca-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d50ca-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d50ca-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d50ca-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d50ca-141">End of client support</span></span><br/>    | <span data-ttu-id="d50ca-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d50ca-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d50ca-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d50ca-143">End of server support</span></span><br/>    | <span data-ttu-id="d50ca-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d50ca-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d50ca-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d50ca-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50ca-146">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="d50ca-146">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
