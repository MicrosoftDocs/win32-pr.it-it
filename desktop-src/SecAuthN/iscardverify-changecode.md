---
description: Sostituisce il codice CHV (verifica del contenitore di schede) corrente con il nuovo codice CHV.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'Metodo ISCardVerify:: ChangeCode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757019"
---
# <a name="iscardverifychangecode-method"></a><span data-ttu-id="dd16b-103">Metodo ISCardVerify:: ChangeCode</span><span class="sxs-lookup"><span data-stu-id="dd16b-103">ISCardVerify::ChangeCode method</span></span>

<span data-ttu-id="dd16b-104">\[Il metodo **ChangeCode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="dd16b-104">\[The **ChangeCode** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd16b-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dd16b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd16b-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="dd16b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dd16b-107">Il metodo **ChangeCode** sostituisce il codice CHV corrente (verifica del contenitore di schede) con il nuovo codice CHV.</span><span class="sxs-lookup"><span data-stu-id="dd16b-107">The **ChangeCode** method replaces the current CHV (card holder verification) code with new CHV code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd16b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd16b-108">Syntax</span></span>


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="dd16b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd16b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd16b-110">*pOldCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd16b-110">*pOldCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd16b-111">Puntatore a un [**IByteBuffer**](ibytebuffer.md) contenente il codice corrente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dd16b-111">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the user's current code.</span></span>

</dd> <dt>

<span data-ttu-id="dd16b-112">*pNewCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd16b-112">*pNewCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd16b-113">Puntatore a un [**IByteBuffer**](ibytebuffer.md) contenente il nuovo codice che verrà presentato alla [*Smart Card*](../secgloss/s-gly.md) durante il processo di modifica per autenticare l'utente.</span><span class="sxs-lookup"><span data-stu-id="dd16b-113">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the new code that will be presented to the [*smart card*](../secgloss/s-gly.md) during the change process to authenticate the user.</span></span>

</dd> <dt>

<span data-ttu-id="dd16b-114">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd16b-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd16b-115">Indica se il codice è globale o locale e se il codice deve essere abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="dd16b-115">Indicates whether the code is global or local, and whether the code should be enabled or disabled.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="dd16b-116">**SC \_ FL \_ IHV \_ globale**</span><span class="sxs-lookup"><span data-stu-id="dd16b-116">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="dd16b-117">**SC \_ FL \_ IHV \_ locale**</span><span class="sxs-lookup"><span data-stu-id="dd16b-117">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

<span data-ttu-id="dd16b-118">**\_ \_ Abilitazione SC FL IHV \_**</span><span class="sxs-lookup"><span data-stu-id="dd16b-118">**SC\_FL\_IHV\_ENABLE**</span></span>
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

<span data-ttu-id="dd16b-119">**SC \_ FL \_ IHV \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="dd16b-119">**SC\_FL\_IHV\_DISABLE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="dd16b-120">*lRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd16b-120">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd16b-121">Riferimento specifico per smart card.</span><span class="sxs-lookup"><span data-stu-id="dd16b-121">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd16b-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd16b-122">Return value</span></span>

<span data-ttu-id="dd16b-123">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd16b-123">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="dd16b-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dd16b-124">Return code</span></span>                                                                                   | <span data-ttu-id="dd16b-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd16b-125">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dd16b-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd16b-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dd16b-127">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="dd16b-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="dd16b-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dd16b-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dd16b-129">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="dd16b-129">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="dd16b-130"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd16b-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dd16b-131">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="dd16b-131">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="dd16b-132"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="dd16b-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dd16b-133">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="dd16b-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="dd16b-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd16b-134">Remarks</span></span>

<span data-ttu-id="dd16b-135">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="dd16b-135">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="dd16b-136">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="dd16b-136">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dd16b-137">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dd16b-137">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd16b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd16b-138">Requirements</span></span>



| <span data-ttu-id="dd16b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd16b-139">Requirement</span></span> | <span data-ttu-id="dd16b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="dd16b-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd16b-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd16b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="dd16b-142">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd16b-142">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="dd16b-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd16b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="dd16b-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd16b-144">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dd16b-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="dd16b-145">End of client support</span></span><br/>    | <span data-ttu-id="dd16b-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd16b-146">Windows XP</span></span><br/>                                |
| <span data-ttu-id="dd16b-147">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="dd16b-147">End of server support</span></span><br/>    | <span data-ttu-id="dd16b-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd16b-148">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="dd16b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd16b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd16b-150">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="dd16b-150">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> <dt>

[<span data-ttu-id="dd16b-151">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="dd16b-151">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

[<span data-ttu-id="dd16b-152">Valori restituiti da Smart Card</span><span class="sxs-lookup"><span data-stu-id="dd16b-152">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
