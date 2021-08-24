---
title: Proprietà Connected
description: Proprietà Connected
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af3a44e97236060733adc55ec6e44eddd0b1d8879250b2a28b54c0bca384cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726092"
---
# <a name="connected-property"></a>Proprietà Connected

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se il controllo corrente è connesso al server Microsoft Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Connected* *  \[  =  *booleano*\]



| Parte      | Descrizione                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se il controllo è connesso. **True** Il controllo è connesso.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

In molte situazioni, specificando il controllo viene creata automaticamente una connessione con il server Microsoft Agent. Ad esempio, se si specifica il CLSID del controllo Microsoft Agent nel tag in una pagina Web, viene aperta automaticamente una connessione server e la chiusura della pagina chiude <OBJECT> la connessione. Analogamente, per Visual Basic o altre lingue che consentono di rilasciare un controllo in un form, l'esecuzione del programma apre automaticamente una connessione e l'uscita dal programma chiude la connessione. Se il server non è attualmente in esecuzione, viene avviato automaticamente.

Tuttavia, se si vuole creare un controllo Agent in fase di esecuzione, potrebbe anche essere necessario aprire in modo esplicito una nuova connessione al server usando la **proprietà Connected.** Ad esempio, in Visual Basic è possibile creare un oggetto ActiveX in fase di esecuzione usando l'istruzione Set con la parola chiave **New** (o la funzione CreateObject). Anche se questo crea l'oggetto , potrebbe non creare la connessione al server. È possibile usare la **proprietà Connected** prima di qualsiasi codice che chiama l'interfaccia di programmazione di Microsoft Agent, come illustrato nell'esempio seguente:


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



La creazione di un controllo con questa tecnica non espone gli eventi del controllo Agent. In Visual Basic 5.0 (e versioni successive), è possibile accedere agli eventi del controllo includendo il controllo nei riferimenti del progetto e usare la parola chiave **WithEvents** nella dichiarazione di variabile:


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



**L'uso di WithEvents** per creare un'istanza del controllo Agent in fase di esecuzione apre automaticamente la connessione con il server Microsoft Agent. Pertanto, non è necessario includere un'istruzione **Connected.**

È possibile chiudere la connessione al server rilasciando tutti i riferimenti creati agli oggetti Agent, ad esempio IAgentCtlCharacterEx e IAgentCtlCommandEx. È anche necessario rilasciare il riferimento al controllo Agent stesso. In Visual Basic, è possibile rilasciare un riferimento a un oggetto impostandone la variabile su **Nothing**. Se sono stati caricati caratteri, scaricarli prima di rilasciare l'oggetto carattere.


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
> Non è possibile chiudere la connessione al server rilasciando i riferimenti in cui è stato aggiunto il componente. Ad esempio, non è possibile chiudere la connessione al server nelle pagine Web in cui si usa il tag per dichiarare il controllo o in un'applicazione Visual Basic in cui si rilascia il controllo <OBJECT> in un form. Mentre il rilascio di tutti i riferimenti a Agent ridurrà l'working set di Agent, la connessione rimane finché non si passa alla pagina successiva o non si esce dall'applicazione.

 

 

 





