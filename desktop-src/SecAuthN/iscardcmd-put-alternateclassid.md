---
description: Specifica un nuovo identificatore di classe alternativo nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: 'ISCardCmd: metodo:p ut_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307237"
---
# <a name="iscardcmdput_alternateclassid-method"></a><span data-ttu-id="972df-103">ISCardCmd::p UT \_ AlternateClassId metodo</span><span class="sxs-lookup"><span data-stu-id="972df-103">ISCardCmd::put\_AlternateClassId method</span></span>

<span data-ttu-id="972df-104">\[Il metodo **put \_ AlternateClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="972df-104">\[The **put\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="972df-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="972df-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="972df-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="972df-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="972df-107">Il metodo **put \_ AlternateClassId** specifica un nuovo identificatore di classe alternativo nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="972df-107">The **put\_AlternateClassId** method specifies a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="972df-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="972df-108">Syntax</span></span>


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="972df-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="972df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="972df-110">*byClass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="972df-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="972df-111">Identificatore di classe alternativo.</span><span class="sxs-lookup"><span data-stu-id="972df-111">Alternate class identifier.</span></span> <span data-ttu-id="972df-112">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="972df-112">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="972df-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="972df-113">Return value</span></span>

<span data-ttu-id="972df-114">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="972df-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="972df-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="972df-115">Return code</span></span>                                                                                  | <span data-ttu-id="972df-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="972df-116">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="972df-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="972df-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="972df-118">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="972df-118">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="972df-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="972df-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="972df-120">Il parametro *byClass* non è valido.</span><span class="sxs-lookup"><span data-stu-id="972df-120">The *byClass* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="972df-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="972df-121">Remarks</span></span>

<span data-ttu-id="972df-122">Con le comunicazioni che usano il [*protocollo T = 0*](../secgloss/t-gly.md), i comandi della scheda aggiuntivi possono essere generati automaticamente da APDU e inviati all'unità dati del protocollo di trasmissione (TPDU).</span><span class="sxs-lookup"><span data-stu-id="972df-122">With communications using the [*T=0 protocol*](../secgloss/t-gly.md), additional card commands can be automatically generated by the APDU and sent to the transmission protocol data unit (TPDU).</span></span> <span data-ttu-id="972df-123">I comandi aggiuntivi usano in genere lo stesso ID di classe del comando originale. la specifica di un nuovo ID di classe per mezzo di questo metodo consente ai comandi generati automaticamente di usare il nuovo ID di classe.</span><span class="sxs-lookup"><span data-stu-id="972df-123">The additional commands typically use the same class ID as the original command; specifying a new class ID by means of this method allows automatically generated commands to use the new class ID.</span></span>

## <a name="examples"></a><span data-ttu-id="972df-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="972df-124">Examples</span></span>

<span data-ttu-id="972df-125">Nell'esempio seguente viene illustrato come impostare un nuovo identificatore di classe alternativo nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="972df-125">The following example shows how to set a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="972df-126">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="972df-126">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="972df-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="972df-127">Requirements</span></span>



| <span data-ttu-id="972df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="972df-128">Requirement</span></span> | <span data-ttu-id="972df-129">Valore</span><span class="sxs-lookup"><span data-stu-id="972df-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="972df-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="972df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="972df-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="972df-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="972df-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="972df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="972df-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="972df-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="972df-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="972df-134">End of client support</span></span><br/>    | <span data-ttu-id="972df-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="972df-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="972df-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="972df-136">End of server support</span></span><br/>    | <span data-ttu-id="972df-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="972df-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="972df-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="972df-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="972df-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="972df-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="972df-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="972df-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="972df-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="972df-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="972df-142">DLL</span><span class="sxs-lookup"><span data-stu-id="972df-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="972df-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="972df-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="972df-144">IID</span><span class="sxs-lookup"><span data-stu-id="972df-144">IID</span></span><br/>                      | <span data-ttu-id="972df-145">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="972df-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="972df-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="972df-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972df-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="972df-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="972df-148">**ottenere \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="972df-148">**get\_AlternateClassId**</span></span>](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
