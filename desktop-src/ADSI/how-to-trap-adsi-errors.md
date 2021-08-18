---
title: Come intercettare gli errori ADSI
description: VBScript offre solo un modo per intercettare gli errori nella gestione degli errori inline.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd66283d2427c2c42162ce46a0a66ecbda87737cf2572d183ebdb0017232e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082535"
---
# <a name="how-to-trap-adsi-errors"></a>Come intercettare gli errori ADSI

VBScript offre solo un modo per intercettare gli errori: gestione degli errori inline. Un gestore degli errori inline inizia con **l'istruzione On Error Resume Next.** Poiché  In caso di errore Riprendi successivo impedirà a eventuali errori di arrestare l'esecuzione dello script fino alla fine dell'ambito da cui viene chiamato On **Error Resume Next,** è necessario controllare il valore di **Err** in ogni punto dopo l'istruzione On **Error Resume Next** in cui si prevede che si verifichi un errore. L'esempio seguente illustra la gestione degli errori inline in uno script ADSI:


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



Dopo ogni posizione in cui è probabile che si verifichi un errore nello script, è presente **un'istruzione If Err.** **L'oggetto Err** contiene il codice di errore dell'ultimo errore che si è verificato durante l'esecuzione dello script. Se non si è verificato alcun errore, **Err** sarà sempre zero (0). Nell'esempio precedente, un errore causerà il passaggio dell'esecuzione alla subroutine **AdsiErr,** che controlla il valore di **Err.Number** per gli errori previsti. Invece di usare un messaggio di errore criptico, lo script offrirà una spiegazione più dettagliata del motivo per cui l'esecuzione è stata interrotta.

Tenere presente che all'interno dell'ambito in cui viene chiamato On **Error Resume Next,** qualsiasi errore che si verifica dopo la chiamata On **Error Resume Next** verrà ignorato. Ciò può rendere più difficile il debug di uno script se si dimentica di controllare il valore **di Err** nelle posizioni appropriate. Ogni volta che si prevede che un errore sia probabile, assicurarsi di controllare il valore di **Err**.

Quando si esegue inizialmente il debug dello script, è possibile consentire semplicemente allo script di interrompere l'esecuzione e visualizzare il numero di riga che ha generato l'errore in caso di errore, quindi aggiungere i gestori degli errori dopo che il flusso di base del programma è corretto.

 

 




