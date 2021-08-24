---
title: Registrazione di un callback
description: Se l'applicazione richiede una notifica quando il valore di una variabile di stato cambia o l'istanza del servizio che rappresenta non è più disponibile, l'applicazione deve registrare una funzione di callback.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3dca603e6226d3171aed920311bafcf6844ec9fab5c7aa05deafee7a13fd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768531"
---
# <a name="registering-a-callback"></a>Registrazione di un callback

Se l'applicazione richiede una notifica quando il valore di una variabile di stato cambia o l'istanza del servizio che rappresenta non è più disponibile, l'applicazione deve registrare una funzione di callback. Per registrare una funzione di callback per l'oggetto servizio da richiamare, usare il [**metodo IUPnPService::AddCallback.**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) Questo metodo può essere usato per registrare più callback.

Gli sviluppatori non devono annullare un'operazione asincrona all'interno di un callback asincrono.

> [!Note]  
> L'aggiunta di un callback Visual Basic è diversa dal metodo usato in VBScript. La **funzione GetRef** usata in VBScript non è disponibile in Visual Basic. Pertanto, uno sviluppatore deve creare un [**oggetto IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con la funzione di callback come metodo predefinito. Vedere [Registrazione di un callback in Visual Basic](registering-a-callback-in-visual-basic.md).

 

## <a name="vbscript-example"></a>Esempio di VBScript

Il codice VBScript seguente definisce la funzione di callback **serviceChangeCallback** da richiamare quando i valori delle variabili di stato cambiano o quando l'istanza del servizio non è più disponibile. La funzione ha quattro argomenti.

Il primo argomento della funzione specifica il motivo per cui viene richiamato il callback. Viene richiamato perché una variabile di stato è stata modificata o perché l'istanza del servizio non è più disponibile.

Il secondo argomento è l'oggetto Service per il quale viene richiamato il callback. Se il callback viene richiamato per una modifica della variabile di stato, alla funzione vengono passati due argomenti aggiuntivi: il nome della variabile modificata e il nuovo valore.

In questo esempio, il callback visualizza semplicemente una finestra di messaggio che mostra il nome della variabile modificata e il relativo nuovo valore e se il callback è stato richiamato per una modifica della variabile di stato. In caso contrario, viene visualizzato un messaggio che indica che l'istanza del servizio non è più disponibile.

L'ultima parte del frammento di codice mostra come registrare la funzione di callback usando il [**metodo AddCallback.**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) Si presuppone che le variabili *dell'oggetto* servizio appService e *xportService* siano state inizializzate come illustrato in [Recupero di oggetti servizio.](obtaining-service-objects.md)


```VB
'State Change Callback Function
 
'Note:  In the sub declaration statement below, VARIABLE_UPDATE
'is one of two possible values for the callbackType argument; 
'the other is SERVICE_INSTANCE_DIED

Sub serviceChangeCallback(callbacktype, svcObj, varName, value)
    If (callbacktype = "VARIABLE_UPDATE") then
        Dim outString
        outString = "State Variable Changed:" & vbCrLf
        outString = outString & varName & " == " & value
    
        MsgBox(outString, "Service Callback")
    Else if (callbacktype = "SERVICE_INSTANCE_DIED") then
        MsgBox("Service instance is no longer available", 
               "Service Callback")
    End If
End Sub

' ...
    
'Add our state change callback to each service
appService.AddCallback GetRef("serviceChangeCallback")
xportService.AddCallback GetRef("serviceChangeCallback")
```



## <a name="c-example"></a>Esempio C++


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

class CUPnPServiceCallback : public IUPnPServiceCallback
{
public:
    CUPnPServiceCallback()
    {
        m_lRefCount = 0;
    };
    
    STDMETHODIMP QueryInterface(REFIID iid, LPVOID* ppvObject)
    {
        HRESULT hr = S_OK;
        
        if(NULL == ppvObject)
        {
            hr = E_POINTER;
        }
        else
        {
            *ppvObject = NULL;
        }
        
        if(SUCCEEDED(hr))
        {
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPServiceCallback))
            {
                *ppvObject = static_cast<IUPnPServiceCallback*>(this);
                AddRef();
            }
            else
            {
                hr = E_NOINTERFACE;
            }
        }
        
        return hr;
    };
    
    STDMETHODIMP_(ULONG) AddRef()
    {
        return ::InterlockedIncrement(&m_lRefCount);
    };
    
    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRefCount = ::InterlockedDecrement(&m_lRefCount);
        if(0 == lRefCount)
        {
            delete this;
        }
        
        return lRefCount;
    };
    
    STDMETHODIMP StateVariableChanged(IUPnPService *pus, LPCWSTR pcwszStateVarName, VARIANT varValue)
    {
        HRESULT    hr = S_OK;
        BSTR ServiceId;
        hr = pus->get_Id(&ServiceId);
        if (SUCCEEDED(hr))
        {
            VARIANT AlphaVariant;
            VariantInit(&AlphaVariant);
            hr = VariantChangeType(&AlphaVariant, &varValue, VARIANT_ALPHABOOL, VT_BSTR);
            if(SUCCEEDED(hr))
            {
                printf("StateVariableChanged called for the %S service"
                       " for %S state variable with the value=%S.\n",
                        ServiceId, pcwszStateVarName, V_BSTR(&AlphaVariant));
                VariantClear(&AlphaVariant);
            }
            SysFreeString(ServiceId);
        }
        return hr;
    };

    STDMETHODIMP ServiceInstanceDied(IUPnPService *pus)
    {
        HRESULT hr = S_OK;
        BSTR ServiceType;
        hr = pus->get_ServiceTypeIdentifier(&ServiceType);
        if(SUCCEEDED(hr))
        {
            printf("ServiceInstanceDied called for the %S service!\n", ServiceType);
            SysFreeString(ServiceType);
        }
        return hr;
    };
    
private:
    LONG m_lRefCount;
    
};

HRESULT AddCallbackToService(IUPnPService* pUPnPService)
{
    HRESULT hr = S_OK;

    IUnknown* pUPnPServiceCallback = new CUPnPServiceCallback;
    if(NULL != pUPnPServiceCallback)
    {
        pUPnPServiceCallback->AddRef();
        hr = pUPnPService->AddCallback(pUPnPServiceCallback);
        pUPnPServiceCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
    return hr;
}
```



 

 