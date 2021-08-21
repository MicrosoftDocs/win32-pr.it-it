---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86cedf8c4a349da800f34f2f6acd7266f9cd0c3c383be9accb72dd162df8e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748709"
---
# <a name="ittsnotifysinkw"></a>ITTSNotifySinkW

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il motore deve chiamare tramite [**AudioStop,**](https://www.bing.com/search?q=**AudioStop**) [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)e [**Visual**](https://www.bing.com/search?q=**Visual**). Il callback **visivo** deve fornire fonemi IPA. (Alfabeto fonetico internazionale \[ IPA \] è una notazione universale per descrivere il contenuto fonetico della comunicazione parlata. Tutti i fonemi parlabili hanno rappresentazioni in IPA. I dettagli di IPA sono inclusi nella specifica microsoft Speech API del download di \[ Speech SDK 4.0 \] [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) all'indirizzo .

Anche se [**la notifica**](https://www.bing.com/search?q=**Visual**) visiva è piuttosto ricca, Microsoft Agent usa solo il valore **cIPAPhoneme** per animare la bocca mentre parla il carattere. Qualsiasi motore compatibile con Microsoft Agent deve fornire  un flusso strettamente sincronizzato di notifiche visive che riflettono il contenuto fonetico dell'espressione prodotta. In questo caso, la "notifica relativamente temporale" non è adeguata, perché i parlanti sono piuttosto sensibili alle discrepanze tra la posizione della bocca e il contenuto acustico. **Le notifiche** visive devono essere restituite tempestivamente.

 

 




