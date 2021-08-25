---
description: In alcuni casi, si verifica una situazione in cui un messaggio non può essere recapitato correttamente alla destinazione desiderata, in genere a causa di un problema con il sistema o la configurazione.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Gestione degli errori nei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314ff367e656043746bb34bcb28b6c5a3dc8db9b86b58a482af45f684fb658c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991081"
---
# <a name="handling-errors-in-queued-components"></a>Gestione degli errori nei componenti in coda

In alcuni casi, si verifica una situazione in cui un messaggio non può essere recapitato correttamente alla destinazione desiderata, in genere a causa di un problema con il sistema o la configurazione. Ad esempio, il messaggio potrebbe essere indirizzato a una coda inesistente o la coda di destinazione potrebbe non essere in uno stato da ricevere. Lo strumento di spostamento messaggi è uno strumento che sposta tutti i messaggi di [Accodamento](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messaggi non riusciti da una coda a un'altra in modo che possano essere ritentati. L'utilità di spostamento dei messaggi è un oggetto di Automazione che può essere richiamato con vbscript.

## <a name="components-services-administrative-tool"></a>Strumento amministrativo servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Il codice di esempio seguente illustra come creare un oggetto MessageMover, impostare le proprietà necessarie e avviare il trasferimento. Per usarlo da Visual Basic, aggiungere un riferimento alla libreria dei tipi dei servizi COM+.

> [!Note]  
> Per usare l'oggetto MessageMover, è necessario che Nel computer sia installato Accodamento messaggi e che l'applicazione specificata da AppName sia abilitata per l'accodamento. Per informazioni sull'installazione di Accodamento messaggi, vedere Guida e supporto tecnico nel menu **Start.**

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



Il codice Visual Basic seguente illustra come chiamare la funzione MyMessageMover.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



Il percorso di origine del messaggio è la coda di attesa finale. Si tratta della coda non attiva, ovvero una coda privata di Accodamento messaggi e denominata coda non attiva \_ AppName. I messaggi vengono spostati qui se la transazione viene interrotta ripetutamente quando viene tentata la quinta coda di tentativi. Con lo strumento di spostamento dei messaggi, è possibile spostare il messaggio di nuovo nella prima coda, denominata AppName. Per altre informazioni sulle code di ripetizione dei tentativi, vedere [Errori sul lato server](server-side-errors.md).

Se gli attributi della coda lo consentono, lo spostamento dei messaggi sposta i messaggi in modo che non siano persi o duplicati in caso di errore durante lo spostamento. Lo strumento mantiene tutte le proprietà dei messaggi che possono essere mantenute quando si spostano messaggi da una coda a un'altra.

Se i messaggi vengono generati da chiamate ai componenti in coda COM+, l'utilità di spostamento messaggi mantiene l'identificatore di sicurezza del chiamante originale mentre sposta i messaggi tra le code. Se le code di destinazione e di origine sono transazionali, l'intera operazione viene eseguita in modo transizione. Se le code di origine o di destinazione non sono transazionali, l'operazione non viene eseguita in una transazione. Un errore imprevisto , ad esempio un arresto anomalo del sistema, e il riavvio di uno spostamento non transazionale potrebbero duplicare il messaggio spostato al momento dell'errore.

## <a name="cc"></a>C/C++

Il codice di esempio seguente illustra come creare un oggetto MessageMover, impostare le proprietà necessarie e avviare il trasferimento. Il metodo ErrorDescription è descritto in [Interpretazione dei codici di errore](interpreting-error-codes.md).

> [!Note]  
> Per usare l'oggetto MessageMover, è necessario che Nel computer sia installato Accodamento messaggi e che l'applicazione specificata da AppName sia abilitata per l'accodamento. Per informazioni sull'installazione di Accodamento messaggi, vedere Guida e supporto tecnico nel menu **Start.**

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



Il codice C++ seguente illustra come chiamare la funzione MyMessageMover.


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



Il percorso di origine del messaggio è la coda di attesa finale. Si tratta della coda non attiva, ovvero una coda privata di Accodamento messaggi e denominata coda non attiva \_ AppName. I messaggi vengono spostati qui se la transazione viene interrotta ripetutamente quando viene tentata la quinta coda di tentativi. Con lo strumento di spostamento dei messaggi, è possibile spostare il messaggio di nuovo nella prima coda, denominata AppName. Per altre informazioni sulle code di ripetizione dei tentativi, vedere [Errori sul lato server](server-side-errors.md).

Se gli attributi della coda lo consentono, lo spostamento dei messaggi sposta i messaggi in modo che non siano persi o duplicati in caso di errore durante lo spostamento. Lo strumento mantiene tutte le proprietà dei messaggi che possono essere mantenute quando si spostano messaggi da una coda a un'altra.

Se i messaggi vengono generati da chiamate ai componenti in coda COM+, l'utilità di spostamento messaggi mantiene l'identificatore di sicurezza del chiamante originale mentre sposta i messaggi tra le code. Se le code di destinazione e di origine sono transazionali, l'intera operazione viene eseguita in modo transizione. Se le code di origine o di destinazione non sono transazionali, l'operazione non viene eseguita in una transazione. Un errore imprevisto , ad esempio un arresto anomalo del sistema, e il riavvio di uno spostamento non transazionale potrebbero duplicare il messaggio spostato al momento dell'errore.

## <a name="remarks"></a>Commenti

COM+ gestisce le interruzioni sul lato server (lettore) spostando il messaggio che ha esito negativo in un'altra coda di "riposo finale", per uscire dal gioco. Il listener e il lettore non possono continuare a eseguire il ciclo su un messaggio che viene interrotto. In molti casi, la transazione interrotta può essere corretta tramite l'esecuzione di un'azione nel server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori dei componenti in coda](queued-components-errors.md)
</dt> </dl>

 

 



