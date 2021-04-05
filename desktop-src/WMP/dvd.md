---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, migrazione di DVD
- Modello a oggetti di Windows Media Player, DVD
- modello a oggetti, DVD
- Controllo ActiveX di Windows Media Player, DVD
- Controllo ActiveX, DVD
- Controllo ActiveX Windows Media Player Mobile, DVD
- Windows Media Player Mobile, migrazione di DVD
- Guida alla migrazione, DVD
- Migrazione di DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711626"
---
# <a name="dvd"></a>DVD

Il controllo ActiveX Windows Media Player 6,4 contiene un oggetto **DVD** che espone un'ampia gamma di metodi e proprietà e un evento per la gestione specifica del contenuto DVD. Ad esempio, per determinare il numero di titoli DVD disponibili, usare **Player6**. proprietà **titlesAvailable** :


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



Il modello a oggetti di Windows Media Player 7 o versione successiva implementa un approccio più integrato a DVD. Proprietà, metodi ed eventi specifici per DVD sono implementati solo se necessario. In caso contrario, la funzionalità del modello a oggetti esistente funziona con supporti DVD come previsto. Per determinare, ad esempio, il numero di titoli DVD disponibili quando si usa Windows Media Player 7 o versione successiva, è possibile recuperare un oggetto **playlist** dall'oggetto **CDROM** :


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



Nell'esempio precedente viene recuperato un oggetto **playlist** con una prima voce che rappresenta il supporto DVD nella prima unità. Le voci aggiuntive rappresentano i singoli titoli di DVD. Il numero di titoli disponibili può pertanto essere calcolato come segue:


```C++
var numTitles = dvdTitles.count - 1;

```



Di seguito sono riportate le principali differenze da tenere presenti durante la migrazione dalla versione 6,4:

-   La riproduzione di DVD è supportata solo quando si usa Windows Media Player per Windows XP o versione successiva e il sistema operativo Windows XP o versione successiva.
-   Le unità DVD-ROM vengono enumerate esattamente come le unità CD-ROM usando l'oggetto **cdromcollection** .
-   Le singole unità DVD-ROM vengono gestite tramite l'oggetto **CDROM** .
-   L'oggetto **DVD** estende il modello a oggetti con i metodi e una proprietà specifica per l'utilizzo di DVD.
-   Sono disponibili due nuovi eventi, **OpenPlaylistSwitch** e **DomainChange**, in particolare per l'uso di DVD.
-   Il contenuto del DVD è organizzato usando oggetti della **playlist** e oggetti **multimediali** .
-   Le lingue DVD sono gestite usando le funzionalità del linguaggio disponibili nell'oggetto **Controls** (Windows Media Player 9 Series o versione successiva).
-   I controlli di trasporto e le informazioni sulla posizione per il DVD funzionano come per altri tipi di supporti digitali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows con Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




