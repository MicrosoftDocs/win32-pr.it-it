---
description: È possibile usare il Registro di sistema per specificare che l'esplorazione in un punto di giunzione aprirà una visualizzazione radice anziché la visualizzazione predefinita del contenuto dell'estensione associata.
title: Come aprire una visualizzazione radice di un punto di giunzione tramite il Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f575d4265a207e97c20f0c2a42456ddbf55cebbe5a0d42664c1fdfa9f5986d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593161"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Come aprire una visualizzazione radice di un punto di giunzione tramite il Registro di sistema

È possibile usare il Registro di sistema per specificare che l'esplorazione in un punto di giunzione aprirà una visualizzazione radice anziché la visualizzazione predefinita del contenuto dell'estensione associata.

## <a name="instructions"></a>Istruzioni


Per specificare che l'esplorazione in un punto di giunzione deve aprire una visualizzazione radice, aggiungere le sottochiavi Open Command ed Explore Command alla sottochiave \\   \\  **CLSID** dell'estensione, con i relativi valori predefiniti assegnati alle righe di comando illustrate di seguito:

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

Dopo aver aggiunto questi valori, viene avviata un'istanza di Explorer.exe per visualizzare il contenuto dell'estensione come visualizzazione radice quando l'utente seleziona il punto di giunzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica del percorso di un'estensione dello spazio dei nomi](nse-junction.md)
</dt> <dt>

[Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



