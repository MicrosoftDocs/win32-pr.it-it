---
title: Metodi di proprietà IADsDomain (IADs. h)
description: I metodi dell'interfaccia IADsDomain leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsDomain ADSI
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964664"
---
# <a name="iadsdomain-property-methods"></a><span data-ttu-id="32a3d-105">Metodi di proprietà IADsDomain</span><span class="sxs-lookup"><span data-stu-id="32a3d-105">IADsDomain Property Methods</span></span>

<span data-ttu-id="32a3d-106">I metodi dell'interfaccia [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) leggono e scrivono le proprietà descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="32a3d-106">The [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="32a3d-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="32a3d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="32a3d-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32a3d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="32a3d-109">**AutoUnlockInterval**</span><span class="sxs-lookup"><span data-stu-id="32a3d-109">**AutoUnlockInterval**</span></span>
<span data-ttu-id="32a3d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-111">Indica il tempo minimo che deve trascorrere prima che l'account venga riabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="32a3d-111">Indicates the minimum time that must elapse before the account is automatically reenabled.</span></span>

<dt>

<span data-ttu-id="32a3d-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-114">**Gruppo di lavoro**</span><span class="sxs-lookup"><span data-stu-id="32a3d-114">**IsWorkgroup**</span></span>
<span data-ttu-id="32a3d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-116">Questa proprietà non è più implementata.</span><span class="sxs-lookup"><span data-stu-id="32a3d-116">This property is no longer implemented.</span></span>

<dt>

<span data-ttu-id="32a3d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32a3d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-118">Tipo di dati di scripting: **\_ bool Variant**</span><span class="sxs-lookup"><span data-stu-id="32a3d-118">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-119">**LockoutObservationInterval**</span><span class="sxs-lookup"><span data-stu-id="32a3d-119">**LockoutObservationInterval**</span></span>
<span data-ttu-id="32a3d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-121">Indica l'intervallo di tempo durante il quale il conteggio delle password non valide viene monitorato e accumulato prima di determinare se è necessario bloccare l'account. Se, ad esempio, il numero di tentativi di password non validi per un account supera la soglia (numero massimo di password non valide consentite) durante il periodo di tempo specificato (intervallo di osservazione del blocco), l'account verrà bloccato impostando la proprietà appropriata nel set di proprietà del parametro login.</span><span class="sxs-lookup"><span data-stu-id="32a3d-121">Indicates the time window during which the bad password count is monitored and accumulated before determining whether the account needs to be locked out. For example, if the number of bad password attempts on an account exceed the threshold (Maximum Bad Passwords Allowed) during the specified time period (Lockout Observation Interval) the account will be locked out by setting the appropriate property in the Login Parameter property set.</span></span>

<dt>

<span data-ttu-id="32a3d-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-123">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-124">**MaxBadPasswordsAllowed**</span><span class="sxs-lookup"><span data-stu-id="32a3d-124">**MaxBadPasswordsAllowed**</span></span>
<span data-ttu-id="32a3d-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-126">Indica il numero massimo di accessi con password errati consentiti prima del blocco di un account.</span><span class="sxs-lookup"><span data-stu-id="32a3d-126">Indicates the maximum number of bad password logins allowed before an account lockout.</span></span>

<dt>

<span data-ttu-id="32a3d-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-128">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-129">**MaxPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="32a3d-129">**MaxPasswordAge**</span></span>
<span data-ttu-id="32a3d-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-131">Indica l'intervallo di tempo massimo, in secondi, dopo il quale la password deve essere modificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="32a3d-131">Indicates the maximum time interval, in seconds, after which the password must be changed by the user.</span></span>

<dt>

<span data-ttu-id="32a3d-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-133">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-134">**MinPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="32a3d-134">**MinPasswordAge**</span></span>
<span data-ttu-id="32a3d-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-136">Indica l'intervallo di tempo minimo, in secondi, prima che la password possa essere modificata.</span><span class="sxs-lookup"><span data-stu-id="32a3d-136">Indicates the minimum time interval, in seconds, before the password can be changed.</span></span>

<dt>

<span data-ttu-id="32a3d-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-138">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-139">**MinPasswordLength**</span><span class="sxs-lookup"><span data-stu-id="32a3d-139">**MinPasswordLength**</span></span>
<span data-ttu-id="32a3d-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-141">Indica il numero minimo di caratteri che deve essere utilizzato per una password.</span><span class="sxs-lookup"><span data-stu-id="32a3d-141">Indicates the minimum number of characters that must be used for a password.</span></span>

<dt>

<span data-ttu-id="32a3d-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-143">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-143">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-144">**PasswordAttributes**</span><span class="sxs-lookup"><span data-stu-id="32a3d-144">**PasswordAttributes**</span></span>
<span data-ttu-id="32a3d-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-146">Indica le restrizioni relative alle password, come definito dall'elenco di attributi e valori seguente.</span><span class="sxs-lookup"><span data-stu-id="32a3d-146">Indicates restrictions on passwords, as defined by the following list of attributes and values.</span></span>

> [!Note]  
> <span data-ttu-id="32a3d-147">Per \_ la password attr \_ Complex, la password deve includere almeno un segno di punteggiatura o un carattere non stampabile.</span><span class="sxs-lookup"><span data-stu-id="32a3d-147">For PASSWORD\_ATTR\_COMPLEX, the password must include at least one punctuation mark or non-printable character.</span></span>

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

<span data-ttu-id="32a3d-148">**Password \_ di ATTR \_ None** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="32a3d-148">**PASSWORD\_ATTR\_NONE** (0x00000000)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

<span data-ttu-id="32a3d-149">**Password \_ di \_ \_ Caso misto attr** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="32a3d-149">**PASSWORD\_ATTR\_MIXED\_CASE** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

<span data-ttu-id="32a3d-150">**Password \_ di \_Complesso attr** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="32a3d-150">**PASSWORD\_ATTR\_COMPLEX** (0x00000002)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="32a3d-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-152">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-152">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="32a3d-153">**PasswordHistoryLength**</span><span class="sxs-lookup"><span data-stu-id="32a3d-153">**PasswordHistoryLength**</span></span>
<span data-ttu-id="32a3d-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32a3d-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="32a3d-155">Indica il numero di password precedenti salvate nell'elenco della cronologia.</span><span class="sxs-lookup"><span data-stu-id="32a3d-155">Indicates the number of previous passwords saved in the history list.</span></span> <span data-ttu-id="32a3d-156">L'utente non può riutilizzare una password nell'elenco della cronologia.</span><span class="sxs-lookup"><span data-stu-id="32a3d-156">The user cannot reuse a password in the history list.</span></span>

<dt>

<span data-ttu-id="32a3d-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32a3d-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32a3d-158">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32a3d-158">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="32a3d-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="32a3d-159">Examples</span></span>

<span data-ttu-id="32a3d-160">Nell'esempio di codice seguente viene visualizzato il valore della proprietà **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="32a3d-160">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



<span data-ttu-id="32a3d-161">Nell'esempio di codice seguente viene visualizzato il valore della proprietà **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="32a3d-161">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a><span data-ttu-id="32a3d-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32a3d-162">Requirements</span></span>



| <span data-ttu-id="32a3d-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a3d-163">Requirement</span></span> | <span data-ttu-id="32a3d-164">Valore</span><span class="sxs-lookup"><span data-stu-id="32a3d-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32a3d-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32a3d-165">Minimum supported client</span></span><br/> | <span data-ttu-id="32a3d-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32a3d-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32a3d-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32a3d-167">Minimum supported server</span></span><br/> | <span data-ttu-id="32a3d-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32a3d-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32a3d-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32a3d-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="32a3d-170"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="32a3d-170"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="32a3d-171">DLL</span><span class="sxs-lookup"><span data-stu-id="32a3d-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32a3d-172"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32a3d-172"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="32a3d-173">IID</span><span class="sxs-lookup"><span data-stu-id="32a3d-173">IID</span></span><br/>                      | <span data-ttu-id="32a3d-174">IID \_ IADsDomain è definito come 00E4C220-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="32a3d-174">IID\_IADsDomain is defined as 00E4C220-FD16-11CE-ABC4-02608C9E7553</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="32a3d-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32a3d-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a3d-176">**IADsDomain**</span><span class="sxs-lookup"><span data-stu-id="32a3d-176">**IADsDomain**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[<span data-ttu-id="32a3d-177">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="32a3d-177">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





