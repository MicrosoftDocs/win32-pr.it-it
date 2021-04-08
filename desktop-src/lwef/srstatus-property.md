---
title: Proprietà SRStatus
description: Proprietà SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045382"
---
# <a name="srstatus-property"></a>Proprietà SRStatus

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se è possibile avviare l'input vocale per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri ("*** CharacterID * * *"). SRStatus**



| Valore | Descrizione                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Le condizioni supportano l'input vocale.                                                                                                                                                                                                          |
| 1     | Nessun dispositivo di input audio disponibile nel sistema. Si noti che questo non rileva se un microfono è installato; può solo rilevare se l'utente dispone di una scheda audio abilitata per l'input correttamente installata con un driver funzionante. |
| 2     | Un altro client è il client attivo di questo carattere oppure il carattere corrente non è in primo piano.                                                                                                                                           |
| 3     | Il canale di input o di output audio è attualmente occupato, un'applicazione sta usando audio.                                                                                                                                                       |
| 4     | Si è verificato un errore non specificato durante il processo di inizializzazione del sottosistema di riconoscimento vocale. Ciò include la possibilità che non sia disponibile un motore di riconoscimento vocale corrispondente all'impostazione della lingua del carattere.                          |
| 5     | L'utente ha disabilitato l'input vocale nelle opzioni dei caratteri avanzati.                                                                                                                                                                     |
| 6     | Si è verificato un errore durante il controllo dello stato dell'audio, ma la cause dell'errore non è stata restituita dal sistema.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà restituisce le condizioni necessarie per supportare l'input vocale, incluso lo stato del dispositivo audio. È possibile controllare questa proprietà prima di chiamare il metodo [**Listen**](listen-method.md) per garantirne l'esito positivo.

Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'esecuzione di una query su questa proprietà caricherà il motore associato, se non è già caricato, e avvierà servizi vocali. Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è automaticamente visualizzabile. (Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**Listen (metodo)**](listen-method.md)


 

 




