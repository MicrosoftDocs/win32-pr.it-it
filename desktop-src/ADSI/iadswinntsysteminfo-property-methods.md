---
title: Metodi di proprietà IADsWinNTSystemInfo (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsWinNTSystemInfo ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsWinNTSystemInfo ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301084"
---
# <a name="iadswinntsysteminfo-property-methods"></a><span data-ttu-id="f346f-105">Metodi di proprietà IADsWinNTSystemInfo</span><span class="sxs-lookup"><span data-stu-id="f346f-105">IADsWinNTSystemInfo Property Methods</span></span>

<span data-ttu-id="f346f-106">I metodi di proprietà dell'interfaccia [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f346f-106">The property methods of the [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="f346f-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f346f-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f346f-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f346f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f346f-109">**NomeComputer**</span><span class="sxs-lookup"><span data-stu-id="f346f-109">**ComputerName**</span></span>
<span data-ttu-id="f346f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f346f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f346f-111">Nome del computer host in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f346f-111">Name of the host computer where the application is running.</span></span>

<dt>

<span data-ttu-id="f346f-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f346f-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f346f-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f346f-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f346f-114">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="f346f-114">**DomainName**</span></span>
<span data-ttu-id="f346f-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f346f-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f346f-116">Nome del dominio a cui appartiene l'utente.</span><span class="sxs-lookup"><span data-stu-id="f346f-116">Name of the domain to which the user belongs.</span></span>

<dt>

<span data-ttu-id="f346f-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f346f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f346f-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f346f-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f346f-119">**PDC**</span><span class="sxs-lookup"><span data-stu-id="f346f-119">**PDC**</span></span>
<span data-ttu-id="f346f-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f346f-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="f346f-121">Nome del controller di dominio primario a cui appartiene il computer host.</span><span class="sxs-lookup"><span data-stu-id="f346f-121">Name of the primary domain controller to which the host computer belongs.</span></span>

<dt>

<span data-ttu-id="f346f-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f346f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f346f-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f346f-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f346f-124">**UserName**</span><span class="sxs-lookup"><span data-stu-id="f346f-124">**UserName**</span></span>
<span data-ttu-id="f346f-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f346f-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="f346f-126">Nome dell'account utente con cui viene creato l'oggetto **WinNTSystemInfo** .</span><span class="sxs-lookup"><span data-stu-id="f346f-126">Name of the user account under which the **WinNTSystemInfo** object is created.</span></span>

<dt>

<span data-ttu-id="f346f-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f346f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f346f-128">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f346f-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="f346f-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="f346f-129">Examples</span></span>

<span data-ttu-id="f346f-130">Nell'esempio di codice C/C++ riportato di seguito vengono recuperate le informazioni sul sistema WinNT.</span><span class="sxs-lookup"><span data-stu-id="f346f-130">The following C/C++ code example retrieves the WinNT system information.</span></span> <span data-ttu-id="f346f-131">Per brevità, il controllo degli errori viene omesso.</span><span class="sxs-lookup"><span data-stu-id="f346f-131">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="f346f-132">Nell'esempio di codice Visual Basic riportato di seguito vengono recuperate le informazioni sul sistema WinNT.</span><span class="sxs-lookup"><span data-stu-id="f346f-132">The following Visual Basic code example retrieves the WinNT system information.</span></span>


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



<span data-ttu-id="f346f-133">Nell'esempio di codice seguente Visual Basic Scripting Edition/Active Server Pages vengono recuperate le informazioni sul sistema WinNT.</span><span class="sxs-lookup"><span data-stu-id="f346f-133">The following Visual Basic Scripting Edition/Active Server Pages code example retrieves the WinNT system information.</span></span>


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a><span data-ttu-id="f346f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f346f-134">Requirements</span></span>



| <span data-ttu-id="f346f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f346f-135">Requirement</span></span> | <span data-ttu-id="f346f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f346f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f346f-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f346f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f346f-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f346f-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f346f-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f346f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f346f-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f346f-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f346f-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f346f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f346f-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f346f-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f346f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f346f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f346f-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f346f-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f346f-145">IID</span><span class="sxs-lookup"><span data-stu-id="f346f-145">IID</span></span><br/>                      | <span data-ttu-id="f346f-146">IID \_ IADsWinNTSystemInfo è definito come 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="f346f-146">IID\_IADsWinNTSystemInfo is defined as 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f346f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f346f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f346f-148">**IADsWinNTSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="f346f-148">**IADsWinNTSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





