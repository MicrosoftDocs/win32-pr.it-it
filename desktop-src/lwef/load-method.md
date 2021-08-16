---
title: Metodo Load
description: Metodo Load
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e201053bf3eb9fbd7a3c5c7eb94f9b032cde13087f76e1fcfa176d068655137a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748653"
---
# <a name="load-method"></a>Metodo Load

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Carica un carattere nella [**raccolta Characters.**](/windows/desktop/lwef/the-characters-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Characters.Load "**_CharacterID_*_",_ *  *Provider*



| Parte          | Descrizione                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Obbligatorio. Valore stringa che verrà utilizzato per fare riferimento ai dati di tipo carattere da caricare.                                                                                                                                                  |
| *Provider*    | Obbligatorio. Tipo di dati variant che deve essere uno dei seguenti: **Filespec** Percorso del file locale del file di definizione del carattere specificato. <br/> **URL** Indirizzo HTTP per il file di definizione del carattere.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile caricare caratteri dalla sottodirectory Agent specificando un percorso relativo(uno che non include due punti o una barra iniziale). Questo antefissi il percorso con la directory dei caratteri di Agent (che si trova nella directory Windows \\ msagent). Ad esempio, se si specifica quanto segue, viene caricato Il file Genie.acs dalla directory Chars dell'agente:


```
   Agent.Character.Load "genie", "genie.acs"
```



È anche possibile specificare la propria directory nella directory Chars di Agent.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



È possibile caricare il carattere attualmente impostato come carattere predefinito dell'utente corrente non includendo un percorso come secondo parametro del **metodo Load.**


```
   Agent.Character.Load "character"
```



Non è possibile caricare più volte lo stesso carattere (un carattere con lo stesso GUID) da una singola istanza del controllo. Analogamente, non è possibile caricare il carattere predefinito e altri caratteri contemporaneamente da una singola istanza del controllo perché il carattere predefinito potrebbe essere lo stesso dell'altro carattere. Se si tenta di eseguire questa operazione, il server genera un errore. Tuttavia, è possibile creare un'altra istanza del controllo Agent e caricare lo stesso carattere.

Microsoft Agent provider di dati il caricamento di dati di tipo carattere archiviati come singolo file strutturato (. ACS) con dati di tipo carattere e dati di animazione insieme o come dati di tipo carattere separati (. ACF) e animazione (. ACA). Usare il singolo oggetto strutturato . File ACS per caricare un carattere archiviato in un disco locale o in una rete e accessibile tramite un protocollo di file convenzionale,ad esempio i nomi di percorso UNC. Usare l'oggetto separato . ACF e . File ACA quando si desidera caricare i file di animazione singolarmente da un sito remoto a cui si accede tramite il protocollo HTTP.

Per. I file ACS, usando **il metodo Load,** forniscono l'accesso alle animazioni di un carattere. Per. File ACF, si usa anche il [**metodo Get per**](get-method.md) caricare i dati dell'animazione. Il **metodo Load** non supporta il download di . File ACS da un sito HTTP.

Il caricamento di un carattere non visualizza automaticamente il carattere. Usare prima [**il metodo Show**](show-method.md) per rendere visibile il carattere.

Se si usa il **metodo Load** per caricare un file di caratteri archiviato nel computer locale e la chiamata ha esito negativo; Ad esempio, poiché il file non viene trovato, Agent genera un errore. È possibile usare il supporto nel linguaggio di programmazione per fornire una routine di gestione degli errori per intercettare ed elaborare l'errore.


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



È anche possibile gestire l'errore impostando [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) su **False**, dichiarando un oggetto e assegnando la richiesta **Load.** Seguire quindi la **chiamata Load** con un'istruzione che controlla lo stato [**dell'oggetto**](/windows/desktop/lwef/the-request-object) Request.


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



Se si carica un carattere non locale; Ad esempio, usando il protocollo HTTP, è anche possibile verificare la presenza di un errore **di** caricamento assegnando un [**oggetto Request**](/windows/desktop/lwef/the-request-object) al **metodo Load.** Tuttavia, poiché questo metodo di caricamento di un carattere viene gestito in modo asincrono, controllarne lo stato [**nell'evento RequestComplete.**](requestcomplete-event.md) Questa tecnica non funziona caricando un carattere usando il protocollo UNC perché il **metodo Load** viene elaborato in modo sincrono.

 

