---
title: Estensione della classe helper NDF
description: In questo esempio viene illustrato come implementare le funzioni di diagnosi e correzione NDF.
ms.assetid: 18e66d09-e565-4b86-8bc3-600f2159a4bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd8fd7683aded0573034ffec56097256093c61e2bb0f9ec2e7bcd353ff8d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802111"
---
# <a name="ndf-helper-class-extension"></a>Estensione della classe helper NDF

In questo esempio viene illustrato come implementare le funzioni di diagnosi e correzione NDF. In questo esempio deve esistere un file di configurazione critico perché il sistema rimanga integro. Di conseguenza, il problema è determinare se il file esiste. In caso contrario, il sistema non è integro e il problema viene diagnosticato dalla funzione NDF. Il ripristino consente di creare nuovamente il file mancante.

Per diagnosticare e correggere il problema, è necessario usare quattro metodi [**INetDiagHelper:**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)e [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).

## <a name="initializing-the-helper-class"></a>Inizializzazione della classe helper

Inizializzare e recuperare il nome del file da individuare. Questo nome file viene passato durante la diagnosi come attributo helper denominato "filename".


```C++
#include <windows.h>
//utility function to simplify string allocation and copies, user throughout example
HRESULT 
StringCchCopyWithAlloc (
    PWSTR* Dest, 
    size_t cchMaxLen,
    in PCWSTR Src)
{
    if (NULL == Dest || NULL == Src || cchMaxLen > USHRT_MAX)
    {
        return E_INVALIDARG;
    }
    size_t cchSize = 0;

    HRESULT hr = StringCchLength(Src, cchMaxLen - 1, &cchSize); 
    if (FAILED(hr))
    {
        return hr;
    }

    size_t cbSize = (cchSize + 1)*sizeof(WCHAR);
    *Dest = (PWSTR) CoTaskMemAlloc(cbSize);
    if (NULL == *Dest)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(*Dest, cbSize);

    return StringCchCopy((STRSAFE_LPWSTR)*Dest, cchSize + 1, Src);    
}

HRESULT SimpleFileHelperClass::Initialize(
        /* [in] */ ULONG celt,
        /* [size_is][in] */ HELPER_ATTRIBUTE rgAttributes[  ])
{
    if(celt < 1)
    {
        return E_INVALIDARG;
    }
    if(rgAttributes == NULL)
    {
        return E_INVALIDARG; 
    }
    else
    {
        //verify the attribute is named as expected
        if (wcscmp(rgAttributes[0].pwszName, L"filename")==0)
        {
            //copy the attribute to member variable
            return StringCchCopyWithAlloc(&m_pwszTestFile, MAX_PATH, 
                    rgAttributes[0].PWStr);
        } else {
            //the attribute isn't named as expected
            return E_INVALIDARG;
        }
    }
}

```



## <a name="checking-on-the-files-existence"></a>Verifica dell'esistenza del file

Il [**metodo LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) viene usato per verificare l'esistenza del file. Se il file esiste, lo stato della diagnosi viene impostato **su DS \_ REJECTED,** a indicare che non ci sono problemi. Se non è possibile trovare il file, lo stato della diagnosi viene impostato su **DS \_ CONFIRMED.**


```C++
#include <windows.h>

HRESULT SimpleFileHelperClass::LowHealth( 
            /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
            /* [string][out] */ LPWSTR *ppwszDescription,
            /* [out] */ long *pDeferredTime,
            /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    HANDLE hFile = NULL;
    LPWSTR pwszDiagString=NULL;
    // does the file already exist?
    hFile = CreateFile(
        m_pwszTestFile, 
        GENERIC_READ, 
        0, 
        NULL, 
        OPEN_EXISTING, 
        FILE_ATTRIBUTE_NORMAL, 
        NULL);

    if(INVALID_HANDLE_VALUE == hFile)
    { 
        // alloc and set the diagnosis description and status
        HRESULT hr = StringCchCopyWithAlloc(&pwszDiagString, MAX_PATH, 
                    L"The file was deleted.");
        if (FAILED(hr))
        {
            return hr;
        }
  
        *ppwszDescription = pwszDiagString;
        *pStatus = DS_CONFIRMED;
        return S_OK;
    }
    CloseHandle(hFile); 
    
    //the file exists
    *pStatus = DS_REJECTED;
    return S_OK;
}
```



## <a name="determining-the-repair-action"></a>Determinazione dell'azione di ripristino

Se [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) restituisce **DS \_ CONFIRMED,** [**GetRepairInfo viene**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) implementato per determinare l'azione di ripristino appropriata. In questo esempio, ciò significa creare nuovamente il file.


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::GetRepairInfo( 
            /* [in] */ PROBLEM_TYPE problem,
            /* [out] */ ULONG *pcelt,
            /* [size_is][size_is][out] */ RepairInfo **ppInfo)
{
    HRESULT hr=S_OK;
    RepairInfo* pRepair = (RepairInfo *)CoTaskMemAlloc(sizeof(RepairInfo));
    if (pRepair == NULL) {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pRepair,sizeof(RepairInfo));

    // set the repair description and class name
    hr = StringCchCopyWithAlloc(&pRepair->pwszClassName, MAX_PATH,
                L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    hr = StringCchCopyWithAlloc(&pRepair->pwszDescription, MAX_PATH, 
                L"Low Health Repair");
    if (FAILED(hr))
    {
        goto Error;
    }
  
    // set the resolution GUID and cost
    pRepair->guid = ID_LowHealthRepair;
    pRepair->cost = 0;
    // set repair status flags
    pRepair->sidType = WinWorldSid;
    pRepair->scope = RS_SYSTEM;
    pRepair->risk = RR_NORISK;
    pRepair->flags |= DF_IMPERSONATION; //impersonate the user when repairing
    pRepair->UiInfo.type = UIT_NONE;
    
    //pass back the repair
    *ppInfo = pRepair; 
    *pcelt = 1; //number of repairs

    return S_OK;

Error:
    if(pRepair){
        if(pRepair->pwszClassName){
            CoTaskMemFree(pRepair->pwszClassName);
        }
        if(pRepair->pwszDescription){
            CoTaskMemFree(pRepair->pwszDescription);
        }
    }
    return hr;
}

```



## <a name="repairing-the-problem"></a>Correzione del problema

All'utente vengono presentate le opzioni di correzione restituite da [**GetRepairInfo,**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)a meno che non sia presente una sola opzione di ripristino, nel qual caso viene eseguita automaticamente. Il [**metodo Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) viene chiamato con la struttura [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) applicabile in modo che il file di configurazione possa essere ripristinato.


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::Repair( 
            /* [in] */ RepairInfo *pInfo,
            /* [out] */ long *pDeferredTime,
            /* [out] */ REPAIR_STATUS *pStatus)
{
    //verify expected repair was requested
    if(IsEqualGUID(ID_LowHealthRepair, pInfo->guid)){
        HANDLE hFile = NULL;
        hFile = CreateFile(m_pwszTestFile, 
                                GENERIC_WRITE, 
                                0, 
                                NULL, 
                                CREATE_ALWAYS,
                                FILE_ATTRIBUTE_NORMAL, 
                                NULL);
        if(INVALID_HANDLE_VALUE == hFile)
        {
            // repair failed
            *pStatus = RS_UNREPAIRED;
            return HRESULT_FROM_WIN32(GetLastError());
        }
        CloseHandle(hFile);
        
        // repair succeeded
        *pStatus = RS_REPAIRED;
    } else {
        return E_INVALIDARG; //unkown repair passed in
    }
    return S_OK;
}
```



 

 




