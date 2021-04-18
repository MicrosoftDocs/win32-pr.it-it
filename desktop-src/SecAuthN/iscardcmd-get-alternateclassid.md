---
description: Recupera il valore dell'ID della classe alternativa.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Metodo ISCardCmd:: get_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317063"
---
# <a name="iscardcmdget_alternateclassid-method"></a><span data-ttu-id="11fd4-103">Metodo ISCardCmd:: Get \_ AlternateClassId</span><span class="sxs-lookup"><span data-stu-id="11fd4-103">ISCardCmd::get\_AlternateClassId method</span></span>

<span data-ttu-id="11fd4-104">\[Il metodo **get \_ AlternateClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="11fd4-104">\[The **get\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="11fd4-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="11fd4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="11fd4-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="11fd4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="11fd4-107">Il metodo **get \_ AlternateClassId** Recupera il valore dell'ID di classe alternativo.</span><span class="sxs-lookup"><span data-stu-id="11fd4-107">The **get\_AlternateClassId** method retrieves the value of the alternate class ID.</span></span> <span data-ttu-id="11fd4-108">Questo metodo avrà esito negativo a meno che l'ID alternativo non sia stato impostato da una chiamata precedente a [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="11fd4-108">This method will fail unless the alternate ID has been set by a previous call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="11fd4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11fd4-109">Syntax</span></span>


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="11fd4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="11fd4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fd4-111">*pbyClass* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11fd4-111">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11fd4-112">Puntatore al byte che contiene il valore dell'ID di classe alternativo al ritorno.</span><span class="sxs-lookup"><span data-stu-id="11fd4-112">Pointer to the byte that contains the alternate class ID value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fd4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11fd4-113">Return value</span></span>

<span data-ttu-id="11fd4-114">Il metodo restituisce i valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="11fd4-114">The method returns the following possible values.</span></span>



| <span data-ttu-id="11fd4-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="11fd4-115">Return code</span></span>                                                                                    | <span data-ttu-id="11fd4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11fd4-116">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11fd4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11fd4-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="11fd4-118">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="11fd4-118">Operation was completed successfully.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="11fd4-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="11fd4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="11fd4-120">Il parametro *pbyClass* non è valido.</span><span class="sxs-lookup"><span data-stu-id="11fd4-120">The *pbyClass* parameter is not valid.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="11fd4-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="11fd4-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="11fd4-122">L'ID di classe alternativo non è stato impostato in precedenza da una chiamata a [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="11fd4-122">The alternate class ID has not been previously set by a call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11fd4-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="11fd4-123">Remarks</span></span>

<span data-ttu-id="11fd4-124">Questo metodo si applica alle comunicazioni che utilizzano il [*protocollo T = 0*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="11fd4-124">This method applies to communications using the [*T=0 protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="11fd4-125">Per altre informazioni, vedere [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="11fd4-125">For more information, see [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="examples"></a><span data-ttu-id="11fd4-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="11fd4-126">Examples</span></span>

<span data-ttu-id="11fd4-127">Nell'esempio seguente viene illustrato come recuperare l'ID della classe alternativa.</span><span class="sxs-lookup"><span data-stu-id="11fd4-127">The following example shows how to retrieve the alternate class ID.</span></span> <span data-ttu-id="11fd4-128">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="11fd4-128">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="11fd4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11fd4-129">Requirements</span></span>



| <span data-ttu-id="11fd4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="11fd4-130">Requirement</span></span> | <span data-ttu-id="11fd4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="11fd4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11fd4-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11fd4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="11fd4-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="11fd4-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="11fd4-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11fd4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="11fd4-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="11fd4-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11fd4-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="11fd4-136">End of client support</span></span><br/>    | <span data-ttu-id="11fd4-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="11fd4-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="11fd4-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="11fd4-138">End of server support</span></span><br/>    | <span data-ttu-id="11fd4-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11fd4-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="11fd4-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11fd4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="11fd4-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="11fd4-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="11fd4-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="11fd4-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="11fd4-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="11fd4-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="11fd4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="11fd4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11fd4-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11fd4-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="11fd4-146">IID</span><span class="sxs-lookup"><span data-stu-id="11fd4-146">IID</span></span><br/>                      | <span data-ttu-id="11fd4-147">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="11fd4-147">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="11fd4-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11fd4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11fd4-149">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="11fd4-149">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="11fd4-150">**Inserisci \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="11fd4-150">**put\_AlternateClassId**</span></span>](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
