---
title: Richiamo di azioni
description: Il Metodo InvokeAction di IUPnPService consente di richiamare azioni sugli oggetti servizio.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7550575281681f3f533db90ef1c1034dbaa085
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399468"
---
# <a name="invoking-actions"></a><span data-ttu-id="eb760-103">Richiamo di azioni</span><span class="sxs-lookup"><span data-stu-id="eb760-103">Invoking Actions</span></span>

<span data-ttu-id="eb760-104">Il metodo [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) consente di richiamare le azioni sugli oggetti servizio.</span><span class="sxs-lookup"><span data-stu-id="eb760-104">The [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) method allows actions to be invoked on Service objects.</span></span> <span data-ttu-id="eb760-105">Questo metodo ha due parametri di input: il nome di un'azione e una matrice di argomenti di input per tale azione.</span><span class="sxs-lookup"><span data-stu-id="eb760-105">This method has two input parameters: the name of an action and an array of input arguments to that action.</span></span> <span data-ttu-id="eb760-106">Il metodo ha due parametri:</span><span class="sxs-lookup"><span data-stu-id="eb760-106">The method has two parameters:</span></span>

-   <span data-ttu-id="eb760-107">Parametro uno: parametro di input/output, ovvero una matrice di argomenti di output per l'azione.</span><span class="sxs-lookup"><span data-stu-id="eb760-107">Parameter one — an input/output parameter: an array of output arguments for that action.</span></span>
-   <span data-ttu-id="eb760-108">Parametro due, un parametro di output: un valore restituito.</span><span class="sxs-lookup"><span data-stu-id="eb760-108">Parameter two — an output parameter: a return value.</span></span>

<span data-ttu-id="eb760-109">Il metodo fa in modo che l'azione venga richiamata sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb760-109">The method causes the action to be invoked on the device.</span></span> <span data-ttu-id="eb760-110">Il dispositivo genera notifiche di eventi se l'azione causa la modifica delle variabili di stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb760-110">The device generates event notifications if the action causes state variables of the device to change.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="eb760-111">Esempio di VBScript</span><span class="sxs-lookup"><span data-stu-id="eb760-111">VBScript Example</span></span>

<span data-ttu-id="eb760-112">Nell'esempio di codice VBScript riportato di seguito vengono richiamate due azioni su un oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="eb760-112">The following VBScript code example invokes two actions on a Service object.</span></span> <span data-ttu-id="eb760-113">La prima azione, *GetTrackInfo*, accetta un argomento di input, un numero di traccia.</span><span class="sxs-lookup"><span data-stu-id="eb760-113">The first action, *GetTrackInfo*, takes one input argument, a track number.</span></span> <span data-ttu-id="eb760-114">L'azione *GetTrackInfo* restituisce la lunghezza della traccia come valore restituito.</span><span class="sxs-lookup"><span data-stu-id="eb760-114">The *GetTrackInfo* action returns the track length as the return value.</span></span> <span data-ttu-id="eb760-115">L'azione ha anche un argomento di output, che contiene il titolo della traccia se il metodo restituisce Success.</span><span class="sxs-lookup"><span data-stu-id="eb760-115">The action also has one output argument, which contains the track title if the method returns success.</span></span>

<span data-ttu-id="eb760-116">Dopo aver richiamato l'azione *GetTrackInfo* , nell'esempio viene richiamata l'azione Play, che non accetta argomenti.</span><span class="sxs-lookup"><span data-stu-id="eb760-116">After invoking the *GetTrackInfo* action, the example invokes the Play action, which takes no arguments.</span></span> <span data-ttu-id="eb760-117">Tuttavia, poiché la sintassi di [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) richiede una matrice di entrambi gli argomenti di input e di output, è necessario che nell'esempio venga creata una matrice vuota, *emptyArgs*, senza elementi.</span><span class="sxs-lookup"><span data-stu-id="eb760-117">However, because the syntax of [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires an array of both input and output arguments, the example must create an empty array, *emptyArgs*, with no elements.</span></span> <span data-ttu-id="eb760-118">Nell'esempio la matrice viene passata a **InvokeAction** per gli argomenti di input e di output, insieme al nome dell'azione.</span><span class="sxs-lookup"><span data-stu-id="eb760-118">The example passes this array to **InvokeAction** for both the input and output arguments, along with the name of the action.</span></span>


```VB
Dim returnVal
Dim outArgs(1)
Dim args(1)
args(0) = 3
returnVal = service.InvokeAction("GetTrackInfo", args, outArgs)
'return Val now contains the track length
'and outArgs(0) contains the track title
Dim emptyArgs(0)
returnVal = service.InvokeAction("Play", emptyArgs, emptyArgs)
'returnVal indicates if the action was successful
```



## <a name="c-example"></a><span data-ttu-id="eb760-119">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="eb760-119">C++ Example</span></span>

<span data-ttu-id="eb760-120">Nell'esempio seguente viene definita una funzione C++ che richiama un'azione senza argomenti.</span><span class="sxs-lookup"><span data-stu-id="eb760-120">The following example defines a C++ function that invokes an action with no arguments.</span></span> <span data-ttu-id="eb760-121">Poiché [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) richiede un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di argomenti da passare, in questo esempio viene creato un **SAFEARRAY** vuoto.</span><span class="sxs-lookup"><span data-stu-id="eb760-121">Because [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of arguments to be passed in, this example creates an empty **SAFEARRAY**.</span></span> <span data-ttu-id="eb760-122">Poiché questa azione non restituisce un valore o ha argomenti di output, in questo esempio vengono ignorati gli ultimi due valori [**Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) passati a **InvokeAction**.</span><span class="sxs-lookup"><span data-stu-id="eb760-122">Since this action does not return a value or have output arguments, this example ignores the last two [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) values passed to **InvokeAction**.</span></span>

<span data-ttu-id="eb760-123">Il dispositivo genera notifiche di eventi se l'azione causa la modifica delle variabili di stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb760-123">The device generates event notifications if the action causes state variables of the device to change.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokePlay(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"Play");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 0;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            LONG    lStatus;
            VARIANT varInArgs;

            VariantInit(&varInArgs);

            varInArgs.vt = VT_VARIANT | VT_ARRAY;

            V_ARRAY(&varInArgs) = psa;

            hr = pService->InvokeAction(bstrActionName,
                                        varInArgs,
                                        NULL,
                                        NULL);

            if (SUCCEEDED(hr))
            {
                wcout << L"Action invoked successfully\n"; 
            }
            else
            {
                wcerr << L"Failed to invoke action - HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        

            }                                   

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



<span data-ttu-id="eb760-124">Nell'esempio seguente viene richiamata l'azione fittizia *GetTrackInfo* .</span><span class="sxs-lookup"><span data-stu-id="eb760-124">The following example invokes the fictitious *GetTrackInfo* action.</span></span> <span data-ttu-id="eb760-125">Accetta un numero di traccia come argomento, restituisce la lunghezza della traccia come valore restituito e restituisce il titolo della traccia in un argomento di output.</span><span class="sxs-lookup"><span data-stu-id="eb760-125">It takes a track number as an argument, returns the track length as a return value, and returns the track title in an output argument.</span></span> <span data-ttu-id="eb760-126">Il codice è simile all'esempio precedente, ad eccezione del fatto che anziché creare un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) vuoto di argomenti di input, in questo esempio viene inserita una [**variante**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) che contiene il numero di traccia.</span><span class="sxs-lookup"><span data-stu-id="eb760-126">The code is similar to the previous example, except that instead of creating an empty [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of input arguments, this example inserts a [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) that contains the track number.</span></span> <span data-ttu-id="eb760-127">Se [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) restituisce Success, in questo esempio vengono esaminati il valore restituito e la matrice di argomenti di output.</span><span class="sxs-lookup"><span data-stu-id="eb760-127">If [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) returns success, this example examines the return value and the array of output arguments.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokeGetTrackInfo(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"GetTrackInfo");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 1;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            long rgIndices[1];
            VARIANT varTrackNum;

            rgIndices[0] = 0;
            VariantInit(&varTrackNum);

            varTrackNum.vt = VT_I4;
            // An arbitrary track is chosen (track 3)
            V_I4(&varTrackNum) = 3;

            hr = SafeArrayPutElement(psa,
                                     rgIndices,
                                     (void *) &varTrackNum);

            VariantClear(&varTrackNum);

            if (SUCCEEDED(hr))
            {            
                LONG    lStatus;
                VARIANT varInArgs;
                VARIANT varOutArgs;
                VARIANT varReturnVal;

                VariantInit(&varInArgs);
                VariantInit(&varOutArgs);
                VariantInit(&varReturnVal);

                varInArgs.vt = VT_VARIANT | VT_ARRAY;

                V_ARRAY(&varInArgs) = psa;

                hr = pService->InvokeAction(bstrActionName,
                                            varInArgs,
                                            &varOutArgs,
                                            &varReturnVal);

                if (SUCCEEDED(hr))
                {
                    SAFEARRAY * psaOutArgs = NULL;
                    VARIANT   varTrackTitle;

                    psaOutArgs = V_ARRAY(&varOutArgs);
                    VariantInit(&varTrackTitle);

                    rgIndices[0] = 0;
                    hr = SafeArrayGetElement(psaOutArgs,
                                             rgIndices,
                                             (void *)&varTrackTitle);                    

                    if (SUCCEEDED(hr))
                    {                    
                        wcout << L"Action invoked successfully\n"
                              << L"\tTrack Length == " 
                              << V_I4(&varReturnVal) << L"\n"
                              << L"\tTrack Title == " 
                              << V_BSTR(&varTrackTitle) << L"\n";
                    }
                    else
                    {
                        wcerr << L"Failed to get array element -"
                              << L" HRESULT 0x" 
                              << setbase(16)
                              << hr << L"\n";                        
                    }

                    VariantClear(&varTrackTitle);
                    VariantClear(&varReturnVal);
                    VariantClear(&varOutArgs);
                }
                else
                {
                    wcerr << L"Failed to invoke action - HRESULT 0x" 
                          << setbase(16)
                          << hr << L"\n";                        
                }                                   
            }
            else
            {
                wcerr << L"Failed to insert argument into array - "
                      << L"HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        
            }

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



 

 