---
title: Richiamo di azioni
description: Il metodo InvokeAction IUPnPService consente di richiamare azioni sugli oggetti service.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7b294d7f0ed80988e9d4a9f75393764fd0a58b20d84581ab9ab10677efc6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137204"
---
# <a name="invoking-actions"></a>Richiamo di azioni

Il [**metodo IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) consente di richiamare azioni sugli oggetti Service. Questo metodo ha due parametri di input: il nome di un'azione e una matrice di argomenti di input per tale azione. Il metodo ha due parametri:

-   Parametro 1: parametro di input/output: matrice di argomenti di output per l'azione.
-   Parametro due: un parametro di output: un valore restituito.

Il metodo fa in modo che l'azione sia richiamata nel dispositivo. Il dispositivo genera notifiche degli eventi se l'azione causa la modifica delle variabili di stato del dispositivo.

## <a name="vbscript-example"></a>Esempio di VBScript

Nell'esempio di codice VBScript seguente vengono richiamate due azioni su un oggetto Service. La prima azione, *GetTrackInfo,* accetta un argomento di input, un numero di traccia. *L'azione GetTrackInfo* restituisce la lunghezza della traccia come valore restituito. L'azione ha anche un argomento di output, che contiene il titolo della traccia se il metodo restituisce l'esito positivo.

Dopo aver richiamato *l'azione GetTrackInfo,* l'esempio richiama l'azione Play, che non accetta argomenti. Tuttavia, poiché la sintassi di [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) richiede una matrice di argomenti sia di input che di output, l'esempio deve creare una matrice vuota, *emptyArgs,* senza elementi. Nell'esempio questa matrice viene passata **a InvokeAction** per gli argomenti di input e output, insieme al nome dell'azione.


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



## <a name="c-example"></a>Esempio C++

L'esempio seguente definisce una funzione C++ che richiama un'azione senza argomenti. Poiché [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) richiede che [**sia passato un SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di argomenti, in questo esempio viene creato un oggetto **SAFEARRAY vuoto.** Poiché questa azione non restituisce un valore o dispone di argomenti di output, in questo esempio vengono ignorati gli ultimi due valori [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) passati a **InvokeAction.**

Il dispositivo genera notifiche degli eventi se l'azione causa la modifica delle variabili di stato del dispositivo.


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



L'esempio seguente richiama l'azione *GetTrackInfo* fittizia. Accetta un numero di traccia come argomento, restituisce la lunghezza della traccia come valore restituito e restituisce il titolo della traccia in un argomento di output. Il codice è simile all'esempio precedente, ad eccezione del fatto che invece di creare un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) vuoto di argomenti di input, questo esempio inserisce un elemento [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) che contiene il numero di traccia. Se [**InvokeAction restituisce**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) un esito positivo, questo esempio esamina il valore restituito e la matrice di argomenti di output.


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



 

 