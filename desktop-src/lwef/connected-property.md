---
title: Proprietà connessa
description: Proprietà connessa
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331087"
---
# <a name="connected-property"></a>Proprietà connessa

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se il controllo corrente è connesso al server Microsoft Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. * * * connesso* *  \[  =  *valore booleano*\]



| Parte      | Descrizione                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se il controllo è connesso. Valore **true** Il controllo è connesso.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

In molte situazioni, l'impostazione del controllo crea automaticamente una connessione al server Microsoft Agent. Se, ad esempio, si specifica il CLSID del controllo Microsoft Agent nel <OBJECT> tag in una pagina Web, viene aperta automaticamente una connessione al server e l'uscita dalla pagina chiude la connessione. Analogamente, per Visual Basic o altri linguaggi che consentono di eliminare un controllo in un form, l'esecuzione del programma apre automaticamente una connessione e l'uscita dal programma chiude la connessione. Se il server non è attualmente in esecuzione, viene avviato automaticamente.

Tuttavia, se si desidera creare un controllo agente in fase di esecuzione, potrebbe essere necessario aprire in modo esplicito una nuova connessione al server utilizzando la proprietà **connessa** . In Visual Basic, ad esempio, è possibile creare un oggetto ActiveX in fase di esecuzione usando l'istruzione set con la parola chiave **New** (o la funzione CreateObject). Durante la creazione dell'oggetto, è possibile che non crei la connessione al server. È possibile usare la proprietà **Connected** prima del codice che chiama l'interfaccia di programmazione di Microsoft Agent, come illustrato nell'esempio seguente:


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



La creazione di un controllo utilizzando questa tecnica non espone gli eventi del controllo agente. In Visual Basic 5,0 (e versioni successive) è possibile accedere agli eventi del controllo includendo il controllo nei riferimenti del progetto e usare la parola chiave **WithEvents** nella dichiarazione di variabile:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



L'utilizzo di **WithEvents** per creare un'istanza del controllo agente in fase di esecuzione apre automaticamente la connessione al server Microsoft Agent. Non è quindi necessario includere un'istruzione **connessa** .

È possibile chiudere la connessione al server rilasciando tutti i riferimenti creati agli oggetti di Agent, ad esempio IAgentCtlCharacterEx e IAgentCtlCommandEx. È inoltre necessario rilasciare il riferimento al controllo agente stesso. In Visual Basic è possibile rilasciare un riferimento a un oggetto impostando la relativa variabile su **Nothing**. Se sono stati caricati caratteri, scaricarli prima di rilasciare l'oggetto carattere.


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> Non è possibile chiudere la connessione al server rilasciando i riferimenti in cui è stato aggiunto il componente. Non è ad esempio possibile chiudere la connessione al server nelle pagine Web in cui si usa il <OBJECT> tag per dichiarare il controllo o in un'applicazione Visual Basic in cui si rilascia il controllo in un form. Quando si rilasciano tutti i riferimenti all'agente, il working set dell'agente viene ridotto, la connessione rimane fino a quando non si passa alla pagina successiva o si esce dall'applicazione.

 

 

 





