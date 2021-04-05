---
title: Metodi di proprietà IADsADSystemInfo (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsADSystemInfo ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsADSystemInfo ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120762"
---
# <a name="iadsadsysteminfo-property-methods"></a><span data-ttu-id="7331e-105">Metodi di proprietà IADsADSystemInfo</span><span class="sxs-lookup"><span data-stu-id="7331e-105">IADsADSystemInfo Property Methods</span></span>

<span data-ttu-id="7331e-106">I metodi di proprietà dell'interfaccia [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7331e-106">The property methods of the [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="7331e-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="7331e-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7331e-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7331e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7331e-109">**NomeComputer**</span><span class="sxs-lookup"><span data-stu-id="7331e-109">**ComputerName**</span></span>
<span data-ttu-id="7331e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-111">Recupera il nome distinto del computer locale.</span><span class="sxs-lookup"><span data-stu-id="7331e-111">Retrieves the distinguished name of the local computer.</span></span>

<dt>

<span data-ttu-id="7331e-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-114">**DomainDNSName**</span><span class="sxs-lookup"><span data-stu-id="7331e-114">**DomainDNSName**</span></span>
<span data-ttu-id="7331e-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-116">Recupera il nome DNS del dominio del computer locale, ad esempio "domainName.companyName.com".</span><span class="sxs-lookup"><span data-stu-id="7331e-116">Retrieves the DNS name of the local computer's domain, such as "domainName.companyName.com".</span></span>

<dt>

<span data-ttu-id="7331e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-119">**DomainShortName**</span><span class="sxs-lookup"><span data-stu-id="7331e-119">**DomainShortName**</span></span>
<span data-ttu-id="7331e-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-121">Recupera il nome breve del dominio del computer locale, ad esempio "DomainName".</span><span class="sxs-lookup"><span data-stu-id="7331e-121">Retrieves the short name of the local computer's domain, such as "domainName".</span></span>

<dt>

<span data-ttu-id="7331e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-124">**ForestDNSName**</span><span class="sxs-lookup"><span data-stu-id="7331e-124">**ForestDNSName**</span></span>
<span data-ttu-id="7331e-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-126">Recupera il nome DNS della foresta del computer locale.</span><span class="sxs-lookup"><span data-stu-id="7331e-126">Retrieves the DNS name of the local computer's forest.</span></span>

<dt>

<span data-ttu-id="7331e-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-128">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-129">**IsNativeMode**</span><span class="sxs-lookup"><span data-stu-id="7331e-129">**IsNativeMode**</span></span>
<span data-ttu-id="7331e-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-131">Determina se il dominio del computer locale è in modalità nativa o mista.</span><span class="sxs-lookup"><span data-stu-id="7331e-131">Determines whether the local computer's domain is in native or mixed mode.</span></span>

<dt>

<span data-ttu-id="7331e-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-133">Tipo di dati di scripting: **bool**</span><span class="sxs-lookup"><span data-stu-id="7331e-133">Scripting data type: **BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-134">**PDCRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="7331e-134">**PDCRoleOwner**</span></span>
<span data-ttu-id="7331e-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-136">Recupera il nome distinto dell'oggetto DSA (Directory Service Agent) per il controller di dominio proprietario del ruolo del controller di dominio primario nel dominio del computer locale.</span><span class="sxs-lookup"><span data-stu-id="7331e-136">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the primary domain controller role in the local computer's domain.</span></span>

<dt>

<span data-ttu-id="7331e-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-138">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-139">**SchemaRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="7331e-139">**SchemaRoleOwner**</span></span>
<span data-ttu-id="7331e-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-141">Recupera il nome distinto dell'oggetto DSA (Directory Service Agent) per il controller di dominio proprietario del ruolo di master schema nella foresta del computer locale.</span><span class="sxs-lookup"><span data-stu-id="7331e-141">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the schema master role in the local computer's forest.</span></span>

<dt>

<span data-ttu-id="7331e-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-143">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-144">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="7331e-144">**SiteName**</span></span>
<span data-ttu-id="7331e-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-146">Recupera il nome del sito del computer locale.</span><span class="sxs-lookup"><span data-stu-id="7331e-146">Retrieves the site name of the local computer.</span></span>

<dt>

<span data-ttu-id="7331e-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-148">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-148">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7331e-149">**UserName**</span><span class="sxs-lookup"><span data-stu-id="7331e-149">**UserName**</span></span>
<span data-ttu-id="7331e-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7331e-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="7331e-151">Recupera il Active Directory nome distinto dell'utente corrente, ovvero l'utente connesso o l'utente rappresentato dal thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="7331e-151">Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.</span></span>

<dt>

<span data-ttu-id="7331e-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7331e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7331e-153">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7331e-153">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="7331e-154">Esempio</span><span class="sxs-lookup"><span data-stu-id="7331e-154">Examples</span></span>

<span data-ttu-id="7331e-155">Nell'esempio di codice C++ riportato di seguito vengono recuperate le informazioni sul sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="7331e-155">The following C++ code example retrieves the Windows system information.</span></span> <span data-ttu-id="7331e-156">Per brevità, il controllo degli errori viene omesso.</span><span class="sxs-lookup"><span data-stu-id="7331e-156">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="7331e-157">Nell'esempio di codice seguente Visual Basic vengono recuperate le informazioni sul sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="7331e-157">The following Visual Basic code example retrieves the Windows system information.</span></span>


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



<span data-ttu-id="7331e-158">Nell'esempio di codice VBScript/ASP riportato di seguito vengono recuperate le informazioni sul sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="7331e-158">The following VBScript/ASP code example retrieves the Windows system information.</span></span>


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a><span data-ttu-id="7331e-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7331e-159">Requirements</span></span>



| <span data-ttu-id="7331e-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="7331e-160">Requirement</span></span> | <span data-ttu-id="7331e-161">Valore</span><span class="sxs-lookup"><span data-stu-id="7331e-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7331e-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7331e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="7331e-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7331e-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7331e-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7331e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="7331e-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7331e-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7331e-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7331e-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="7331e-167"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7331e-167"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="7331e-168">DLL</span><span class="sxs-lookup"><span data-stu-id="7331e-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7331e-169"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7331e-169"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="7331e-170">IID</span><span class="sxs-lookup"><span data-stu-id="7331e-170">IID</span></span><br/>                      | <span data-ttu-id="7331e-171">IID \_ IADsADSystemInfo è definito come 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="7331e-171">IID\_IADsADSystemInfo is defined as 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="7331e-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7331e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7331e-173">**IADsADSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="7331e-173">**IADsADSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[<span data-ttu-id="7331e-174">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="7331e-174">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

