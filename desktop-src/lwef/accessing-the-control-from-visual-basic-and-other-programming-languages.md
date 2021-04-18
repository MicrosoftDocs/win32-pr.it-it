---
title: Accesso al controllo da Visual Basic e altri linguaggi di programmazione
description: Accesso al controllo da Visual Basic e altri linguaggi di programmazione
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45854b55b3826354543411c44dcd21d9f1d77e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298564"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Accesso al controllo da Visual Basic e altri linguaggi di programmazione

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

È anche possibile usare il controllo di Microsoft Agent da Visual Basic e altri linguaggi di programmazione. Verificare che il linguaggio supporti completamente l'interfaccia di controllo ActiveX e seguire le convenzioni per l'aggiunta e l'accesso ai controlli ActiveX. Per accedere al controllo, Agent deve essere già installato nel sistema di destinazione.

È quindi possibile scaricare il file CAB di installazione automatica dell'agente dal sito Web usando l'opzione Salva anziché Esegui. Questo file può essere incluso nel programma di installazione dell'installazione. Ogni volta che viene eseguita, l'agente verrà installato automaticamente nel sistema di destinazione. Per ulteriori informazioni sull'installazione, vedere il contratto di licenza per la distribuzione di Microsoft Agent. Non è supportata l'installazione di un file CAB con installazione automatica di Agent, ad esempio il tentativo di copiare e registrare i file dei componenti dell'agente. In questo modo si garantisce un'installazione coerente e completa. Si noti che il file di installazione automatica di Microsoft Agent non viene installato in Microsoft Windows 2000, perché tale versione del sistema operativo include già la propria versione dell'agente.

Per installare correttamente Agent in un sistema di destinazione, è inoltre necessario assicurarsi che il sistema di destinazione disponga di una versione recente di Microsoft Visual C++ Runtime (Msvcrt.dll), Microsoft Registration Tool (Regsvr32.dll) e dll Microsoft COM. Il modo più semplice per garantire che i componenti necessari si trovino sul sistema di destinazione, è necessario che sia installato Microsoft Internet Explorer 3,02 o versione successiva. In alternativa, è possibile installare i primi due componenti disponibili come parte del Microsoft Visual C++. Le DLL COM necessarie possono essere installate come parte dell'aggiornamento Microsoft DCOM, disponibile nel sito Web Microsoft. Per ulteriori informazioni e informazioni sulle licenze per questi componenti, vedere il sito Web Microsoft.

I componenti della lingua dell'agente possono essere installati nello stesso modo. Analogamente, è possibile utilizzare questa tecnica per installare il formato ACS dei caratteri Microsoft disponibili per la distribuzione dal sito Web Microsoft Agent. I file di caratteri vengono installati automaticamente nella \\ sottodirectory chars di Microsoft Agent.

Poiché i componenti di Microsoft Agent sono progettati come componenti del sistema operativo, Agent potrebbe non essere disinstallato. Analogamente, in cui Agent è già installato come parte del sistema operativo Windows, è possibile che il cabinet di installazione automatica dell'agente non venga installato.

 

 




