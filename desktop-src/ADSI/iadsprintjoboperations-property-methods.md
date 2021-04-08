---
title: Metodi di proprietà IADsPrintJobOperations (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsPrintJobOperations leggono e scrivono le proprietà elencate nella tabella seguente. Per ulteriori informazioni sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPrintJobOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874241"
---
# <a name="iadsprintjoboperations-property-methods"></a><span data-ttu-id="9839e-105">Metodi di proprietà IADsPrintJobOperations</span><span class="sxs-lookup"><span data-stu-id="9839e-105">IADsPrintJobOperations Property Methods</span></span>

<span data-ttu-id="9839e-106">I metodi di proprietà dell'interfaccia [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) leggono e scrivono le proprietà elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9839e-106">The property methods of the [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) interface read and write the properties listed in the following table.</span></span> <span data-ttu-id="9839e-107">Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9839e-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9839e-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9839e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9839e-109">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="9839e-109">**PagesPrinted**</span></span>
<span data-ttu-id="9839e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9839e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="9839e-111">Contiene il numero di pagine stampate.</span><span class="sxs-lookup"><span data-stu-id="9839e-111">Contains the number of pages printed.</span></span>

<dt>

<span data-ttu-id="9839e-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9839e-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9839e-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="9839e-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9839e-114">**Position**</span><span class="sxs-lookup"><span data-stu-id="9839e-114">**Position**</span></span>
<span data-ttu-id="9839e-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9839e-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="9839e-116">Contiene la posizione del processo di stampa nella coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="9839e-116">Contains the position of this print job in the print queue.</span></span>

<dt>

<span data-ttu-id="9839e-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9839e-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9839e-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="9839e-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9839e-119">**Status**</span><span class="sxs-lookup"><span data-stu-id="9839e-119">**Status**</span></span>
<span data-ttu-id="9839e-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9839e-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="9839e-121">Contiene lo stato corrente del processo di stampa come indicato da uno dei valori delle [**costanti di stato del processo di stampa ADSI**](adsi-print-job-status-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="9839e-121">Contains the current status of the print job as indicated by one of the [**ADSI Print Job Status Constants**](adsi-print-job-status-constants.md) values.</span></span>

<dt>

<span data-ttu-id="9839e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9839e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9839e-123">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="9839e-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="9839e-124">**TimeElapsed**</span><span class="sxs-lookup"><span data-stu-id="9839e-124">**TimeElapsed**</span></span>
<span data-ttu-id="9839e-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9839e-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="9839e-126">Contiene il numero di millisecondi trascorsi dall'avvio del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="9839e-126">Contains the number of milliseconds elapsed since the print job started.</span></span>

<dt>

<span data-ttu-id="9839e-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9839e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9839e-128">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="9839e-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="9839e-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="9839e-129">Examples</span></span>

<span data-ttu-id="9839e-130">Nell'esempio di codice riportato di seguito viene illustrato come è possibile utilizzare le proprietà per [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) .</span><span class="sxs-lookup"><span data-stu-id="9839e-130">The following code example shows how the properties for [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) may be used.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a><span data-ttu-id="9839e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9839e-131">Requirements</span></span>



| <span data-ttu-id="9839e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9839e-132">Requirement</span></span> | <span data-ttu-id="9839e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9839e-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9839e-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9839e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9839e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9839e-135">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="9839e-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9839e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9839e-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9839e-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9839e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9839e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9839e-139"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9839e-139"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="9839e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9839e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9839e-141"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9839e-141"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="9839e-142">IID</span><span class="sxs-lookup"><span data-stu-id="9839e-142">IID</span></span><br/>                      | <span data-ttu-id="9839e-143">IID \_ IADsPrintJobOperations è definito come 32FB6780-1ED0-11CF-a988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="9839e-143">IID\_IADsPrintJobOperations is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9839e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9839e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9839e-145">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="9839e-145">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="9839e-146">**IADsPrintJobOperations**</span><span class="sxs-lookup"><span data-stu-id="9839e-146">**IADsPrintJobOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[<span data-ttu-id="9839e-147">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="9839e-147">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="9839e-148">**Costanti di stato del processo di stampa ADSI**</span><span class="sxs-lookup"><span data-stu-id="9839e-148">**ADSI Print Job Status Constants**</span></span>](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





