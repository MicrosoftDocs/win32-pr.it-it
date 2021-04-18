---
title: Come intercettare gli errori ADSI
description: VBScript offre solo un modo per intercettare gli errori di gestione degli errori inline.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa36b3e9b1027e1733009d58a572a0b27c7ef0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297679"
---
# <a name="how-to-trap-adsi-errors"></a><span data-ttu-id="62020-103">Come intercettare gli errori ADSI</span><span class="sxs-lookup"><span data-stu-id="62020-103">How to Trap ADSI Errors</span></span>

<span data-ttu-id="62020-104">VBScript offre solo un modo per intercettare gli errori: gestione degli errori inline.</span><span class="sxs-lookup"><span data-stu-id="62020-104">VBScript only offers one way to trap errors: inline error handling.</span></span> <span data-ttu-id="62020-105">Un gestore degli errori inline inizia con l'istruzione **On Error Resume Next** .</span><span class="sxs-lookup"><span data-stu-id="62020-105">An inline error handler begins with the **On Error Resume Next** statement.</span></span> <span data-ttu-id="62020-106">Poiché **in seguito alla ripresa** degli errori, non sarà più possibile arrestare l'esecuzione dello script fino alla fine dell'ambito da cui viene chiamato il metodo in caso di errore di ripresa **successiva** , è necessario controllare il valore di **Err** in ogni punto dopo l'istruzione **On Error Resume Next** in cui si prevede che si verifichi un errore.</span><span class="sxs-lookup"><span data-stu-id="62020-106">Since **On Error Resume Next** will prevent any errors from stopping execution of the script until the end of the scope from which **On Error Resume Next** is called, you must check the value of **Err** at every point after the **On Error Resume Next** statement where you expect an error might occur.</span></span> <span data-ttu-id="62020-107">Nell'esempio seguente viene illustrata la gestione degli errori inline in uno script ADSI:</span><span class="sxs-lookup"><span data-stu-id="62020-107">The following example demonstrates inline error handling in an ADSI script:</span></span>


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



<span data-ttu-id="62020-108">Dopo ogni posizione in cui è probabile che lo script riscontri un errore, è presente un'istruzione **If Err** .</span><span class="sxs-lookup"><span data-stu-id="62020-108">After each location where the script is likely to encounter an error, there is an **If Err** statement.</span></span> <span data-ttu-id="62020-109">L'oggetto **Err** contiene il codice di errore dell'ultimo errore che si è verificato durante l'esecuzione dello script. Se non si è verificato alcun errore, **Err** sarà sempre zero (0).</span><span class="sxs-lookup"><span data-stu-id="62020-109">The **Err** object contains the error code of the last error that occurred during execution of the script; if no error has occurred, **Err** will always be zero (0).</span></span> <span data-ttu-id="62020-110">Nell'esempio precedente, un errore provocherà il passaggio dell'esecuzione alla subroutine **AdsiErr** , che verifica il valore di **Err. Number** per gli errori previsti.</span><span class="sxs-lookup"><span data-stu-id="62020-110">In the previous example, an error will cause execution to jump to the **AdsiErr** subroutine, which checks the value of **Err.Number** for expected errors.</span></span> <span data-ttu-id="62020-111">Invece di morire con un messaggio di errore enigmatico, lo script fornirà una spiegazione piuttosto migliore per il motivo per cui l'esecuzione è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="62020-111">Instead of dying with a cryptic error message, the script will give a somewhat better explanation for why it stopped running.</span></span>

<span data-ttu-id="62020-112">Tenere presente che all'interno dell'ambito in cui viene chiamato il metodo in caso di **errore Resume Next** , eventuali errori che si verificano dopo la chiamata **a On Error Resume Next** verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="62020-112">Remember that within the scope in which **On Error Resume Next** is called, any error that occurs after the **On Error Resume Next** call will be ignored.</span></span> <span data-ttu-id="62020-113">In questo modo è possibile eseguire il debug di uno script se si dimentica di controllare il valore di **Err** in posizioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="62020-113">This can actually make a script harder to debug if you forget to check the value of **Err** in appropriate locations.</span></span> <span data-ttu-id="62020-114">Quando si prevede che un errore sia probabilmente, assicurarsi di controllare il valore di **Err**.</span><span class="sxs-lookup"><span data-stu-id="62020-114">Wherever you expect an error to be likely, be sure to check the value of **Err**.</span></span>

<span data-ttu-id="62020-115">Quando si esegue il debug iniziale dello script, è possibile che si desideri semplicemente interrompere l'esecuzione dello script e visualizzare il numero di riga che ha causato l'errore, quindi aggiungere i gestori degli errori dopo la correttezza del flusso di programma di base.</span><span class="sxs-lookup"><span data-stu-id="62020-115">(When you are initially debugging the script you may want to simply let the script halt its execution and display the offending line number on an error, then add the error handlers after the basic program flow is correct.)</span></span>

 

 




