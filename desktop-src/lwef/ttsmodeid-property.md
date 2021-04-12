---
title: Proprietà TTSModeID
description: Proprietà TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221893"
---
# <a name="ttsmodeid-property"></a>Proprietà TTSModeID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la modalità del motore di TTS utilizzata per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *").* *  \[  =  *ModeID* TTSModeID\]



| Parte     | Descrizione                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Espressione stringa che corrisponde all'ID modalità di un motore vocale. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà determina l'ID della modalità del motore TTS (sintesi vocale) per l'output parlato di un carattere. L'ID modalità per un motore TTS è una stringa formattata definita dal fornitore vocale che identifica in modo univoco la modalità del motore. Per altre informazioni, vedere [accesso a un motore di riconoscimento vocale nel codice](accessing-a-speech-engine-in-your-code.md).

L'impostazione di questa proprietà esegue l'override del tentativo del server di caricare un motore in base all'impostazione TTS compilata del carattere e all'impostazione [**LanguageID**](languageid-property.md) corrente del carattere. Tuttavia, se si specifica un ID modalità per un motore che non è installato o se l'utente ha disabilitato l'output vocale nella finestra delle proprietà dell'agente Microsoft (**AudioOutput. Enabled = false**), il server genera un errore.

In caso contrario, impostare un ID modalità TTS per il carattere, il server verificherà se l'impostazione della modalità TTS compilata del carattere corrisponde all'impostazione [**LanguageID**](languageid-property.md) del carattere e che il motore TTS associato sia installato. In tal caso, la modalità TTS utilizzata dal carattere per l'output parlato e questa proprietà restituisce tale ID modalità. In caso contrario, il server richiede un motore di riconoscimento vocale SAPI compatibile che corrisponde al **LanguageID** del carattere, nonché il genere e l'età impostati per l'ID modalità compilata del carattere. Se il **LanguageID** del carattere non è stato impostato, il relativo **LanguageID** è la lingua dell'utente corrente. Se non è possibile trovare alcun motore corrispondente, l'esecuzione di una query per questa proprietà restituisce una stringa vuota per l'ID modalità del motore. Analogamente, se si esegue una query su questa proprietà quando l'utente ha disabilitato l'output vocale nella finestra delle proprietà dell'agente Microsoft (**AudioOutput. Enabled = false**), il valore sarà una stringa vuota.

Se si esegue una query o si imposta questa proprietà, il motore associato verrà caricato (se non è già stato caricato). Tuttavia, se il motore specificato nell'impostazione di TTS compilata del carattere è installato e corrisponde all'impostazione dell'ID lingua del carattere, il motore verrà caricato quando viene caricato il carattere.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft. I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.

> [!Note]  
> Questa proprietà restituisce anche la stringa vuota se nel sistema non è installato alcun supporto audio compatibile.

 

> [!Note]  
> L'impostazione di **TTSModeID** può avere esito negativo se Speech.dll non è installato e il motore specificato non corrisponde all'impostazione della modalità TTS compilata del carattere.

 

> [!Note]  
> L'esecuzione di query su questa proprietà in genere non restituisce un errore. Tuttavia, se il tempo di caricamento del motore vocale richiede un tempo insolitamente lungo, potrebbe essere presente un errore che indica che si è verificato il timeout della query.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà LanguageID**](languageid-property.md)


 

 




