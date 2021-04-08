---
title: Tipi di dati semplici ADSI (IADs. h)
description: Active Directory Service Interfaces (ADSI) definisce e utilizza i tipi di dati semplici seguenti.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048002"
---
# <a name="adsi-simple-data-types"></a><span data-ttu-id="e5d1f-114">Tipi di dati semplici ADSI</span><span class="sxs-lookup"><span data-stu-id="e5d1f-114">ADSI Simple Data Types</span></span>

<span data-ttu-id="e5d1f-115">Active Directory Service Interfaces (ADSI) definisce e utilizza i tipi di dati semplici seguenti.</span><span class="sxs-lookup"><span data-stu-id="e5d1f-115">Active Directory Service Interfaces (ADSI) defines and uses the following simple data types.</span></span>


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

<span data-ttu-id="e5d1f-116">**\_valore booleano ADS**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-116">**ADS\_BOOLEAN**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-117">DWORD</span><span class="sxs-lookup"><span data-stu-id="e5d1f-117">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-118">**\_ \_ stringa esatta del case Ads \_**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-118">**ADS\_CASE\_EXACT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-119">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e5d1f-119">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-120">**caso ADS, \_ \_ Ignora \_ stringa**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-120">**ADS\_CASE\_IGNORE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-121">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e5d1f-121">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-122">**\_stringa DN \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-122">**ADS\_DN\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-123">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e5d1f-123">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-124">**\_Integer ADS**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-124">**ADS\_INTEGER**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="e5d1f-125">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-126">**ADS \_ grande \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-126">**ADS\_LARGE\_INTEGER**</span></span>
</dt> <dd>

[<span data-ttu-id="e5d1f-127">**\_Integer grande**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-127">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

<span data-ttu-id="e5d1f-128">**\_stringa numerica Ads \_**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-128">**ADS\_NUMERIC\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-129">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e5d1f-129">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-130">**\_classe di oggetti ADS \_**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-130">**ADS\_OBJECT\_CLASS**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-131">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e5d1f-131">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-132">**\_stringa stampabile \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-132">**ADS\_PRINTABLE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-133">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e5d1f-133">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-134">**\_handle di ricerca Ads \_**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-134">**ADS\_SEARCH\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="e5d1f-135">HANDLE</span><span class="sxs-lookup"><span data-stu-id="e5d1f-135">HANDLE</span></span>

</dd> <dt>

<span data-ttu-id="e5d1f-136">**\_ora UTC \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-136">**ADS\_UTC\_TIME**</span></span>
</dt> <dd>

[<span data-ttu-id="e5d1f-137">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="e5d1f-137">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5d1f-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5d1f-138">Remarks</span></span>

<span data-ttu-id="e5d1f-139">Quando ADSI legge un attributo definito come **Integer** nello schema LDAP, gestisce sempre il valore integer come valore a 32 bit e può troncare i dati.</span><span class="sxs-lookup"><span data-stu-id="e5d1f-139">When ADSI reads an attribute that has been defined as an **INTEGER** in the LDAP schema, it will always handle the integer as a 32-bit value and may truncate the data.</span></span> <span data-ttu-id="e5d1f-140">Si tratta solo di un problema per i server LDAP che consentono valori integer con dimensione arbitraria.</span><span class="sxs-lookup"><span data-stu-id="e5d1f-140">This is only a concern for LDAP servers that allow arbitrary sized integer values.</span></span> <span data-ttu-id="e5d1f-141">Se l'attributo è un attributo personalizzato definito estendendo lo schema, è possibile evitare questo problema definendo l'attributo personalizzato sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="e5d1f-141">If the attribute is a custom attribute defined by extending the schema, this problem can be avoided by defining the custom attribute as a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d1f-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5d1f-142">Requirements</span></span>



| <span data-ttu-id="e5d1f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d1f-143">Requirement</span></span> | <span data-ttu-id="e5d1f-144">Valore</span><span class="sxs-lookup"><span data-stu-id="e5d1f-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e5d1f-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5d1f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d1f-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5d1f-146">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="e5d1f-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5d1f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d1f-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5d1f-148">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="e5d1f-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5d1f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d1f-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d1f-150"><dt>Iads.h</dt></span></span> </dl> |



 

