---
description: Confronta due stringhe Unicode per determinare se una stringa è un prefisso dell'altro.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Funzione RtlPrefixUnicodeString (ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483133"
---
# <a name="rtlprefixunicodestring-function"></a><span data-ttu-id="31fb8-103">RtlPrefixUnicodeString (funzione)</span><span class="sxs-lookup"><span data-stu-id="31fb8-103">RtlPrefixUnicodeString function</span></span>

<span data-ttu-id="31fb8-104">Confronta due stringhe Unicode per determinare se una stringa è un prefisso dell'altro.</span><span class="sxs-lookup"><span data-stu-id="31fb8-104">Compares two Unicode strings to determine whether one string is a prefix of the other.</span></span>

## <a name="syntax"></a><span data-ttu-id="31fb8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31fb8-105">Syntax</span></span>


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="31fb8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="31fb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31fb8-107">*String1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31fb8-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31fb8-108">Puntatore alla prima stringa, che può essere un prefisso della stringa Unicode memorizzata nel buffer in *string2*.</span><span class="sxs-lookup"><span data-stu-id="31fb8-108">Pointer to the first string, which might be a prefix of the buffered Unicode string at *String2*.</span></span>

</dd> <dt>

<span data-ttu-id="31fb8-109">*String2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31fb8-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31fb8-110">Puntatore alla seconda stringa.</span><span class="sxs-lookup"><span data-stu-id="31fb8-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="31fb8-111">*CaseInSensitive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31fb8-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31fb8-112">Se **true**, la distinzione tra maiuscole e minuscole deve essere ignorata durante il confronto.</span><span class="sxs-lookup"><span data-stu-id="31fb8-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31fb8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31fb8-113">Return value</span></span>

<span data-ttu-id="31fb8-114">**True** se *String1* è un prefisso di *string2*.</span><span class="sxs-lookup"><span data-stu-id="31fb8-114">**TRUE** if *String1* is a prefix of *String2*.</span></span>

## <a name="requirements"></a><span data-ttu-id="31fb8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31fb8-115">Requirements</span></span>



| <span data-ttu-id="31fb8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="31fb8-116">Requirement</span></span> | <span data-ttu-id="31fb8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="31fb8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31fb8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31fb8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31fb8-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="31fb8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="31fb8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31fb8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31fb8-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="31fb8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="31fb8-122">Piattaforma di destinazione</span><span class="sxs-lookup"><span data-stu-id="31fb8-122">Target platform</span></span><br/>          | <dl> <span data-ttu-id="31fb8-123"><dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="31fb8-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="31fb8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31fb8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="31fb8-125"><dt>Ntddk. h (include ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31fb8-125"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="31fb8-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="31fb8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="31fb8-127"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31fb8-127"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="31fb8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="31fb8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31fb8-129"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31fb8-129"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="31fb8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31fb8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fb8-131">**RtlCompareUnicodeString**</span><span class="sxs-lookup"><span data-stu-id="31fb8-131">**RtlCompareUnicodeString**</span></span>](rtlcompareunicodestring.md)
</dt> </dl>

 

 




