---
description: Come per tutte le applicazioni, WMI riceve i codici di errore dal Windows sistema operativo.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Recupero di un codice di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16bb7af3c5c2b17d3a99ac00c9122a2ddfa6c075f463819e182fe44193613a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640631"
---
# <a name="retrieving-an-error-code"></a>Recupero di un codice di errore

Come per tutte le applicazioni, WMI riceve i codici di errore dal Windows sistema operativo.

Quando si riceve un codice di errore, sono disponibili le opzioni seguenti:

-   Esaminare il registro eventi.

    WMI invia messaggi di errore al servizio Registro eventi che controlla i log eventi per determinare la causa di un errore. È possibile usare le classi supportate dal provider [di log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) eventi per accedere ai log eventi a livello di codice.

-   Recuperare normalmente il codice di errore.

    WMI supporta le tecniche standard per recuperare i codici di errore, ovvero i codici di errore COM per C++, e gli oggetti errore nativi, ad esempio [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))o [**SWbemLastError**](swbemlasterror.md) se il provider fornisce informazioni sull'errore.

Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md).

In questo argomento vengono illustrate le sezioni seguenti:

-   [Gestione di un errore con VBScript](#handling-an-error-with-vbscript)
-   [Gestione di un errore con C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Gestione di un errore con VBScript

Se una chiamata a WMI tramite l'API di scripting per WMI causa un errore, sono disponibili le opzioni seguenti per accedere alle informazioni sull'errore:

-   Usare meccanismi di errore nativi del linguaggio di scripting, ad esempio in VBScript usare [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) per supportare la gestione degli errori.
-   Creare un [**oggetto SWbemLastError**](swbemlasterror.md) per ottenere una segnalazione errori.

Lo script seguente illustra l'uso [dell'oggetto Err nativo (VBScript).](/previous-versions//sbf5ze0e(v=vs.85)) Quando viene specificato un valore non corretto per l'handle di processo, viene generato un errore.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> La **proprietà Description** di [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) è vuota quando ci si connette a WMI tramite il moniker "winmgmts:". Tuttavia, se ci si connette usando [**SWbemLocator,**](swbemlocator.md)la descrizione è disponibile.
>
> Nella tabella seguente sono elencate le proprietà [di Err Object (VBScript).](/previous-versions//sbf5ze0e(v=vs.85))
>
> 
>
> | Proprietà                   | Contiene                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Descrizione**<br/> | Descrizione localizzata e leggibile dell'errore.<br/> |
> | **Number**<br/>      | **HRESULT restituito** dall'API scripting per WMI.<br/>  |
> | **Origine**<br/>      | Identifica l'oggetto che ha generato l'errore.<br/>        |
>
> 
>
>  

 

Lo script seguente illustra l'uso di [**un oggetto SWbemLastError**](swbemlasterror.md) per ottenere informazioni dettagliate sull'errore. Si noti che non tutti i provider forniscono informazioni **a SWbemLastError**. Per altre informazioni sui codici di errore nello script, vedere [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Gestione di un errore con C++

Un'applicazione client WMI può ricevere errori specifici di COM o WMI. Gli errori COM sono conformi alla struttura dei codici di errore COM. Tutte le interfacce WMI possono restituire un errore specifico di COM, ad eccezione delle interfacce [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)e [**IWbemQualifierSet.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) Per altre informazioni sui codici di errore COM, vedere [Gestione degli errori](../com/error-handling-in-com.md). Le pagine di riferimento delle interfacce WMI elencano i codici di errore WMI appropriati nella sezione Codici di errore.

Un'applicazione client deve seguire gli standard COM per controllare lo stato e i codici restituiti degli errori. La differenza principale da scegliere è se recuperare il codice di errore da una chiamata sincrona, semisincrona o asincrona.

**Per accedere ai messaggi di errore sincroni e semisincroni usando C++**

1.  Recuperare le informazioni sull'errore con una chiamata alla funzione COM [GetErrorInfo.]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo)

    Assicurarsi di chiamare [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediatamente dopo che un metodo di interfaccia indica un errore. Sono inclusi i metodi [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) che si chiamano durante l'elaborazione di un processo semisincrono.

2.  Esaminare l'oggetto errore COM restituito con una chiamata al [**metodo IErrorInterface::QueryInterface.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

    Assicurarsi di specificare IID \_ WbemClassObject per il *parametro riid* nella [**chiamata QueryInterface.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Il **metodo QueryInterface** restituisce un'istanza di una classe WMI, in genere [**\_ \_ ExtendedStatus**](--extendedstatus.md).

WMI non recapita l'oggetto errore tramite [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) per una chiamata asincrona perché non è possibile sapere quando o su quale thread si è verificata la chiamata asincrona. Pertanto, il codice può gestire solo errori specifici o passare l'errore di chiamata tramite COM.

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile usare la comunicazione semisincrona anziché asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

**Per accedere ai messaggi di errore asincroni tramite C++**

-   Recuperare l'oggetto errore COM dall'implementazione di [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).

    Lo pseudocodice seguente illustra un'implementazione tipica della gestione degli errori per un'applicazione client.

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

