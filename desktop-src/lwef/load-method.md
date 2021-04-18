---
title: Metodo Load
description: Metodo Load
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299699"
---
# <a name="load-method"></a>Metodo Load

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Carica un carattere nella raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Characters. Load "*** CharacterID * * *",* *  *provider*



| Parte          | Descrizione                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Obbligatorio. Valore stringa che verrà utilizzato per fare riferimento ai dati di tipo carattere da caricare.                                                                                                                                                  |
| *Provider*    | Obbligatorio. Tipo di dati Variant che deve essere uno dei seguenti: **filespec** il percorso del file locale del file di definizione del carattere specificato. <br/> **URL** di Indirizzo HTTP per il file di definizione del carattere.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile caricare caratteri dalla sottodirectory Agent specificando un percorso relativo (uno che non include i due punti o il carattere barra rovesciata). Questa operazione previene il prefisso del percorso con la directory characters di Agent, che si trova nella directory msagent di Windows localizzata \\ . Ad esempio, se si specifica quanto segue, viene caricato Genie. ACS dalla directory chars dell'agente:


```
   Agent.Character.Load "genie", "genie.acs"
```



È anche possibile specificare la propria directory nella directory chars dell'agente.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



È possibile caricare il carattere attualmente impostato come carattere predefinito dell'utente corrente senza includere un percorso come secondo parametro del metodo **Load** .


```
   Agent.Character.Load "character"
```



Non è possibile caricare più volte lo stesso carattere, ovvero un carattere con lo stesso GUID, da una singola istanza del controllo. Analogamente, non è possibile caricare contemporaneamente il carattere predefinito e altri caratteri da una singola istanza del controllo, poiché il carattere predefinito potrebbe essere uguale a quello dell'altro carattere. Se si tenta di eseguire questa operazione, il server genera un errore. Tuttavia, è possibile creare un'altra istanza del controllo agente e caricare lo stesso carattere.

Il provider di dati Microsoft Agent supporta il caricamento di dati di tipo carattere archiviati come singolo file strutturato (. ACS) con dati di tipo carattere e dati di animazione insieme o come dati di tipo carattere separati (. ACF) e animazione (. File ACA). Usare il singolo oggetto strutturato. File ACS per caricare un carattere archiviato in un disco locale o in una rete a cui si accede utilizzando un protocollo file convenzionale, ad esempio i percorsi UNC. Usare l'oggetto separato. ACF e. File ACA quando si desidera caricare i file di animazione singolarmente da un sito remoto a cui si accede utilizzando il protocollo HTTP.

Per. I file ACS, usando il metodo **Load** , consentono di accedere alle animazioni di un carattere. Per. File ACF, viene usato anche il metodo [**Get**](get-method.md) per caricare i dati dell'animazione. Il metodo **Load** non supporta il download. File ACS da un sito HTTP.

Il caricamento di un carattere non visualizza automaticamente il carattere. Usare prima il metodo [**show**](show-method.md) per rendere visibile il carattere.

Se si usa il metodo **Load** per caricare un file di caratteri archiviato nel computer locale e la chiamata ha esito negativo; ad esempio, poiché il file non viene trovato, Agent genera un errore. È possibile utilizzare il supporto nel linguaggio di programmazione per fornire una routine di gestione degli errori per intercettare ed elaborare l'errore.


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



È anche possibile gestire l'errore impostando [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) su **false**, dichiarando un oggetto e assegnando la richiesta di **caricamento** . Seguire quindi la chiamata di **caricamento** con un'istruzione che controlla lo stato dell'oggetto [**Request**](/windows/desktop/lwef/the-request-object) .


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



Se si carica un carattere non locale; Se ad esempio si usa il protocollo HTTP, è anche possibile verificare la presenza di un errore di **caricamento** assegnando un oggetto [**Request**](/windows/desktop/lwef/the-request-object) al metodo **Load** . Tuttavia, poiché questo metodo di caricamento di un carattere viene gestito in modo asincrono, verificarne lo stato nell'evento [**RequestComplete**](requestcomplete-event.md) . Questa tecnica non funzionerà il caricamento di un carattere usando il protocollo UNC perché il metodo **Load** viene elaborato in modo sincrono.

 

