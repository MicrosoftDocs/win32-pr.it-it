---
description: Il passaggio finale consiste nell'inserire un riferimento al Setup.exe nella ipotetica pagina Web MySetup (MySetup.html) descritta in Esempio di installazione del programma di installazione Windows basato su URL.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Stabilire un riferimento HTML per Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22be693c4e2e411fa724a70f90da4af4af4cf17ad6bb316bd3a483dd55bfd5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378071"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Stabilire un riferimento HTML per Setup.exe

Il passaggio finale consiste nell'inserire un riferimento al Setup.exe nell'ipotetico sito Web MySetup (MySetup.html) descritto in Esempio di installazione del programma di installazione basato su [URL Windows](a-url-based-windows-installer-installation-example.md). Usare lo script HTML seguente:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Facendo clic sul collegamento "Installazione mySetup" gli utenti possono scegliere di salvare o eseguire da tale percorso. Se l'utente seleziona Esegui da tale percorso, il Setup.exe aggiorna la versione del programma di installazione di Windows nel computer, se necessario, verifica la firma digitale nel pacchetto del programma di installazione e installa il pacchetto nel computer.

L'esempio viene completato.

 

 



