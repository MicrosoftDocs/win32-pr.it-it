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
- MIXERCONTROLDETAILS_BOOLEAN struttura
- MIXERCONTROLDETAILS_LISTTEXT struttura
- controllo a selezione singola
- Controllo a selezione multipla
- controllo mixer
- multiplexer (MUX)
- MUX (multiplexer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f15e1c89e564ddd3b6c263b91242a3e4dc0382fd36f86554ec6bd0556191ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139396"
---
# <a name="lists"></a>Elenchi

I controlli elenco forniscono stati a selezione singola o a selezione multipla per linee audio complesse. Questi controlli usano la [**struttura BOOLEAN MIXERCONTROLDETAILS \_**](/previous-versions//dd757295(v=vs.85)) per recuperare e impostare le proprietà del controllo. La [**struttura MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) viene usata anche per recuperare tutte le descrizioni di testo di un controllo con più elementi. La tabella seguente descrive i tipi di controlli elenco.



| Controllo           | Descrizione                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Selezione singola     | Limita la selezione del controllo a un elemento alla volta. A differenza del controllo multiplexer, questo controllo può essere usato per controllare più righe di origine audio. Ad esempio, è possibile usare questo controllo per selezionare un filtro a passaggio ridotto da un elenco di filtri supportati da un dispositivo mixer. |
| Multiplexer (MUX) | Limita la selezione della riga a una riga di origine alla volta.                                                                                                                                                                                                                       |
| Selezione multipla   | Consente all'utente di selezionare più elementi da un elenco contemporaneamente. A differenza del controllo mixer, il controllo a selezione multipla può essere usato per controllare più righe di origine audio.                                                                                                  |
| Mixer             | Consente all'utente di selezionare le righe di origine da un elenco contemporaneamente.                                                                                                                                                                                                               |



 

 

 