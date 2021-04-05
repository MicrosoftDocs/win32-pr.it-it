---
title: Metodi di proprietà IADsSession (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsSession ottengono o impostano le proprietà descritte nella tabella seguente. Per ulteriori informazioni e per una discussione generale sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsSession ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873669"
---
# <a name="iadssession-property-methods"></a><span data-ttu-id="caa30-105">Metodi di proprietà IADsSession</span><span class="sxs-lookup"><span data-stu-id="caa30-105">IADsSession Property Methods</span></span>

<span data-ttu-id="caa30-106">I metodi di proprietà dell'interfaccia [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="caa30-106">The property methods of the [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="caa30-107">Per ulteriori informazioni e per una discussione generale sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="caa30-107">For more information and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="caa30-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="caa30-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="caa30-109">**Computer**</span><span class="sxs-lookup"><span data-stu-id="caa30-109">**Computer**</span></span>
<span data-ttu-id="caa30-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="caa30-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="caa30-111">Nome della workstation client.</span><span class="sxs-lookup"><span data-stu-id="caa30-111">Name of the client workstation.</span></span>

<dt>

<span data-ttu-id="caa30-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="caa30-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caa30-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="caa30-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="caa30-114">**ComputerPath**</span><span class="sxs-lookup"><span data-stu-id="caa30-114">**ComputerPath**</span></span>
<span data-ttu-id="caa30-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="caa30-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="caa30-116">ADsPath dell'oggetto computer per la workstation client.</span><span class="sxs-lookup"><span data-stu-id="caa30-116">ADsPath of the computer object for the client workstation.</span></span>

<dt>

<span data-ttu-id="caa30-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="caa30-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caa30-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="caa30-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="caa30-119">**Tempo**</span><span class="sxs-lookup"><span data-stu-id="caa30-119">**ConnectTime**</span></span>
<span data-ttu-id="caa30-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="caa30-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="caa30-121">Tempo trascorso, in secondi, dall'avvio della sessione.</span><span class="sxs-lookup"><span data-stu-id="caa30-121">Elapsed time, in seconds, since the session started.</span></span>

<dt>

<span data-ttu-id="caa30-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="caa30-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caa30-123">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="caa30-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="caa30-124">**Tempoinattività**</span><span class="sxs-lookup"><span data-stu-id="caa30-124">**IdleTime**</span></span>
<span data-ttu-id="caa30-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="caa30-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="caa30-126">Tempo di inattività, in secondi, della sessione.</span><span class="sxs-lookup"><span data-stu-id="caa30-126">Idle time, in seconds, of the session.</span></span>

<dt>

<span data-ttu-id="caa30-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="caa30-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caa30-128">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="caa30-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="caa30-129">**Utente**</span><span class="sxs-lookup"><span data-stu-id="caa30-129">**User**</span></span>
<span data-ttu-id="caa30-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="caa30-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="caa30-131">Nome dell'utente della sessione.</span><span class="sxs-lookup"><span data-stu-id="caa30-131">The name of the user of the session.</span></span>

<dt>

<span data-ttu-id="caa30-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="caa30-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caa30-133">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="caa30-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="caa30-134">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="caa30-134">**UserPath**</span></span>
<span data-ttu-id="caa30-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="caa30-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="caa30-136">ADsPath dell'oggetto utente per l'utente della sessione.</span><span class="sxs-lookup"><span data-stu-id="caa30-136">The ADsPath of the user object for the user of this session.</span></span>

<dt>

<span data-ttu-id="caa30-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="caa30-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="caa30-138">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="caa30-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="caa30-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="caa30-139">Examples</span></span>

<span data-ttu-id="caa30-140">Nell'esempio di codice riportato di seguito viene illustrato come esaminare le sessioni per un servizio file.</span><span class="sxs-lookup"><span data-stu-id="caa30-140">The following code example shows how to examine sessions for a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="caa30-141">Nell'esempio di codice seguente viene enumerata una raccolta di sessioni.</span><span class="sxs-lookup"><span data-stu-id="caa30-141">The following code example enumerates a collection of sessions.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a><span data-ttu-id="caa30-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caa30-142">Requirements</span></span>



| <span data-ttu-id="caa30-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="caa30-143">Requirement</span></span> | <span data-ttu-id="caa30-144">Valore</span><span class="sxs-lookup"><span data-stu-id="caa30-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="caa30-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caa30-145">Minimum supported client</span></span><br/> | <span data-ttu-id="caa30-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="caa30-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="caa30-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caa30-147">Minimum supported server</span></span><br/> | <span data-ttu-id="caa30-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="caa30-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="caa30-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="caa30-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa30-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="caa30-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="caa30-151">DLL</span><span class="sxs-lookup"><span data-stu-id="caa30-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caa30-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caa30-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="caa30-153">IID</span><span class="sxs-lookup"><span data-stu-id="caa30-153">IID</span></span><br/>                      | <span data-ttu-id="caa30-154">IID \_ IADsSession è definito come 398B7DA0-4aab-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="caa30-154">IID\_IADsSession is defined as 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="caa30-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="caa30-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa30-156">**IADsFileServiceOperations:: Sessions**</span><span class="sxs-lookup"><span data-stu-id="caa30-156">**IADsFileServiceOperations::Sessions**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[<span data-ttu-id="caa30-157">**IADsSession**</span><span class="sxs-lookup"><span data-stu-id="caa30-157">**IADsSession**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





