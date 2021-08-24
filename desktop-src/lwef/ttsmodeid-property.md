---
title: Proprietà TTSModeID
description: Proprietà TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a720b06362b77418434669146a0d89dea8afd37d7a44c4079b2e12c24fcd2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607961"
---
# <a name="ttsmodeid-property"></a>Proprietà TTSModeID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la modalità del motore TTS utilizzata per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). TTSModeID_ *  \[  =  *ModeID*\]



| Parte     | Descrizione                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Espressione stringa che corrisponde all'ID modalità di un motore di riconoscimento vocale. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà determina l'ID della modalità del motore TTS (sintesi vocale) per l'output parlato di un carattere. L'ID modalità per un motore TTS è una stringa formattata definita dal fornitore del riconoscimento vocale che identifica in modo univoco la modalità del motore. Per altre informazioni, vedere [Accesso a un motore di riconoscimento vocale nel codice.](accessing-a-speech-engine-in-your-code.md)

L'impostazione di questa proprietà sostituisce il tentativo del server di caricare un motore in base all'impostazione TTS compilata del carattere e all'impostazione [**LanguageID**](languageid-property.md) corrente del carattere. Tuttavia, se si specifica un ID modalità per un motore che non è installato o se l'utente ha disabilitato l'output vocale nella finestra delle proprietà di Microsoft Agent (**AudioOutput.Enabled = False**), il server genera un errore.

Se non è stato impostato (o non è stato impostato correttamente) un ID modalità TTS per il carattere, il server verifica se l'impostazione della modalità TTS compilata del carattere corrisponde all'impostazione [**LanguageID**](languageid-property.md) del carattere e se il motore TTS associato è installato. In tal caso, la modalità TTS usata dal carattere per l'output parlato e questa proprietà restituisce tale ID modalità. In caso contrario, il server richiede un motore di riconoscimento vocale SAPI compatibile che corrisponda al **LanguageID** del carattere, nonché il sesso e l'età impostati per l'ID modalità compilata del carattere. Se l'ID lingua del carattere non è stato **impostato,** il **relativo LanguageID** è la lingua dell'utente corrente. Se non viene trovato alcun motore corrispondente, l'esecuzione di query per questa proprietà restituisce una stringa vuota per l'ID modalità del motore. Analogamente, se si esegue una query su questa proprietà quando l'utente ha disabilitato l'output vocale nella finestra delle proprietà di Microsoft Agent (**AudioOutput.Enabled = False),** il valore sarà una stringa vuota.

L'esecuzione di query o l'impostazione di questa proprietà carica il motore associato (se non è già caricato). Tuttavia, se il motore specificato nell'impostazione TTS compilata del carattere è installato e corrisponde all'impostazione dell'ID lingua del carattere, il motore verrà caricato al caricamento del carattere.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore di riconoscimento vocale di Microsoft Agent si basano su Microsoft Speech API. I motori che supportano i requisiti SAPI di Microsoft Agent possono essere installati e usati con Agent.

> [!Note]  
> Questa proprietà restituisce anche la stringa vuota se nel sistema non è installato alcun supporto audio compatibile.

 

> [!Note]  
> **L'impostazione di TTSModeID** può non riuscire se Speech.dll non è installato e il motore specificato non corrisponde all'impostazione della modalità TTS compilata del carattere.

 

> [!Note]  
> L'esecuzione di query su questa proprietà in genere non restituisce un errore. Tuttavia, se il caricamento del motore di riconoscimento vocale richiede un tempo anomalo, è possibile che venga visualizzato un errore che indica che si è verificato il timeout della query.

 

## <a name="see-also"></a>Vedere anche

[**LanguageID - proprietà**](languageid-property.md)


 

 




