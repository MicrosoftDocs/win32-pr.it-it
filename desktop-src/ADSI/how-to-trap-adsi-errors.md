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
# <a name="how-to-trap-adsi-errors"></a>Come intercettare gli errori ADSI

VBScript offre solo un modo per intercettare gli errori: gestione degli errori inline. Un gestore degli errori inline inizia con l'istruzione **On Error Resume Next** . Poiché **in seguito alla ripresa** degli errori, non sarà più possibile arrestare l'esecuzione dello script fino alla fine dell'ambito da cui viene chiamato il metodo in caso di errore di ripresa **successiva** , è necessario controllare il valore di **Err** in ogni punto dopo l'istruzione **On Error Resume Next** in cui si prevede che si verifichi un errore. Nell'esempio seguente viene illustrata la gestione degli errori inline in uno script ADSI:


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



Dopo ogni posizione in cui è probabile che lo script riscontri un errore, è presente un'istruzione **If Err** . L'oggetto **Err** contiene il codice di errore dell'ultimo errore che si è verificato durante l'esecuzione dello script. Se non si è verificato alcun errore, **Err** sarà sempre zero (0). Nell'esempio precedente, un errore provocherà il passaggio dell'esecuzione alla subroutine **AdsiErr** , che verifica il valore di **Err. Number** per gli errori previsti. Invece di morire con un messaggio di errore enigmatico, lo script fornirà una spiegazione piuttosto migliore per il motivo per cui l'esecuzione è stata arrestata.

Tenere presente che all'interno dell'ambito in cui viene chiamato il metodo in caso di **errore Resume Next** , eventuali errori che si verificano dopo la chiamata **a On Error Resume Next** verranno ignorati. In questo modo è possibile eseguire il debug di uno script se si dimentica di controllare il valore di **Err** in posizioni appropriate. Quando si prevede che un errore sia probabilmente, assicurarsi di controllare il valore di **Err**.

Quando si esegue il debug iniziale dello script, è possibile che si desideri semplicemente interrompere l'esecuzione dello script e visualizzare il numero di riga che ha causato l'errore, quindi aggiungere i gestori degli errori dopo la correttezza del flusso di programma di base.

 

 




