---
description: Tutto il riconoscimento per i controlli abilitati per l'input penna avviene tramite un oggetto RecognizerContext. Le API della tecnologia Tablet PC consentono di impostare la proprietà Factoid su un oggetto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Impostazione del contesto per Ink-Enabled controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306ae4c76ce5187c930c24a10631ec703f684cc8a3e4b0a94f46414bddbd058f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091307"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Impostazione del contesto per Ink-Enabled controllo

Tutto il riconoscimento per i controlli abilitati per l'input penna avviene tramite [**un oggetto RecognizerContext.**](inkrecognizercontext-class.md) Le API della tecnologia Tablet PC consentono di impostare la proprietà [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) in un **oggetto RecognizerContext.**

Se si crea un'applicazione abilitata per l'input penna, usare le proprietà [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) e [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per impostare i contesti.

È possibile passare i valori stringa dei nomi negli ambiti di input definiti nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) alla proprietà [**Factoid,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) delimitata da un'apertura (! e un oggetto di chiusura . Ad esempio, per impostare il contesto per un [**oggetto RecognizerContext**](inkrecognizercontext-class.md) in modo che prevari i caratteri usati in un URL, usare la sintassi illustrata negli esempi C \# seguenti:


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> Gli ambiti di input definiti nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) soppiantino i factoid disponibili nelle versioni precedenti di Windows XP Tablet PC Edition SDK, anche se questi factoid continueranno a funzionare per garantire la compatibilità con le versioni precedenti.

 

Nell'esempio C \# seguente viene [**impostata la proprietà Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) per i codici postali:


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



È possibile combinare gli ambiti di input usando la sintassi dell'espressione regolare di scrittura manuale. Per altre informazioni sull'uso della sintassi delle espressioni regolari, vedere [Ambiti di input personalizzati con espressioni regolari.](custom-input-scopes-with-regular-expressions.md)

È possibile impostare flag di riconoscimento [**nell'oggetto RecognizerContext**](inkrecognizercontext-class.md) per influire sul comportamento del riconoscimento. Uno di questi flag è il flag **Coerce** [**nell'enumerazione InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) di **RecognizerContext.** Il flag **Coerce** forza il riconoscimento a restituire un risultato che corrisponde alla definizione del factoid impostato. Ad esempio, se si dispone di un modulo che richiede all'utente di immettere una quantità numerica, può essere utile impostare il factoid **IS \_ NUMBER** e anche impostare la [**proprietà RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) su **Coerce**. In questo caso, il flag **Coerce** garantisce che il riconoscimento restituisca solo numeri.

Nell'esempio C \# seguente la [**proprietà RecognitionFlags viene**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) impostata su **Coerce**:


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



Prestare tuttavia attenzione quando si decide di impostare il flag **Coerce.** Il flag forza il riconoscimento in modo che corrisponda solo alla definizione del factoid. Ad esempio, se si impostano l'ambito di input IS TELEPHONE FULLTELEPHONENUMBER e il flag Coerce, il riconoscimento restituisce risultati che corrispondono esattamente alla definizione dell'ambito di \_ \_ input IS TELEPHONE  \_ \_ FULLTELEPHONENUMBER. Se un utente scrive "911" con l'ambito di input IS TELEPHONE FULLTELEPHONENUMBER e il flag Coerce impostato, il riconoscimento può restituire una stringa vuota o una stringa casuale nel formato \_ \_ (XXX) XXX-XXXX (dove X è una cifra).  Il formato di XXX non corrisponde alla definizione del \_ factoid IS TELEPHONE \_ FULLTELEPHONENUMBER, anche se è un numero di telefono valido.

Per gli elenchi dei formati supportati per ogni ambito di input, vedere le informazioni di [**riferimento su InputScope.**](/windows/win32/api/inputscope/ne-inputscope-inputscope)

Per ripristinare l'impostazione predefinita di un campo per il riconoscimento, impostare il factoid su IS \_ DEFAULT , come nell'esempio C \# seguente:


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



Per le applicazioni che usano il [controllo InkEdit,](inkedit-control-reference.md) impostare il tipo factoid per il controllo specificando:


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Dove `IS_INPUTSCOPE` è il nome dell'ambito di input da applicare.

Il [controllo InkEdit](inkedit-control-reference.md) non espone un [**oggetto RecognizerContext.**](inkrecognizercontext-class.md) È comunque possibile assegnare il contesto usando la proprietà [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) del controllo InkEdit, ma non è possibile impostare il flag **WORDMODE.**

 

 
