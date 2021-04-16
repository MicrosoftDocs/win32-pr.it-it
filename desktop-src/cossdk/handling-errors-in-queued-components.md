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
# <a name="handling-errors-in-queued-components"></a><span data-ttu-id="07bb1-103">Gestione degli errori nei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="07bb1-103">Handling Errors in Queued Components</span></span>

<span data-ttu-id="07bb1-104">In alcuni casi, si verifica una situazione in cui un messaggio non può essere recapitato correttamente alla destinazione prevista, in genere a causa di un problema con il sistema o la configurazione.</span><span class="sxs-lookup"><span data-stu-id="07bb1-104">Occasionally, a situation occurs in which a message cannot be successfully delivered to its intended destination, usually due to a problem with the system or configuration.</span></span> <span data-ttu-id="07bb1-105">Ad esempio, il messaggio potrebbe essere indirizzato a una coda che non esiste o la coda di destinazione potrebbe non trovarsi in uno stato da ricevere.</span><span class="sxs-lookup"><span data-stu-id="07bb1-105">For example, the message might be directed to a queue that does not exist or the destination queue might not be in a state to receive.</span></span> <span data-ttu-id="07bb1-106">Il motore messaggi è uno strumento che sposta tutti i messaggi di [Accodamento](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messaggi non riusciti da una coda a un'altra, in modo che possano essere ripetuti.</span><span class="sxs-lookup"><span data-stu-id="07bb1-106">The message mover is a tool that moves all failed [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="07bb1-107">L'utilità del Mover del messaggio è un oggetto di automazione che può essere richiamato con un VBScript.</span><span class="sxs-lookup"><span data-stu-id="07bb1-107">The message mover utility is an Automation object that can be invoked with a VBScript.</span></span>

## <a name="components-services-administrative-tool"></a><span data-ttu-id="07bb1-108">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="07bb1-108">Components Services Administrative Tool</span></span>

<span data-ttu-id="07bb1-109">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="07bb1-109">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="07bb1-110">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="07bb1-110">Visual Basic</span></span>

<span data-ttu-id="07bb1-111">Nell'esempio di codice seguente viene illustrato come creare un oggetto MessageMover, impostare le proprietà obbligatorie e avviare il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="07bb1-111">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="07bb1-112">Per usarlo da Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="07bb1-112">To use it from Visual Basic, add a reference to the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="07bb1-113">Per utilizzare l'oggetto MessageMover, è necessario che nel computer sia installato Accodamento messaggi e che nell'applicazione specificata da AppName sia abilitato l'accodamento.</span><span class="sxs-lookup"><span data-stu-id="07bb1-113">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="07bb1-114">Per informazioni sull'installazione di Accodamento messaggi, vedere Guida e supporto tecnico nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="07bb1-114">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


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



<span data-ttu-id="07bb1-115">Nel codice di Visual Basic seguente viene illustrato come chiamare la funzione MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="07bb1-115">The following Visual Basic code shows how to call the MyMessageMover function.</span></span>


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



<span data-ttu-id="07bb1-116">Il percorso di origine del messaggio è la coda di riposo finale.</span><span class="sxs-lookup"><span data-stu-id="07bb1-116">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="07bb1-117">Si tratta della coda di messaggi non recapitabili, ovvero una coda di Accodamento messaggi privata e denominata AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="07bb1-117">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="07bb1-118">I messaggi vengono spostati qui se la transazione si interrompe ripetutamente quando viene eseguito un tentativo nella quinta coda di tentativi.</span><span class="sxs-lookup"><span data-stu-id="07bb1-118">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="07bb1-119">Con lo strumento Message Mover è possibile spostare nuovamente il messaggio nella prima coda, denominata AppName.</span><span class="sxs-lookup"><span data-stu-id="07bb1-119">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="07bb1-120">Per ulteriori informazioni sulle code di tentativi, vedere [errori sul lato server](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="07bb1-120">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="07bb1-121">Se gli attributi della coda consentono, il Mover del messaggio Sposta i messaggi in modo transitivo in modo che i messaggi non vengano persi o duplicati in caso di errore durante lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="07bb1-121">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="07bb1-122">Lo strumento mantiene tutte le proprietà del messaggio che possono essere mantenute durante lo trasferimento di messaggi da una coda a un'altra.</span><span class="sxs-lookup"><span data-stu-id="07bb1-122">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="07bb1-123">Se i messaggi vengono generati dalle chiamate ai componenti in coda COM+, l'utilità di gestione dei messaggi conserva l'identificatore di sicurezza del chiamante originale mentre sposta i messaggi tra le code.</span><span class="sxs-lookup"><span data-stu-id="07bb1-123">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="07bb1-124">Se entrambe le code di origine e di destinazione sono transazionali, l'intera operazione viene eseguita in modo transitivo.</span><span class="sxs-lookup"><span data-stu-id="07bb1-124">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="07bb1-125">Se le code di origine o di destinazione non sono transazionali, l'operazione non viene eseguita in una transazione.</span><span class="sxs-lookup"><span data-stu-id="07bb1-125">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="07bb1-126">Un errore imprevisto, ad esempio un arresto anomalo del sistema, e il riavvio di uno spostamento non transazionale potrebbero duplicare il messaggio spostato al momento dell'errore.</span><span class="sxs-lookup"><span data-stu-id="07bb1-126">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="cc"></a><span data-ttu-id="07bb1-127">C/C++</span><span class="sxs-lookup"><span data-stu-id="07bb1-127">C/C++</span></span>

<span data-ttu-id="07bb1-128">Nell'esempio di codice seguente viene illustrato come creare un oggetto MessageMover, impostare le proprietà obbligatorie e avviare il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="07bb1-128">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="07bb1-129">Il metodo ErrorDescription è descritto in [interpretazione dei codici di errore](interpreting-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="07bb1-129">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="07bb1-130">Per utilizzare l'oggetto MessageMover, è necessario che nel computer sia installato Accodamento messaggi e che nell'applicazione specificata da AppName sia abilitato l'accodamento.</span><span class="sxs-lookup"><span data-stu-id="07bb1-130">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="07bb1-131">Per informazioni sull'installazione di Accodamento messaggi, vedere Guida e supporto tecnico nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="07bb1-131">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


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



<span data-ttu-id="07bb1-132">Nel codice C++ riportato di seguito viene illustrato come chiamare la funzione MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="07bb1-132">The following C++ code shows how to call the MyMessageMover function.</span></span>


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



<span data-ttu-id="07bb1-133">Il percorso di origine del messaggio è la coda di riposo finale.</span><span class="sxs-lookup"><span data-stu-id="07bb1-133">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="07bb1-134">Si tratta della coda di messaggi non recapitabili, ovvero una coda di Accodamento messaggi privata e denominata AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="07bb1-134">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="07bb1-135">I messaggi vengono spostati qui se la transazione si interrompe ripetutamente quando viene eseguito un tentativo nella quinta coda di tentativi.</span><span class="sxs-lookup"><span data-stu-id="07bb1-135">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="07bb1-136">Con lo strumento Message Mover è possibile spostare nuovamente il messaggio nella prima coda, denominata AppName.</span><span class="sxs-lookup"><span data-stu-id="07bb1-136">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="07bb1-137">Per ulteriori informazioni sulle code di tentativi, vedere [errori sul lato server](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="07bb1-137">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="07bb1-138">Se gli attributi della coda consentono, il Mover del messaggio Sposta i messaggi in modo transitivo in modo che i messaggi non vengano persi o duplicati in caso di errore durante lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="07bb1-138">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="07bb1-139">Lo strumento mantiene tutte le proprietà del messaggio che possono essere mantenute durante lo trasferimento di messaggi da una coda a un'altra.</span><span class="sxs-lookup"><span data-stu-id="07bb1-139">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="07bb1-140">Se i messaggi vengono generati dalle chiamate ai componenti in coda COM+, l'utilità di gestione dei messaggi conserva l'identificatore di sicurezza del chiamante originale mentre sposta i messaggi tra le code.</span><span class="sxs-lookup"><span data-stu-id="07bb1-140">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="07bb1-141">Se entrambe le code di origine e di destinazione sono transazionali, l'intera operazione viene eseguita in modo transitivo.</span><span class="sxs-lookup"><span data-stu-id="07bb1-141">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="07bb1-142">Se le code di origine o di destinazione non sono transazionali, l'operazione non viene eseguita in una transazione.</span><span class="sxs-lookup"><span data-stu-id="07bb1-142">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="07bb1-143">Un errore imprevisto, ad esempio un arresto anomalo del sistema, e il riavvio di uno spostamento non transazionale potrebbero duplicare il messaggio spostato al momento dell'errore.</span><span class="sxs-lookup"><span data-stu-id="07bb1-143">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="07bb1-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="07bb1-144">Remarks</span></span>

<span data-ttu-id="07bb1-145">COM+ gestisce le interruzioni del lato server (lettore) spostando il messaggio che non riesce in una coda di "riposo finale" diversa, per ottenere la soluzione.</span><span class="sxs-lookup"><span data-stu-id="07bb1-145">COM+ handles server-side (player) aborts by moving the message that is failing onto a different "final resting" queue, to get it out of the way.</span></span> <span data-ttu-id="07bb1-146">Il listener e il lettore non possono eseguire continuamente il ciclo in un messaggio che viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="07bb1-146">The listener and player cannot continually loop on a message that aborts.</span></span> <span data-ttu-id="07bb1-147">In molti casi, è possibile correggere la transazione interrotta intervenendo sul server.</span><span class="sxs-lookup"><span data-stu-id="07bb1-147">In many cases, the aborted transaction can be fixed by taking action at the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07bb1-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07bb1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07bb1-149">Errori dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="07bb1-149">Queued Components Errors</span></span>](queued-components-errors.md)
</dt> </dl>

 

 



