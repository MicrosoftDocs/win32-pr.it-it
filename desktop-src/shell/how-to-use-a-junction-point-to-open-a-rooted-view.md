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
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a><span data-ttu-id="b9f13-103">Come aprire una visualizzazione radice di un punto di giunzione tramite il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b9f13-103">How to Open a Rooted View of a Junction Point Through the Registry</span></span>

<span data-ttu-id="b9f13-104">È possibile utilizzare il registro di sistema per specificare che l'esplorazione in un punto di giunzione apre una vista radice anziché la visualizzazione predefinita del contenuto dell'estensione associata.</span><span class="sxs-lookup"><span data-stu-id="b9f13-104">You can use the registry to specify that browsing into a junction point will open a rooted view rather than the default view of the contents of the associated extension.</span></span>

## <a name="instructions"></a><span data-ttu-id="b9f13-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="b9f13-105">Instructions</span></span>


<span data-ttu-id="b9f13-106">Per specificare che l'esplorazione in un punto di giunzione deve aprire una visualizzazione con radice , aggiungere il \\ **comando** Apri ed **esplorare** le \\ sottochiavi dei **comandi** alla sottochiave **CLSID** dell'estensione, con i valori predefiniti assegnati alle righe di comando illustrate di seguito:</span><span class="sxs-lookup"><span data-stu-id="b9f13-106">To specify that browsing into a junction point should open a rooted view, add **Open**\\**Command** and **Explore**\\**Command** subkeys to your extension's **CLSID** subkey, with their default values assigned to the command lines shown here:</span></span>

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

<span data-ttu-id="b9f13-107">Una volta aggiunti tali valori, viene avviata un'istanza di Explorer.exe per visualizzare il contenuto dell'estensione come visualizzazione radice quando l'utente seleziona il punto di giunzione.</span><span class="sxs-lookup"><span data-stu-id="b9f13-107">Once you've added those values, an instance of Explorer.exe is launched to display the contents of the extension as a rooted view when the user selects the junction point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9f13-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9f13-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9f13-109">Impostazione della posizione di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b9f13-109">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="b9f13-110">Come aprire una visualizzazione radice di un punto di giunzione tramite un file di collegamento</span><span class="sxs-lookup"><span data-stu-id="b9f13-110">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



