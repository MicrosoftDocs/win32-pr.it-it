---
title: Metodo Activate
description: Metodo Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299652"
---
# <a name="activate-method"></a>Metodo Activate

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Descrizione**](../wmformat/description.md)
</dt> <dd>

Imposta il client o il carattere attivo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Attiva* *  \[ *stato*\]



| Parte    | Descrizione                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | facoltativo. Per questo parametro è possibile specificare i valori seguenti: 0 non è il client attivo.<br/> 1 il client attivo. <br/> 2 (impostazione predefinita) carattere superiore.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando sono visibili più caratteri, solo uno dei caratteri riceve l'input vocale alla volta. Analogamente, quando più applicazioni client condividono lo stesso carattere, solo uno dei client riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft). Il set di caratteri per ricevere input da mouse e vocale è il carattere superiore e il client che riceve l'input è il client attivo di tale carattere. La finestra del carattere superiore viene visualizzata anche nella parte superiore dell'ordine z della finestra dei caratteri. In genere, l'utente determina il carattere superiore selezionando in modo esplicito il carattere. Tuttavia, l'attivazione in primo piano cambia anche quando un carattere viene visualizzato o nascosto (il carattere diventa o non è più in primo piano, rispettivamente).

È anche possibile usare questo metodo per gestire in modo esplicito quando il client riceve input indirizzato al carattere, ad esempio quando l'applicazione stessa diventa attiva. Se, ad esempio, si imposta *lo stato* su 2, il carattere è in primo piano e il client riceve tutti gli eventi di input del mouse e vocale generati dall'interazione dell'utente con il carattere. Quindi, rende il client anche il client di input-attivo del carattere.

Tuttavia, è anche possibile impostare se stessi come client attivo per un carattere senza rendere il carattere superiore, impostando *stato* su 1. Ciò consente al client di ricevere input indirizzato a tale carattere quando il carattere diventa più in alto. Analogamente, è possibile impostare il client su non come client attivo (non per ricevere input) quando il carattere diventa in primo piano, impostando *stato* su 0.

Evitare di chiamare questo metodo direttamente dopo un metodo [**show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) . **Mostra** imposta automaticamente il client attivo di input. Quando il carattere è nascosto, la chiamata [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) potrebbe non riuscire se viene elaborata prima del completamento del metodo **show** .

Se si chiama questo metodo in una funzione, viene restituito un valore booleano che indica se il metodo ha avuto esito positivo. Il tentativo di chiamare questo metodo con il parametro *state* impostato su 2 quando il carattere specificato è nascosto avrà esito negativo. Analogamente, se si imposta *lo stato* su 0 e l'applicazione è l'unico client, questa chiamata ha esito negativo perché un carattere deve avere sempre un client in primo piano.


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
> La chiamata a questo metodo con *stato* impostato su 1 in genere non genera un evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) a meno che non ci siano altri caratteri caricati o che l'applicazione sia già in input-Active.

 

## <a name="see-also"></a>Vedere anche

[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)


 

