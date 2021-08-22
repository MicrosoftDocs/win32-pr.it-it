---
title: Accesso al controllo da Visual Basic e altri linguaggi di programmazione
description: Accesso al controllo da Visual Basic e altri linguaggi di programmazione
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fe0c5e7548283a84edff1fb3ded488c1367087e12c15d1578629ce80b51297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976861"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Accesso al controllo da Visual Basic e altri linguaggi di programmazione

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

È anche possibile usare il controllo di Microsoft Agent da Visual Basic e da altri linguaggi di programmazione. Assicurarsi che il linguaggio supporti completamente l'ActiveX di controllo e segua le convenzioni per l'aggiunta e l'accesso ActiveX controlli . Per accedere al controllo, Agent deve essere già installato nel sistema di destinazione.

È quindi possibile scaricare il file CAB auto-installazione di Agent dal sito Web (usando l'opzione Salva anziché Esegui). È possibile includere questo file nel programma di installazione di . Ogni volta che viene eseguito, Agent verrà installato automaticamente nel sistema di destinazione. Per altre informazioni sull'installazione, vedere il contratto di licenza per la distribuzione di Microsoft Agent. L'installazione diversa dall'uso del file CAB autoinstallato di Agent, ad esempio il tentativo di copiare e registrare i file dei componenti di Agent, non è supportata. In questo modo si garantisce un'installazione coerente e completa. Si noti che il file auto-installazione di Microsoft Agent non verrà installato in Microsoft Windows 2000 perché tale versione del sistema operativo include già la propria versione di Agent.

Per installare correttamente Agent in un sistema di destinazione, è inoltre necessario assicurarsi che il sistema di destinazione abbia una versione recente del runtime di Microsoft Visual C++ (Msvcrt.dll), dello strumento di registrazione Microsoft (Regsvr32.dll) e delle DLL COM Microsoft. Il modo più semplice per assicurarsi che i componenti necessari siano nel sistema di destinazione è richiedere l'installazione di Microsoft Internet Explorer 3.02 o versione successiva. In alternativa, è possibile installare i primi due componenti disponibili come parte di Microsoft Visual C++. Le DLL COM necessarie possono essere installate come parte dell'aggiornamento di Microsoft DCOM, disponibile nel sito Web Microsoft. Altre informazioni e informazioni sulle licenze per questi componenti sono disponibili nel sito Web Microsoft.

I componenti del linguaggio di Agent possono essere installati nello stesso modo. Analogamente, è possibile usare questa tecnica per installare il formato ACS dei caratteri Microsoft disponibili per la distribuzione dal sito Web Microsoft Agent. I file di caratteri vengono installati automaticamente nella \\ sottodirectory Chars di Microsoft Agent.

Poiché i componenti di Microsoft Agent sono progettati come componenti del sistema operativo, Agent potrebbe non essere disinstallato. Analogamente, se Agent è già installato come parte del Windows operativo, è possibile che l'archivio auto-installazione di Agent non venga installato.

 

 




