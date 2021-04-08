---
description: Confronta due stringhe Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Funzione RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877701"
---
# <a name="rtlcompareunicodestring-function"></a><span data-ttu-id="e07f0-103">RtlCompareUnicodeString (funzione)</span><span class="sxs-lookup"><span data-stu-id="e07f0-103">RtlCompareUnicodeString function</span></span>

<span data-ttu-id="e07f0-104">Confronta due stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="e07f0-104">Compares two Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e07f0-105">Syntax</span></span>


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="e07f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e07f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07f0-107">*String1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e07f0-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07f0-108">Puntatore alla prima stringa.</span><span class="sxs-lookup"><span data-stu-id="e07f0-108">Pointer to the first string.</span></span>

</dd> <dt>

<span data-ttu-id="e07f0-109">*String2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e07f0-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07f0-110">Puntatore alla seconda stringa.</span><span class="sxs-lookup"><span data-stu-id="e07f0-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="e07f0-111">*CaseInSensitive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e07f0-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07f0-112">Se **true**, la distinzione tra maiuscole e minuscole deve essere ignorata durante il confronto.</span><span class="sxs-lookup"><span data-stu-id="e07f0-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07f0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e07f0-113">Return value</span></span>

<span data-ttu-id="e07f0-114">Valore con segno che fornisce i risultati del confronto:</span><span class="sxs-lookup"><span data-stu-id="e07f0-114">A signed value that gives the results of the comparison:</span></span>



| <span data-ttu-id="e07f0-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e07f0-115">Return code</span></span>                                                                               | <span data-ttu-id="e07f0-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e07f0-116">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e07f0-117"><dt>**Zero**</dt></span><span class="sxs-lookup"><span data-stu-id="e07f0-117"><dt>**Zero**</dt></span></span> </dl>       | <span data-ttu-id="e07f0-118">*String1* è uguale a *string2*.</span><span class="sxs-lookup"><span data-stu-id="e07f0-118">*String1* equals *String2*.</span></span><br/>          |
| <dl> <span data-ttu-id="e07f0-119"><dt>**< zero**</dt></span><span class="sxs-lookup"><span data-stu-id="e07f0-119"><dt>**< Zero**</dt></span></span> </dl>  | <span data-ttu-id="e07f0-120">*String1* è minore di *string2*.</span><span class="sxs-lookup"><span data-stu-id="e07f0-120">*String1* is less than *String2*.</span></span><br/>    |
| <dl> <span data-ttu-id="e07f0-121"><dt>**> zero**</dt></span><span class="sxs-lookup"><span data-stu-id="e07f0-121"><dt>**> Zero** </dt></span></span> </dl> | <span data-ttu-id="e07f0-122">*String1* è maggiore di *string2*.</span><span class="sxs-lookup"><span data-stu-id="e07f0-122">*String1* is greater than *String2*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e07f0-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e07f0-123">Requirements</span></span>



| <span data-ttu-id="e07f0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07f0-124">Requirement</span></span> | <span data-ttu-id="e07f0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e07f0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07f0-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07f0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e07f0-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e07f0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="e07f0-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07f0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e07f0-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e07f0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="e07f0-130">Piattaforma di destinazione</span><span class="sxs-lookup"><span data-stu-id="e07f0-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="e07f0-131"><dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="e07f0-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="e07f0-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e07f0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e07f0-133"><dt>WDM. h (include WDM. h, ntddk. h o Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e07f0-133"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="e07f0-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="e07f0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e07f0-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e07f0-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e07f0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e07f0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e07f0-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e07f0-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="e07f0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e07f0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07f0-139">**RtlCompareString**</span><span class="sxs-lookup"><span data-stu-id="e07f0-139">**RtlCompareString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[<span data-ttu-id="e07f0-140">**RtlEqualString**</span><span class="sxs-lookup"><span data-stu-id="e07f0-140">**RtlEqualString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
