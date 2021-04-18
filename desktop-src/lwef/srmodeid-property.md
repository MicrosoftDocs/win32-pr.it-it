---
title: Proprietà SRModeID
description: Proprietà SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298955"
---
# <a name="srmodeid-property"></a>Proprietà SRModeID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il motore di riconoscimento vocale utilizzato dal carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *").* *  \[  =  *ModeID* SRModeID\]



| Parte     | Descrizione                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Espressione stringa che corrisponde all'ID modalità di un motore vocale. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà determina il motore di riconoscimento vocale usato dal carattere per l'input vocale. L'ID modalità per un motore di riconoscimento vocale è una stringa formattata definita dal fornitore di sintesi vocale che identifica in modo univoco il motore. Per altre informazioni, vedere [accesso a un motore di riconoscimento vocale nel codice](accessing-a-speech-engine-in-your-code.md).

Se si specifica un ID modalità per un motore vocale non installato, se l'utente ha disabilitato il riconoscimento vocale (nella finestra delle proprietà di Microsoft Agent) o se la lingua del motore di riconoscimento vocale specificato non corrisponde all'impostazione [**LanguageID**](languageid-property.md) del carattere, il server genera un errore.

Se si esegue una query su questa proprietà e non è stato ancora impostato il motore di riconoscimento vocale, il server restituisce l'ID modalità del motore restituito da SAPI in base all'impostazione [**LanguageID**](languageid-property.md) del carattere. Se il **LanguageID** del carattere non è stato impostato, Agent restituisce l'ID modalità del motore restituito da SAPI in base all'impostazione dell'ID lingua predefinita dell'utente. Se non è presente alcun motore corrispondente, il server restituisce una stringa vuota (""). Per eseguire una query su questa proprietà non è necessario che [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) sia impostato su **true**. Tuttavia, se si esegue una query sulla proprietà quando l'input vocale è disabilitato, il server restituisce una stringa vuota.

Quando l'input vocale è abilitato (nella finestra Opzioni carattere avanzato), l'esecuzione di una query o l'impostazione di questa proprietà caricherà il motore associato (se non è già caricato) e avvierà servizi vocali. Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile. (Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft. I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.

> [!Note]  
> Questa proprietà restituisce anche la stringa vuota se nel sistema non è installato alcun supporto audio compatibile.

 

> [!Note]  
> L'esecuzione di query su questa proprietà in genere non restituisce un errore. Tuttavia, se il tempo di caricamento del motore vocale richiede un tempo insolitamente lungo, potrebbe essere presente un errore che indica che si è verificato il timeout della query.

 

## <a name="see-also"></a>Vedere anche

[**Proprietà LanguageID**](languageid-property.md)


 

 




