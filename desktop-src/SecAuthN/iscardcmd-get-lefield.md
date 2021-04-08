---
description: Restituisce il campo le dell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'Metodo ISCardCmd:: get_LeField (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760112"
---
# <a name="iscardcmdget_lefield-method"></a><span data-ttu-id="89a98-103">Metodo ISCardCmd:: Get \_ LeField</span><span class="sxs-lookup"><span data-stu-id="89a98-103">ISCardCmd::get\_LeField method</span></span>

<span data-ttu-id="89a98-104">\[Il metodo **get \_ LeField** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="89a98-104">\[The **get\_LeField** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="89a98-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89a98-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="89a98-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="89a98-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="89a98-107">Il metodo **get \_ LeField** restituisce il campo le dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="89a98-107">The **get\_LeField** method returns the Le field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="89a98-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89a98-108">Syntax</span></span>


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="89a98-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="89a98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89a98-110">*plSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89a98-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89a98-111">Puntatore al valore del campo le per la restituzione.</span><span class="sxs-lookup"><span data-stu-id="89a98-111">Pointer to the Le field value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89a98-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89a98-112">Return value</span></span>

<span data-ttu-id="89a98-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="89a98-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="89a98-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="89a98-114">Return code</span></span>                                                                                  | <span data-ttu-id="89a98-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89a98-115">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="89a98-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89a98-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="89a98-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="89a98-117">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="89a98-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="89a98-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="89a98-119">Il parametro *plSize* non è valido.</span><span class="sxs-lookup"><span data-stu-id="89a98-119">The *plSize* parameter is not valid.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="89a98-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="89a98-120">Examples</span></span>

<span data-ttu-id="89a98-121">Nell'esempio seguente viene illustrato come recuperare il valore del campo le dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="89a98-121">The following example shows how to retrieve the Le field value from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="89a98-122">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="89a98-122">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a><span data-ttu-id="89a98-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89a98-123">Requirements</span></span>



| <span data-ttu-id="89a98-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="89a98-124">Requirement</span></span> | <span data-ttu-id="89a98-125">Valore</span><span class="sxs-lookup"><span data-stu-id="89a98-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89a98-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89a98-126">Minimum supported client</span></span><br/> | <span data-ttu-id="89a98-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="89a98-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="89a98-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89a98-128">Minimum supported server</span></span><br/> | <span data-ttu-id="89a98-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89a98-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89a98-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="89a98-130">End of client support</span></span><br/>    | <span data-ttu-id="89a98-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="89a98-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="89a98-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="89a98-132">End of server support</span></span><br/>    | <span data-ttu-id="89a98-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89a98-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="89a98-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89a98-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="89a98-135"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="89a98-135"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="89a98-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="89a98-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="89a98-137"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="89a98-137"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="89a98-138">DLL</span><span class="sxs-lookup"><span data-stu-id="89a98-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89a98-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a98-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="89a98-140">IID</span><span class="sxs-lookup"><span data-stu-id="89a98-140">IID</span></span><br/>                      | <span data-ttu-id="89a98-141">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="89a98-141">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="89a98-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89a98-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a98-143">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="89a98-143">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
