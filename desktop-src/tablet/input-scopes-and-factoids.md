---
description: Descrive come vengono usati gli ambiti di input per il riconoscimento.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Ambiti di input e factoid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881ebd26cbfb70cb215103b9a6face356af078e47b74a2e9140886f81f457eef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450971"
---
# <a name="input-scopes-and-factoids"></a>Ambiti di input e factoid

Un ambito di input è un set definito di parole, numeri, punteggiatura e ordinamenti sintattici consentiti all'interno di un determinato modello linguistico. Gli ambiti di input possono essere usati dalle applicazioni per limitare il modello linguistico usato dal sistema di riconoscimento a un contesto specifico. Ad esempio, un ambito di input IS \_ EMAIL SMTPEMAILADDRESS influenza i risultati del riconoscimento indicando che un campo \_ specifico è un indirizzo di posta elettronica. Di conseguenza, è probabile che il campo contenga caratteri come " " " e non contenga caratteri come @" and " \_ " " e \* spazi.

> [!Note]  
> Anche altre tecnologie Microsoft usano ambiti di input. Questo articolo descrive l'uso del contesto per migliorare l'accuratezza dei motori di riconoscimento della grafia per le applicazioni Tablet PC.

 

Nelle versioni precedenti dell'API Tablet PC Technology sono stati usati factoid per definire il contesto. Per scopi pratici, un factoid è la stessa cosa di un ambito di input. La versione uno della piattaforma Tablet PC SDK ha definito un set di valori factoid [**nell'oggetto Factoid.**](factoid-constants.md) Questi valori sono stati usati per impostare il contesto e influenzare i risultati del riconoscimento quando si usa [**l'oggetto RecognizerContext**](inkrecognizercontext-class.md) per il riconoscimento. Per i riconoscitori di script latini che iniziano con Windows XP Tablet PC Edition 2005, si usa comunque la proprietà [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) dell'oggetto **RecognizerContext** per impostare il contesto, ma è necessario passare un ambito di input, un elenco di frasi o un valore di espressione regolare di scrittura manuale anziché uno dei valori factoid della versione uno. I riconoscitori Microsoft dei caratteri dell'Asia orientale non supportano l'uso dei valori enumerati dell'ambito di input. È consigliabile continuare a usare i valori factoid per i riconoscitori di caratteri dell'Asia orientale.

Gli ambiti di input e i factoid sono restrizioni per le alternative a livello di parola. Le alternative di caratteri possono non rientrare nell'ambito di input specificato anche quando è impostato il flag **COERCE.**

Quando il flag **COERCE** è impostato con un factoid restrittivo, può verificarsi che il riconoscitore non possa produrre una risposta che corrisponda all'input penna e soddisfi il factoid. Un altro scenario in cui il riconoscitore potrebbe non produrre una risposta soddisfacente è quando la lingua del riconoscimento non corrisponde alla lingua dell'input penna ,ad esempio il riconoscimento inglese degli Stati Uniti e i caratteri dell'input penna cinese.

Quando il riconoscimento della grafia non riconosce l'input penna per una determinata parola o carattere, può restituire un elenco alternativo vuoto o un elenco alternativo in cui la prima scelta è il punto di codice 0xffff (carattere non definito). Ciò è particolarmente utile nelle modalità di input della guida boxed, in cui ogni casella con input penna deve avere un elenco non vuoto di alternative. L'applicazione può quindi visualizzare questo carattere non definito in qualsiasi modo scelto (ad esempio come "???").

> [!Note]  
> I valori factoid continuano a funzionare con i riconoscitori dello script latino per garantire la compatibilità con le versioni precedenti.

 

Per altre informazioni sui factoid, vedere [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).

Per informazioni sui factoid dell'Asia orientale, vedere [Factoid supportati dalla versione 1.](supported-factoids-from-version-1.md)

 

 



