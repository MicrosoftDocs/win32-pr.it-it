---
description: In alcuni casi, si verifica una situazione in cui un messaggio non può essere recapitato correttamente alla destinazione prevista, in genere a causa di un problema con il sistema o la configurazione.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Gestione degli errori nei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523873"
---
# <a name="handling-errors-in-queued-components"></a>Gestione degli errori nei componenti in coda

In alcuni casi, si verifica una situazione in cui un messaggio non può essere recapitato correttamente alla destinazione prevista, in genere a causa di un problema con il sistema o la configurazione. Ad esempio, il messaggio potrebbe essere indirizzato a una coda che non esiste o la coda di destinazione potrebbe non trovarsi in uno stato da ricevere. Il motore messaggi è uno strumento che sposta tutti i messaggi di [Accodamento](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messaggi non riusciti da una coda a un'altra, in modo che possano essere ripetuti. L'utilità del Mover del messaggio è un oggetto di automazione che può essere richiamato con un VBScript.

## <a name="components-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Nell'esempio di codice seguente viene illustrato come creare un oggetto MessageMover, impostare le proprietà obbligatorie e avviare il trasferimento. Per usarlo da Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.

> [!Note]  
> Per utilizzare l'oggetto MessageMover, è necessario che nel computer sia installato Accodamento messaggi e che nell'applicazione specificata da AppName sia abilitato l'accodamento. Per informazioni sull'installazione di Accodamento messaggi, vedere Guida e supporto tecnico nel menu **Start** .

 


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



Nel codice di Visual Basic seguente viene illustrato come chiamare la funzione MyMessageMover.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



Il percorso di origine del messaggio è la coda di riposo finale. Si tratta della coda di messaggi non recapitabili, ovvero una coda di Accodamento messaggi privata e denominata AppName \_ deadqueue. I messaggi vengono spostati qui se la transazione si interrompe ripetutamente quando viene eseguito un tentativo nella quinta coda di tentativi. Con lo strumento Message Mover è possibile spostare nuovamente il messaggio nella prima coda, denominata AppName. Per ulteriori informazioni sulle code di tentativi, vedere [errori sul lato server](server-side-errors.md).

Se gli attributi della coda consentono, il Mover del messaggio Sposta i messaggi in modo transitivo in modo che i messaggi non vengano persi o duplicati in caso di errore durante lo spostamento. Lo strumento mantiene tutte le proprietà del messaggio che possono essere mantenute durante lo trasferimento di messaggi da una coda a un'altra.

Se i messaggi vengono generati dalle chiamate ai componenti in coda COM+, l'utilità di gestione dei messaggi conserva l'identificatore di sicurezza del chiamante originale mentre sposta i messaggi tra le code. Se entrambe le code di origine e di destinazione sono transazionali, l'intera operazione viene eseguita in modo transitivo. Se le code di origine o di destinazione non sono transazionali, l'operazione non viene eseguita in una transazione. Un errore imprevisto, ad esempio un arresto anomalo del sistema, e il riavvio di uno spostamento non transazionale potrebbero duplicare il messaggio spostato al momento dell'errore.

## <a name="cc"></a>C/C++

Nell'esempio di codice seguente viene illustrato come creare un oggetto MessageMover, impostare le proprietà obbligatorie e avviare il trasferimento. Il metodo ErrorDescription è descritto in [interpretazione dei codici di errore](interpreting-error-codes.md).

> [!Note]  
> Per utilizzare l'oggetto MessageMover, è necessario che nel computer sia installato Accodamento messaggi e che nell'applicazione specificata da AppName sia abilitato l'accodamento. Per informazioni sull'installazione di Accodamento messaggi, vedere Guida e supporto tecnico nel menu **Start** .

 


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



Nel codice C++ riportato di seguito viene illustrato come chiamare la funzione MyMessageMover.


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



Il percorso di origine del messaggio è la coda di riposo finale. Si tratta della coda di messaggi non recapitabili, ovvero una coda di Accodamento messaggi privata e denominata AppName \_ deadqueue. I messaggi vengono spostati qui se la transazione si interrompe ripetutamente quando viene eseguito un tentativo nella quinta coda di tentativi. Con lo strumento Message Mover è possibile spostare nuovamente il messaggio nella prima coda, denominata AppName. Per ulteriori informazioni sulle code di tentativi, vedere [errori sul lato server](server-side-errors.md).

Se gli attributi della coda consentono, il Mover del messaggio Sposta i messaggi in modo transitivo in modo che i messaggi non vengano persi o duplicati in caso di errore durante lo spostamento. Lo strumento mantiene tutte le proprietà del messaggio che possono essere mantenute durante lo trasferimento di messaggi da una coda a un'altra.

Se i messaggi vengono generati dalle chiamate ai componenti in coda COM+, l'utilità di gestione dei messaggi conserva l'identificatore di sicurezza del chiamante originale mentre sposta i messaggi tra le code. Se entrambe le code di origine e di destinazione sono transazionali, l'intera operazione viene eseguita in modo transitivo. Se le code di origine o di destinazione non sono transazionali, l'operazione non viene eseguita in una transazione. Un errore imprevisto, ad esempio un arresto anomalo del sistema, e il riavvio di uno spostamento non transazionale potrebbero duplicare il messaggio spostato al momento dell'errore.

## <a name="remarks"></a>Commenti

COM+ gestisce le interruzioni del lato server (lettore) spostando il messaggio che non riesce in una coda di "riposo finale" diversa, per ottenere la soluzione. Il listener e il lettore non possono eseguire continuamente il ciclo in un messaggio che viene interrotto. In molti casi, è possibile correggere la transazione interrotta intervenendo sul server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori dei componenti in coda](queued-components-errors.md)
</dt> </dl>

 

 



