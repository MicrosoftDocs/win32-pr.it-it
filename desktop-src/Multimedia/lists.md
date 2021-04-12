---
title: Elenchi
description: Elenchi
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- mixer audio, controlli
- mixer audio, elenchi
- mixer, controlli
- mixer, elenchi
- controlli elenco
- Struttura MIXERCONTROLDETAILS_BOOLEAN
- Struttura MIXERCONTROLDETAILS_LISTTEXT
- controllo a selezione singola
- controllo a selezione multipla
- controllo mixer
- Multiplexer (MUX)
- MUX (Multiplexer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336999"
---
# <a name="lists"></a>Elenchi

I controlli elenco forniscono gli Stati a selezione singola o multipla per le linee audio complesse. Questi controlli utilizzano la [**struttura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) per recuperare e impostare le proprietà del controllo. La [**struttura \_ LISTTEXT di MIXERCONTROLDETAILS**](/previous-versions//dd757296(v=vs.85)) viene usata anche per recuperare tutte le descrizioni di testo di un controllo di più elementi. Nella tabella seguente vengono descritti i tipi di controlli elenco.



| Controllo           | Descrizione                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selezione singola     | Limita la selezione del controllo a un elemento alla volta. A differenza del controllo multiplexer, questo controllo può essere usato per controllare più di righe di origine audio. Ad esempio, è possibile usare questo controllo per selezionare un filtro low-pass da un elenco di filtri supportati da un dispositivo mixer. |
| Multiplexer (MUX) | Limita la selezione di riga a una riga di origine alla volta.                                                                                                                                                                                                                       |
| Selezione multipla   | Consente all'utente di selezionare più elementi contemporaneamente da un elenco. A differenza del controllo mixer, il controllo a selezione multipla può essere usato per controllare più di righe di origine audio.                                                                                                  |
| Mixer             | Consente all'utente di selezionare le righe di origine da un elenco simultaneamente.                                                                                                                                                                                                               |



 

 

 