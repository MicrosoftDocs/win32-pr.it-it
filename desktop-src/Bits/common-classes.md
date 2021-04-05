---
title: Classi comuni di esempio
description: È possibile utilizzare gli esempi di codice in questo argomento come punto di partenza per molte applicazioni Servizio trasferimento intelligente in background (BITS) che eseguono l'inizializzazione COM, necessitano di gestione degli errori e ricevono notifiche di callback.
ms.assetid: 8fe722a3-fbab-4843-b298-1ea11f54d7a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864fe4aa8d7af5bb6a248364b0e2c636e1c250a6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734847"
---
# <a name="example-common-classes"></a>Esempio: classi comuni

È possibile utilizzare gli esempi di codice in questo argomento come punto di partenza per molte applicazioni Servizio trasferimento intelligente in background (BITS) che eseguono l'inizializzazione COM, necessitano di gestione degli errori e ricevono notifiche di callback.


Nell'esempio di codice seguente viene definita una classe Exception per la gestione degli errori.


```C++
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};
```



La classe deexception è una classe di eccezione generica che accetta un codice HRESULT e una stringa di errore.


Nell'esempio di codice seguente viene definita una classe helper di acquisizione delle risorse per la funzione [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) .


```C++
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};
```



La classe CCoInitializer gestisce l'allocazione delle risorse e la deallocazione per l'inizializzazione COM. Questa classe consente di chiamare il distruttore quando la classe esce dall'ambito. Questa classe elimina la necessità di chiamare il metodo [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) dopo ogni blocco di eccezioni.


L'esempio di codice seguente è la dichiarazione dell'interfaccia di callback CNotifyInterface.


```C++
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor
    CNotifyInterface() {m_lRefCount = 1;};

//Destructor
    ~CNotifyInterface() {};

    //IUnknown methods
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);

private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```



Classe CNotifyInterface derivata dall'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) . La classe CNotifyInterface implementa l'interfaccia IUnknown. Per ulteriori informazioni, vedere [IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown).

CNotifyInterface usa i metodi seguenti per ricevere una notifica che indica che un processo è stato completato, è stato modificato o è in uno stato di errore: [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred), [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)e [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror). Tutti questi metodi accettano un oggetto processo [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .

Questo esempio usa [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare risorse di memoria.


L'esempio di codice seguente è l'implementazione dell'interfaccia di callback [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


```C++
HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed. 

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }
    
    // Clean up
    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```




Il file di intestazione seguente viene usato per le classi di codice comuni. Queste classi vengono usate negli esempi di codice precedenti.


```C++
// commoncode.h
#pragma once

//
// Exception class used for error handling
//
class MyException
{
public:
    MyException(HRESULT hr, LPWSTR message):Error(hr), Message(message)
    {

    }
    HRESULT Error;
    std::wstring Message;
};

// CoInitialize helper class
class CCoInitializer 
{
public:
    CCoInitializer( DWORD dwCoInit ) 
    { 
        HRESULT hr = CoInitializeEx( NULL, dwCoInit );
        if (FAILED(hr))
        {
            throw MyException(hr,L"CoInitialize");
        }
    } 

    ~CCoInitializer() throw() 
    { 
        CoUninitialize(); 
    } 
};

//
// Implementation of the Callback interface
//
class CNotifyInterface : public IBackgroundCopyCallback
{
    LONG m_lRefCount;

public:
    //Constructor, Destructor
    CNotifyInterface() {m_lRefCount = 1;};
    ~CNotifyInterface() {};

    //IUnknown
    HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
    ULONG __stdcall AddRef();
    ULONG __stdcall Release();

    //IBackgroundCopyCallback2 methods
    HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
    HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
    HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);
private:
    CNotifyInterface(const CNotifyInterface&);
    CNotifyInterface& operator=(const CNotifyInterface&);
};
```




Il codice di esempio seguente è l'implementazione delle classi di codice comuni.


```C++
//commoncode.cpp

#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
    if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
    {
        *ppvObj = this;
    }
    else
    {
        *ppvObj = NULL; 
        return E_NOINTERFACE;
    }

    AddRef();
    return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
    return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
    // not thread safe
    ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

    if(0 == ulCount) 
    {
        delete this;
    }

    return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
    HRESULT hr;

    wprintf(L"Job transferred. Completing Job...\n");
    hr = pJob->Complete();
    if (FAILED(hr))
    {
        //BITS probably was unable to rename one or more of the 
        //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
        //method for more details.
        wprintf(L"Job Completion Failed with error %x\n", hr);
    }

    PostQuitMessage(0);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
    return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
    WCHAR* pszJobName = NULL;
    WCHAR* pszErrorDescription = NULL;

    //Use pJob and pError to retrieve information of interest. For example,
    //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
    //to determine the context in which the job failed.

    wprintf(L"Job entered error state...\n");
    HRESULT hr = pJob->GetDisplayName(&pszJobName);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get job name\n");
    }

    hr = pError->GetErrorDescription(GetUserDefaultUILanguage(), &pszErrorDescription);
    if (FAILED(hr))
    {
        wprintf(L"Unable to get error description\n");
    }
    if (pszJobName && pszErrorDescription)
    {
        wprintf(L"Job %s ",pszJobName);
        wprintf(L"encountered the following error:\n");
        wprintf(L"%s\n",pszErrorDescription);
    }

    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);

    PostQuitMessage(hr);

    //If you do not return S_OK, BITS continues to call this callback.
    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IUnknown]( /windows/win32/api/unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)
</dt> </dl>

 

 