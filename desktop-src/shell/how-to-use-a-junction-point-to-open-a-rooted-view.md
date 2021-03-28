---
description: È possibile utilizzare il registro di sistema per specificare che l'esplorazione in un punto di giunzione apre una vista radice anziché la visualizzazione predefinita del contenuto dell'estensione associata.
title: Come aprire una visualizzazione radice di un punto di giunzione tramite il registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227431"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Come aprire una visualizzazione radice di un punto di giunzione tramite il registro di sistema

È possibile utilizzare il registro di sistema per specificare che l'esplorazione in un punto di giunzione apre una vista radice anziché la visualizzazione predefinita del contenuto dell'estensione associata.

## <a name="instructions"></a>Istruzioni


Per specificare che l'esplorazione in un punto di giunzione deve aprire una visualizzazione con radice , aggiungere il \\ **comando** Apri ed **esplorare** le \\ sottochiavi dei **comandi** alla sottochiave **CLSID** dell'estensione, con i valori predefiniti assegnati alle righe di comando illustrate di seguito:

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         Shell
            Open
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
            Explore
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
```

Una volta aggiunti tali valori, viene avviata un'istanza di Explorer.exe per visualizzare il contenuto dell'estensione come visualizzazione radice quando l'utente seleziona il punto di giunzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della posizione di un'estensione dello spazio dei nomi](nse-junction.md)
</dt> <dt>

[Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



