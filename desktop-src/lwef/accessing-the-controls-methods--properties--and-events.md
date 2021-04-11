---
title: Accesso ai metodi, alle proprietà e agli eventi dei controlli
description: Accesso ai metodi, alle proprietà e agli eventi dei controlli
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395846"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a>Accesso ai metodi, alle proprietà e agli eventi dei controlli

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'utilizzo del controllo di Microsoft Agent con Visual Basic è molto simile all'utilizzo del controllo con VBScript, ad eccezione del fatto che gli eventi in Visual Basic devono includere il tipo di dati dei parametri passati. Se si aggiunge il controllo Microsoft Agent a un modulo, verranno automaticamente inclusi gli eventi di Microsoft Agent con i relativi parametri appropriati. Verrà inoltre creata automaticamente una connessione al Server Agent durante l'esecuzione dell'applicazione.

È anche possibile usare la sintassi di creazione object's del linguaggio di programmazione per creare un'istanza del controllo in fase di esecuzione. Ad esempio, in Visual Basic (5,0 o versioni successive), se si include il controllo Microsoft Agent 2,0 nei riferimenti del progetto, è possibile usare un [**con eventi**](https://www.bing.com/search?q=**With+Events**). [**Nuova**](https://www.bing.com/search?q=**New**) dichiarazione. Se non si include il riferimento, VB genera un errore che indica che non è stato possibile avviare Microsoft Agent (codice errore 80042502).

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

Per le versioni di VB precedenti alla 5,0, è possibile usare la parola chiave VB [**New**](https://www.bing.com/search?q=**New**) senza Dichiarazione [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) o la funzione [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) di VB, ma queste convenzioni non esporrà gli eventi del controllo agente. È anche necessario usare la proprietà [**Connected**](https://www.bing.com/search?q=**Connected**) prima di fare riferimento a qualsiasi proprietà o metodo di Agent. In caso contrario, VB genererà un errore che indica che non è stato possibile avviare Microsoft Agent (codice errore 80042502).

Analogamente per altri linguaggi di programmazione, potrebbe essere necessario utilizzare la proprietà [**Connected**](https://www.bing.com/search?q=**Connected**) per stabilire una connessione al server dell'agente Component Object Model (com) prima che il codice possa chiamare qualsiasi metodo o proprietà del controllo agente. Per alcuni linguaggi di programmazione, inoltre, i metodi e le proprietà dell'agente potrebbero non essere esposti direttamente, a meno che non si dichiari il controllo Agent utilizzando il relativo tipo. Ad esempio, in Microsoft Access 97, è necessario dichiarare l'oggetto come tipo Agent per visualizzare i metodi e le proprietà visualizzati nella casella di riepilogo a discesa elenco automatico membri quando si digita.

La maggior parte dei linguaggi di programmazione che supportano i controlli ActiveX seguono convenzioni simili a Visual Basic. Per i linguaggi di programmazione che non supportano le raccolte di oggetti, è possibile usare il metodo [**character**](https://www.bing.com/search?q=**Character**) e il metodo [**Command**](https://www.bing.com/search?q=**Command**) per accedere ai metodi e alle proprietà degli elementi nella raccolta.

I linguaggi di programmazione come Visual Basic, che forniscono accesso ai tipi di oggetti esposti dal controllo agente, consentono di usarli nelle dichiarazioni di oggetti. Ad esempio, anziché dichiarare un oggetto come tipo generico:

``` syntax
   Dim Genie as Object
```

È possibile dichiarare un oggetto come tipo specifico:

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

Questo può migliorare le prestazioni complessive dell'applicazione.

Per alcuni tipi di oggetti, è possibile che siano presenti due tipi uguali, ad eccezione del suffisso "ex". In entrambi i casi, usare il tipo "ex" perché fornisce le funzionalità complete di Agent. Le controparti non "ex" sono incluse solo per la compatibilità con le versioni precedenti.

 

 




