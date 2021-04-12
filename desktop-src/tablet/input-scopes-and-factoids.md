---
description: Viene descritto come usare gli ambiti di input per il riconoscimento.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Ambiti di input e factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbb46e21a0524f806daa4eed789fde31e285109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233878"
---
# <a name="input-scopes-and-factoids"></a>Ambiti di input e factoids

Un ambito di input è un set definito di parole, numeri, punteggiatura e ordinamenti sintattici consentiti all'interno di un modello di linguaggio specifico. Gli ambiti di input possono essere utilizzati dalle applicazioni per limitare il modello di linguaggio utilizzato dal riconoscimento a un contesto specifico. Ad esempio, un ambito di input di è \_ posta elettronica \_ SMTPEMAILADDRESS influenza i risultati del riconoscimento indicando che un campo specifico è un indirizzo di posta elettronica. Pertanto, è probabile che il campo contenga caratteri come " @" and " \_ " e che non contenga caratteri quali " \* " e spazi.

> [!Note]  
> Anche altre tecnologie Microsoft usano ambiti di input. Questo articolo è incentrato sull'utilizzo del contesto per migliorare l'accuratezza dei motori di riconoscimento della grafia per le applicazioni Tablet PC.

 

Le versioni precedenti dell'API della tecnologia Tablet PC usavano factoids per definire il contesto. Per motivi pratici, un controllo oggetto è uguale a quello di un ambito di input. Versione una della piattaforma Tablet PC SDK definisce un set di valori del [**controllo dell'oggetto dell'oggetto.**](factoid-constants.md) Questi valori sono stati usati per impostare il contesto e influenzare i risultati del riconoscimento quando si usa l'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per il riconoscimento. Per i riconoscitori degli script latini che iniziano con Windows XP Tablet PC Edition 2005, è comunque possibile usare la proprietà del controllo dell'oggetto **RecognizerContext** per [**impostare il contesto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , ma è necessario passare un ambito di input, un elenco di frasi o un valore di espressione regolare della grafia anziché uno dei valori del controllo della versione uno. I riconoscitori Microsoft dei caratteri asiatici orientali non supportano l'utilizzo dei valori enumerati dell'ambito di input. È necessario continuare a utilizzare i valori del controllore per i riconoscitori dei caratteri asiatici orientali.

Gli ambiti di input e factoids sono restrizioni per le alternative a livello di parola; il carattere alternativo può essere esterno all'ambito di input specificato anche quando è impostato il flag di **coercizione** .

Quando il flag di **coercizione** è impostato con un controllo del controllo restrittivo, è possibile che il riconoscimento non sia in grado di produrre una risposta che corrisponda all'input penna e che soddisfi il controllo del controllo. Un altro scenario in cui il riconoscimento non può produrre una risposta soddisfacente è quando la lingua del riconoscimento non corrisponde alla lingua dell'input penna (ad esempio, il riconoscimento inglese degli Stati Uniti e i caratteri dell'input penna cinese).

Quando il riconoscimento della grafia non riesce a riconoscere l'input penna per una parola o un carattere specifico, può restituire un elenco alternativo vuoto o un elenco alternativo in cui la prima scelta è il punto di codice 0xFFFF (carattere non definito). Questa operazione è particolarmente utile nelle modalità di input della Guida boxed, in cui ogni casella con input penna prevede un elenco non vuoto di alternative. L'applicazione può quindi visualizzare questo carattere non definito nel modo scelto (ad esempio, "???").

> [!Note]  
> I valori del controllore continuano a funzionare con i riconoscitori dello script latino per la compatibilità con le versioni precedenti.

 

Per ulteriori informazioni su factoids, vedere [impostazione del contesto per i controlli Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Per informazioni sulle factoids dell'Asia orientale, vedere [Supported Factoids dalla versione 1](supported-factoids-from-version-1.md).

 

 



