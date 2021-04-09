---
title: Tipo di pulsante
description: Tipo di pulsante
ms.assetid: 0c9e72d5-5cc4-4d6f-b184-2c8c8487e366
keywords:
- Interfacce di Windows Media Player Mobile, tipi di pulsanti
- interfacce, tipi di pulsanti
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58eeb7402a13730fd7f4030d2e4326fe7f18e63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855682"
---
# <a name="button-type"></a>Tipo di pulsante

I pulsanti sono disponibili in due tipi generali: località e area. Ogni tipo generale è costituito da tre tipi specifici, rendendo tutti sei tipi di pulsante in tutti.

> [!Note]  
> I tipi di pulsanti sono deprecati nelle interfacce per Windows Media Player 10 mobile o versioni successive.

 

Tipi di pulsante location

I pulsanti percorso utilizzano le coordinate per definire le rispettive posizioni rispetto allo sfondo. La tabella seguente illustra i valori validi per i tipi di pulsante location. Non è necessario definire i valori per i tipi che non verranno usati nell'interfaccia utente.



| Valore  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Push   | Definisce un pulsante che attiva un evento una sola volta. È necessario eseguire il push del pulsante ogni volta per attivare ulteriori eventi. Un esempio potrebbe essere un pulsante che passa all'elemento successivo nella playlist. Il percorso del pulsante è definito dalle relative coordinate.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Toggle | Definisce un pulsante che attiva un evento che modifica uno stato. Lo stato rimane fino a quando non viene nuovamente premuto il pulsante. Un esempio è un pulsante che mischia la playlist. Quando la playlist è in uno stato casuale, rimarrà casuale fino a quando non si preme di nuovo il pulsante. Il percorso del pulsante è definito dalle relative coordinate.                                                                                                                                                                                                                                                                                                                                                           |
| 2Push  | Definisce un pulsante che attiva un evento, quindi passa a uno stato pronto per attivare un evento diverso. I due stati vengono spostati ogni volta che viene premuto il pulsante. Un esempio è un pulsante che usa la funzione **come playpause** per passare dalla riproduzione alla sospensione dell'elemento multimediale corrente e viceversa. Quando si preme il pulsante per la prima volta, viene attivato lo stato di riproduzione principale e viene visualizzata un'immagine secondaria per indicare che è possibile attivare un evento di **sospensione** . Quando si preme di nuovo il pulsante, viene attivato lo stato di sospensione e viene visualizzata l'immagine originale per indicare che è possibile attivare un evento di **riproduzione** . Il percorso del pulsante è definito dalle relative coordinate. |



 

Tipi di pulsante Region

I pulsanti area usano aree dei colori nell'immagine dell'area per definire dove verranno elaborati i rubinetti per un pulsante specifico. La tabella seguente illustra i valori validi per i tipi di pulsante Region. Non è necessario definire i valori per i tipi che non verranno usati nell'interfaccia utente.



| Valore     | Descrizione                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| PushHit   | Simile al valore del pulsante di push, tranne per il fatto che l'area di hit del pulsante è definita dal valore del colore nell'immagine dell'area.   |
| ToggleHit | Simile al valore dell'interruttore, ad eccezione del fatto che l'area di hit del pulsante è definita dal valore del colore nell'immagine dell'area. |
| 2PushHit  | Simile al valore del pulsante 2Push, tranne per il fatto che l'area di hit del pulsante è definita dal valore del colore nell'immagine dell'area.  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




