---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398648"
---
# <a name="ittsnotifysinkw"></a>ITTSNotifySinkW

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il motore deve chiamare tramite [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)e [**Visual**](https://www.bing.com/search?q=**Visual**). Il callback **visivo** deve fornire fonemi IPA. (Alfabeto \[ fonetico internazionale) IPA \] è una notazione universale per la descrizione del contenuto fonetico della comunicazione parlata. Tutti i fonemi pronunciabili presentano rappresentazioni in IPA. I dettagli del pacchetto IPA si trovano nella parte relativa alla specifica di Microsoft Speech API \[ del download per Speech SDK 4,0 \] all'indirizzo [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .

Sebbene la notifica [**visiva**](https://www.bing.com/search?q=**Visual**) sia abbastanza ricca, Microsoft Agent utilizza solo il valore **cIPAPhoneme** per animare la bocca quando il carattere parla. Qualsiasi motore compatibile con Microsoft Agent deve fornire un flusso strettamente sincronizzato di notifiche **visive** che riflettono il contenuto fonetico della parola prodotta. In questo caso, "notifica relativamente tempestiva" non è adeguata, perché i relatori sono piuttosto sensibili alle discrepanze tra la posizione della bocca e il contenuto acustico. Le notifiche **visive** devono essere restituite tempestivamente.

 

 




