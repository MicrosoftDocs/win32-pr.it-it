---
title: Registrazione di un callback
description: Se l'applicazione richiede una notifica quando il valore di una variabile di stato cambia o l'istanza del servizio che rappresenta diventa non disponibile, l'applicazione deve registrare una funzione di callback.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9095ab4b5b2d43a12f7e806eabc24b174a0311
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728095"
---
# <a name="registering-a-callback"></a><span data-ttu-id="6ac2b-103">Registrazione di un callback</span><span class="sxs-lookup"><span data-stu-id="6ac2b-103">Registering a Callback</span></span>

<span data-ttu-id="6ac2b-104">Se l'applicazione richiede una notifica quando il valore di una variabile di stato cambia o l'istanza del servizio che rappresenta diventa non disponibile, l'applicazione deve registrare una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-104">If the application requires notification when the value of a state variable changes or the service instance it represents becomes unavailable, the application must register a callback function.</span></span> <span data-ttu-id="6ac2b-105">Per registrare una funzione di callback per l'oggetto servizio da richiamare, usare il metodo [**IUPnPService:: AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="6ac2b-105">To register a callback function for the service object to invoke, use the [**IUPnPService::AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="6ac2b-106">Questo metodo può essere utilizzato per registrare più di un callback.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-106">This method can be used to register more than one callback.</span></span>

<span data-ttu-id="6ac2b-107">Gli sviluppatori non devono annullare un'operazione asincrona all'interno di un callback asincrono.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-107">Developers should not cancel an asynchronous operation inside an asynchronous callback.</span></span>

> [!Note]  
> <span data-ttu-id="6ac2b-108">L'aggiunta di un callback in Visual Basic è diversa dal metodo utilizzato in VBScript.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-108">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="6ac2b-109">La funzione **GetRef** utilizzata in VBScript non è disponibile in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-109">The **GetRef** function used in the VBScript is not available in Visual Basic.</span></span> <span data-ttu-id="6ac2b-110">Pertanto, uno sviluppatore deve creare un oggetto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con la funzione di callback come metodo predefinito.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-110">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="6ac2b-111">Vedere [registrazione di un callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="6ac2b-111">See [Registering a Callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="6ac2b-112">Esempio di VBScript</span><span class="sxs-lookup"><span data-stu-id="6ac2b-112">VBScript Example</span></span>

<span data-ttu-id="6ac2b-113">Nel codice VBScript seguente viene definita la funzione di callback **serviceChangeCallback**, da richiamare quando i valori delle variabili di stato cambiano o quando l'istanza del servizio non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-113">The following VBScript code defines the callback function **serviceChangeCallback**, to be invoked when the values of state variables change or when the service instance becomes unavailable.</span></span> <span data-ttu-id="6ac2b-114">La funzione ha quattro argomenti.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-114">The function has four arguments.</span></span>

<span data-ttu-id="6ac2b-115">Il primo argomento della funzione specifica il motivo per cui viene richiamato il callback.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-115">The first argument to the function specifies the reason the callback is invoked.</span></span> <span data-ttu-id="6ac2b-116">Viene richiamato perché una variabile di stato è stata modificata o perché l'istanza del servizio non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-116">It is invoked either because a state variable changed, or because the service instance has become unavailable.</span></span>

<span data-ttu-id="6ac2b-117">Il secondo argomento è l'oggetto servizio per il quale viene richiamato il callback.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-117">The second argument is the Service object for which the callback is invoked.</span></span> <span data-ttu-id="6ac2b-118">Se il callback viene richiamato per una modifica di variabile di stato, alla funzione vengono passati due argomenti aggiuntivi: il nome della variabile modificata e il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-118">If the callback is invoked for a state variable change, then the function is passed two additional arguments: the name of the variable that changed, and its new value.</span></span>

<span data-ttu-id="6ac2b-119">In questo esempio, il callback Visualizza semplicemente una finestra di messaggio che mostra il nome della variabile modificata e il nuovo valore e se il callback è stato richiamato per una modifica della variabile di stato.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-119">In this example, the callback simply displays a message box that shows the name of the changed variable and its new value, and if the callback was invoked for a state variable change.</span></span> <span data-ttu-id="6ac2b-120">In caso contrario, viene visualizzato un messaggio che indica che l'istanza del servizio non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6ac2b-120">Otherwise, it displays a message that indicates the service instance is no longer available.</span></span>

<span data-ttu-id="6ac2b-121">Nell'ultima parte del frammento di codice viene illustrato come registrare la funzione di callback utilizzando il metodo [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="6ac2b-121">The last part of the code fragment shows how to register the callback function using the [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="6ac2b-122">Si presuppone che le variabili dell'oggetto servizio, *Appservice* e *xportService* , siano state inizializzate come illustrato in [acquisizione degli oggetti servizio](obtaining-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6ac2b-122">The service object variables, *appService* and *xportService* are assumed to have been initialized as shown in [Obtaining Service Objects](obtaining-service-objects.md).</span></span>


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



## <a name="c-example"></a><span data-ttu-id="6ac2b-123">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="6ac2b-123">C++ Example</span></span>


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



 

 