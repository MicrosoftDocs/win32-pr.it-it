---
title: Metodo Activate
description: Metodo Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5032c7c7f2faf7ec53028a0cc0ce55847fe300864bb531968fc8190b4e00d164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753160"
---
# <a name="activate-method"></a>Metodo Activate

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Descrizione**](../wmformat/description.md)
</dt> <dd>

Imposta il client o il carattere attivo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Stato_ *  \[ *di attivazione*\]



| Parte    | Descrizione                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | facoltativo. È possibile specificare i valori seguenti per questo parametro: 0 Non il client attivo.<br/> 1 Il client attivo. <br/> 2 (impostazione predefinita) Carattere in primo piano.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando sono visibili più caratteri, solo uno dei caratteri riceve l'input vocale alla volta. Analogamente, quando più applicazioni client condividono lo stesso carattere, solo uno dei client riceve l'input del mouse,ad esempio gli eventi di clic o trascinamento del controllo di Microsoft Agent. Il set di caratteri per ricevere l'input tramite mouse e voce è il carattere più in alto e il client che riceve l'input è il client attivo di tale carattere. La finestra del carattere più in alto viene visualizzata anche nella parte superiore dell'ordine z della finestra dei caratteri. In genere, l'utente determina il carattere in primo piano selezionando il carattere in modo esplicito. Tuttavia, l'attivazione in primo piano cambia anche quando un carattere viene visualizzato o nascosto (il carattere diventa o non è più in primo piano, rispettivamente).

È anche possibile usare questo metodo per gestire in modo esplicito quando il client riceve input indirizzato al carattere, ad esempio quando l'applicazione stessa diventa attiva. Ad esempio, se si imposta *Stato* su 2, il carattere viene visualizzato in primo piano e il client riceve tutti gli eventi di input del mouse e del riconoscimento vocale generati dall'interazione dell'utente con il carattere. Pertanto, rende anche il client il client attivo di input del carattere.

Tuttavia, è anche possibile impostare se stessi come client attivo per un carattere senza rendere il carattere in primo piano, impostando *Stato* su 1. In questo modo il client può ricevere l'input indirizzato a tale carattere quando il carattere diventa in primo piano. Analogamente, è possibile impostare il client in modo che non sia il client attivo (per non ricevere input) quando il carattere diventa in primo piano, impostando *Stato* su 0.

Evitare di chiamare questo metodo direttamente dopo un [**metodo Show.**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) **Mostra** imposta automaticamente il client attivo di input. Quando il carattere è nascosto, la [**chiamata Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) potrebbe non riuscire se viene elaborata prima del **completamento del** metodo Show.

Se si chiama questo metodo a una funzione, restituisce un valore booleano che indica se il metodo ha avuto esito positivo. Il tentativo di chiamare questo metodo con *il parametro State* impostato su 2 quando il carattere specificato è nascosto avrà esito negativo. Analogamente, se si imposta *State* su 0 e l'applicazione è l'unico client, questa chiamata non riesce perché un carattere deve avere sempre un client in primo piano.


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> La chiamata di questo metodo con *State* impostato su 1 in genere genera un evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) a meno che non siano stati caricati altri caratteri o che l'applicazione non sia già attiva per l'input.

 

## <a name="see-also"></a>Vedere anche

[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)


 

