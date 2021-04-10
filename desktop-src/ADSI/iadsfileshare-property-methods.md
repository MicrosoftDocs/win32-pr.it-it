---
title: Metodi di proprietà IADsFileShare (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsFileshare ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsFileShare ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120743"
---
# <a name="iadsfileshare-property-methods"></a><span data-ttu-id="3ccea-105">Metodi di proprietà IADsFileShare</span><span class="sxs-lookup"><span data-stu-id="3ccea-105">IADsFileShare Property Methods</span></span>

<span data-ttu-id="3ccea-106">I metodi di proprietà dell'interfaccia [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3ccea-106">The property methods of the [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="3ccea-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3ccea-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3ccea-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ccea-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3ccea-109">**CurrentUserCount**</span><span class="sxs-lookup"><span data-stu-id="3ccea-109">**CurrentUserCount**</span></span>
<span data-ttu-id="3ccea-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3ccea-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3ccea-111">Il numero di utenti connessi alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="3ccea-111">The number of users connected to the share.</span></span>

<dt>

<span data-ttu-id="3ccea-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ccea-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ccea-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="3ccea-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ccea-114">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3ccea-114">**Description**</span></span>
<span data-ttu-id="3ccea-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3ccea-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3ccea-116">Descrizione della condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3ccea-116">The description of the file share.</span></span>

<dt>

<span data-ttu-id="3ccea-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3ccea-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3ccea-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3ccea-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ccea-119">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="3ccea-119">**HostComputer**</span></span>
<span data-ttu-id="3ccea-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3ccea-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="3ccea-121">Riferimento ADsPath al computer host.</span><span class="sxs-lookup"><span data-stu-id="3ccea-121">An ADsPath reference to the host computer.</span></span>

<dt>

<span data-ttu-id="3ccea-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3ccea-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3ccea-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3ccea-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ccea-124">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="3ccea-124">**MaxUserCount**</span></span>
<span data-ttu-id="3ccea-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3ccea-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="3ccea-126">Il numero massimo di utenti autorizzati ad accedere alla condivisione in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="3ccea-126">The maximum number of users allowed to access the share at one time.</span></span>

<dt>

<span data-ttu-id="3ccea-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ccea-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ccea-128">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="3ccea-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3ccea-129">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="3ccea-129">**Path**</span></span>
<span data-ttu-id="3ccea-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3ccea-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="3ccea-131">Percorso file system della directory condivisa.</span><span class="sxs-lookup"><span data-stu-id="3ccea-131">The file system path to the shared directory.</span></span>

<dt>

<span data-ttu-id="3ccea-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3ccea-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3ccea-133">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3ccea-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="3ccea-134">Esempio</span><span class="sxs-lookup"><span data-stu-id="3ccea-134">Examples</span></span>

<span data-ttu-id="3ccea-135">Per accedere alle proprietà delle condivisioni file in un computer, è innanzitutto necessario eseguire l'associazione a "LanmanServer" nel computer.</span><span class="sxs-lookup"><span data-stu-id="3ccea-135">To access the properties of file shares on a computer, you must first bind to the "LanmanServer" on the machine.</span></span> <span data-ttu-id="3ccea-136">Nell'esempio di codice seguente viene illustrato come impostare la descrizione e il numero massimo di utenti consentiti per tutte le condivisioni file pubbliche nel computer, denominato "computer", nel dominio predefinito.</span><span class="sxs-lookup"><span data-stu-id="3ccea-136">The following code example shows how to set up the description and the maximum number of allowed users for all the public file shares on the computer, named as "myMachine", in the default domain.</span></span>


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



<span data-ttu-id="3ccea-137">Nell'esempio di codice seguente viene illustrato come rendere la directory C: \\ cartella esistente una condivisione file pubblica.</span><span class="sxs-lookup"><span data-stu-id="3ccea-137">The following code example shows how to make the existing C:\\MyFolder directory a public file share.</span></span>


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



<span data-ttu-id="3ccea-138">L'esempio di codice seguente rende la directory C: \\ cartella esistente una condivisione file pubblica.</span><span class="sxs-lookup"><span data-stu-id="3ccea-138">The following code example makes the existing C:\\MyFolder directory a public file share.</span></span>


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a><span data-ttu-id="3ccea-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ccea-139">Requirements</span></span>



| <span data-ttu-id="3ccea-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ccea-140">Requirement</span></span> | <span data-ttu-id="3ccea-141">Valore</span><span class="sxs-lookup"><span data-stu-id="3ccea-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccea-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ccea-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3ccea-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ccea-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ccea-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ccea-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3ccea-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ccea-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ccea-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ccea-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ccea-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ccea-147"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3ccea-148">DLL</span><span class="sxs-lookup"><span data-stu-id="3ccea-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ccea-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ccea-149"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ccea-150">IID</span><span class="sxs-lookup"><span data-stu-id="3ccea-150">IID</span></span><br/>                      | <span data-ttu-id="3ccea-151">IID \_ IADsFileShare è definito come EB6DCAF0-4b83-11CF-A995-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="3ccea-151">IID\_IADsFileShare is defined as EB6DCAF0-4B83-11CF-A995-00AA006BC149</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3ccea-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ccea-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ccea-153">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="3ccea-153">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="3ccea-154">**IADsFileShare**</span><span class="sxs-lookup"><span data-stu-id="3ccea-154">**IADsFileShare**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[<span data-ttu-id="3ccea-155">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="3ccea-155">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





