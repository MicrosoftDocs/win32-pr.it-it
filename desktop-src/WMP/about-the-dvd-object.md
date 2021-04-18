---
title: Informazioni sull'oggetto DVD
description: Informazioni sull'oggetto DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player, oggetto DVD
- Modello a oggetti di Windows Media Player, oggetto DVD
- modello a oggetti, oggetto DVD
- Controllo ActiveX Windows Media Player, oggetto DVD
- Controllo ActiveX, oggetto DVD
- Controllo ActiveX Windows Media Player Mobile, oggetto DVD
- Windows Media Player Mobile, oggetto DVD
- Oggetto DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328524"
---
# <a name="about-the-dvd-object"></a>Informazioni sull'oggetto DVD

L'oggetto **DVD** aggiunge funzionalità specifiche dei supporti DVD. In generale, i supporti DVD sono trattati come altri supporti digitali in Windows Media Player. Ad esempio, le unità DVD vengono enumerate usando l'oggetto **cdromcollection** e i titoli e i capitoli dei DVD vengono modificati usando oggetti della **playlist** e oggetti **multimediali** . Alcune funzionalità sono tuttavia specifiche del DVD e l'oggetto **DVD** lo fornisce. Ad esempio, il DVD ha un concetto denominato dominio. Per recuperare il dominio corrente per i supporti DVD, digitare quanto segue:


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




