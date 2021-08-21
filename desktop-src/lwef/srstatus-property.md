---
title: Proprietà SRStatus
description: Proprietà SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7cc079c79b3539fa5ad90da4f45907236f19d3b841cf580142446b230ff7c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975681"
---
# <a name="srstatus-property"></a>Proprietà SRStatus

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se è possibile iniziare l'input vocale per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). SRStatus_*



| Valore | Descrizione                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Le condizioni supportano l'input vocale.                                                                                                                                                                                                          |
| 1     | In questo sistema non è disponibile alcun dispositivo di input audio. Si noti che non viene rilevato se è installato un microfono, ma solo se l'utente dispone di una scheda audio abilitata per l'input installata correttamente con un driver funzionante. |
| 2     | Un altro client è il client attivo di questo carattere o il carattere corrente non è in primo piano.                                                                                                                                           |
| 3     | Il canale di input o output audio è attualmente occupato e un'applicazione usa l'audio.                                                                                                                                                       |
| 4     | Si è verificato un errore non specificato durante il processo di inizializzazione del sottosistema di riconoscimento vocale. Ciò include la possibilità che non sia disponibile alcun motore di riconoscimento vocale corrispondente all'impostazione della lingua del carattere.                          |
| 5     | L'utente ha disabilitato l'input vocale in Opzioni avanzate per i caratteri.                                                                                                                                                                     |
| 6     | Si è verificato un errore durante il controllo dello stato audio, ma la causa dell'errore non è stata restituita dal sistema.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà restituisce le condizioni necessarie per supportare l'input vocale, incluso lo stato del dispositivo audio. È possibile controllare questa proprietà prima di chiamare il [**metodo Listen**](listen-method.md) per garantirne l'esito positivo.

Quando l'input vocale è abilitato nella finestra delle proprietà di Agent (Opzioni carattere avanzate), l'esecuzione di query su questa proprietà carica il motore associato, se non è già caricato, e avvia i servizi voce. Ciò significa che la chiave di ascolto è disponibile e il suggerimento per l'ascolto è automaticamente visualizzabile. Le opzioni Chiave di ascolto e Suggerimento per l'ascolto sono abilitate solo se sono abilitate anche in Opzioni avanzate per i caratteri. Tuttavia, se si esegue una query sulla proprietà quando il riconoscimento vocale è disabilitato, il server non avvia i servizi voce.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**Metodo Listen**](listen-method.md)


 

 




