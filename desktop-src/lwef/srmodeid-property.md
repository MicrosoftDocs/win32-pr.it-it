---
title: Proprietà SRModeID
description: Proprietà SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2ea6664230f9b2446cbe10a31a0129abb8bc52f0679bb6fdec0a1f0a8be211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960861"
---
# <a name="srmodeid-property"></a>Proprietà SRModeID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il motore di riconoscimento vocale utilizzato dal carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Characters("**_CharacterID_*_"). ModeID SRModeID_ *  \[  =  \]



| Parte     | Descrizione                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Espressione stringa che corrisponde all'ID modalità di un motore di riconoscimento vocale. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà determina il motore di riconoscimento vocale usato dal carattere per l'input vocale. L'ID modalità per un motore di riconoscimento vocale è una stringa formattata definita dal fornitore del riconoscimento vocale che identifica in modo univoco il motore. Per altre informazioni, vedere [Accesso a un motore di riconoscimento vocale nel codice](accessing-a-speech-engine-in-your-code.md).

Se si specifica un ID modalità per un motore di riconoscimento vocale che non è installato, se l'utente ha disabilitato il riconoscimento vocale (nella finestra delle proprietà di Microsoft Agent) o se la lingua del motore di riconoscimento vocale specificato non corrisponde all'impostazione [**LanguageID**](languageid-property.md) del carattere, il server genera un errore.

Se si esegue una query su questa proprietà e non si è ancora (correttamente) impostato il motore di riconoscimento vocale, il server restituisce l'ID modalità del motore restituito da SAPI in base all'impostazione [**LanguageID**](languageid-property.md) del carattere. Se non è stato impostato **languageID** del carattere, Agent restituisce l'ID modalità del motore restituito da SAPI in base all'impostazione predefinita dell'ID lingua dell'utente. Se non è presente alcun motore corrispondente, il server restituisce una stringa vuota (""). L'esecuzione di query su questa proprietà non richiede che [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) sia impostato su **True.** Tuttavia, se si esegue una query sulla proprietà quando l'input vocale è disabilitato, il server restituisce una stringa vuota.

Quando l'input vocale è abilitato (nella finestra Opzioni carattere avanzate), l'esecuzione di query o l'impostazione di questa proprietà carica il motore associato (se non è già caricato) e avvia i servizi voce. Ciò significa che la chiave di ascolto è disponibile e il suggerimento per l'ascolto è visualizzabile. La chiave di ascolto e il suggerimento di ascolto sono abilitati solo se sono abilitati anche in Opzioni carattere avanzate. Tuttavia, se si esegue una query sulla proprietà quando la voce è disabilitata, il server non avvia i servizi voce.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore di riconoscimento vocale di Microsoft Agent sono basati su Microsoft Speech API. I motori che supportano i requisiti SAPI di Microsoft Agent possono essere installati e usati con Agent.

> [!Note]  
> Questa proprietà restituisce anche la stringa vuota se nel sistema non è installato alcun supporto audio compatibile.

 

> [!Note]  
> L'esecuzione di query su questa proprietà in genere non restituisce un errore. Tuttavia, se il caricamento del motore di riconoscimento vocale richiede un tempo anomalo, è possibile che venga visualizzato un errore che indica che si è verificato il timeout della query.

 

## <a name="see-also"></a>Vedere anche

[**LanguageID - proprietà**](languageid-property.md)


 

 




