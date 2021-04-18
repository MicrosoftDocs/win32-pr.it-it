---
description: Tutto il riconoscimento per i controlli abilitati all'input penna viene eseguito tramite un oggetto RecognizerContext. Le API della tecnologia Tablet PC consentono di impostare la proprietà del controllo del controllo su un oggetto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Impostazione del contesto per i controlli Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348626"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Impostazione del contesto per i controlli Ink-Enabled

Tutto il riconoscimento per i controlli abilitati all'input penna viene eseguito tramite un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) . Le API della tecnologia Tablet PC consentono di impostare la [**proprietà del controllo del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) su un oggetto **RecognizerContext** .

Se si sta creando un'applicazione abilitata per l'input penna, usare le proprietà del [**controllo dell'oggetto RecognizerContext e del**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) [**nome**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per impostare i contesti.

È possibile passare i valori stringa dei nomi negli ambiti di input definiti nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) [**alla proprietà del controllo oggetto,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) delimitata da un'apertura (! e una chiusura. Per impostare, ad esempio, il contesto di un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) su bias verso i caratteri utilizzati in un URL, utilizzare la sintassi illustrata negli \# esempi C seguenti:


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> Gli ambiti di input come definito nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) sostituiscono il factoids disponibile nelle versioni precedenti di Windows XP Tablet PC Edition SDK, anche se questi factoids continueranno a funzionare per garantire la compatibilità con le versioni precedenti.

 

Nell'esempio C seguente \# viene impostata [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) la proprietà del controllore per i codici postali:


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



È possibile combinare gli ambiti di input usando la sintassi delle espressioni regolari della grafia. Per altri dettagli sull'uso della sintassi delle espressioni regolari, vedere [ambiti di input personalizzati con espressioni regolari](custom-input-scopes-with-regular-expressions.md).

È possibile impostare i flag di riconoscimento nell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per influire sul comportamento del riconoscimento. Uno di questi flag è il flag di **coercizione** nell'enumerazione [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) dell'oggetto **RecognizerContext**. Il flag di **coercizione** impone al riconoscimento di restituire un risultato che corrisponda alla definizione del controllo oggetto impostato. Se, ad esempio, si dispone di un modulo che richiede all'utente di immettere una quantità numerica, può essere utile impostare il controllo del controllo dei **\_ numeri** e impostare anche la proprietà [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) su **coercizione**. In tale istanza, il flag di **coercizione** garantisce che il riconoscimento restituisca solo numeri.

L'esempio C seguente \# imposta la proprietà [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) su **coercizione**:


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



Tuttavia, prestare attenzione quando si decide di impostare il flag di **coercizione** . Il flag impone al riconoscimento di trovare la corrispondenza solo con la definizione del controllo del controllo. Se, ad esempio, si imposta l' \_ \_ ambito di input FULLTELEPHONENUMBER telefonico e il flag di **coercizione** , il riconoscimento restituisce risultati che corrispondono esattamente alla definizione dell' \_ ambito di \_ input di FULLTELEPHONENUMBER telefonico. Se un utente scrive "911" con l' \_ \_ ambito di input is Phone FULLTELEPHONENUMBER e il flag di **coercizione** impostato, il riconoscimento può restituire una stringa vuota o una stringa casuale nel formato (xxx) xxx-xxxx (dove X è una cifra). Il formato XXX non corrisponde alla definizione del controllo del \_ \_ codice FULLTELEPHONENUMBER telefonico, anche se è un numero di telefono valido.

Per gli elenchi dei formati supportati per ogni ambito di input, vedere la Guida di riferimento a [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .

Per restituire un campo all'impostazione predefinita per il riconoscimento, impostare il controllo oggetto su è \_ predefinito, come nell'esempio C seguente \# :


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



Per le applicazioni che usano il controllo [InkEdit](inkedit-control-reference.md) , impostare il tipo di controllo dell'oggetto per il controllo specificando:


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Dove `IS_INPUTSCOPE` è il nome dell'ambito di input che si desidera applicare.

Il controllo [InkEdit](inkedit-control-reference.md) non espone un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) . È comunque possibile [**assegnare il contesto usando la proprietà del**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) controllo InkEdit del controllo InkEdit, ma non è possibile impostare il flag **WORDMODE** .

 

 
