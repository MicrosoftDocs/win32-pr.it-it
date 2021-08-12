---
title: Informazioni sull'oggetto DVD
description: Informazioni sull'oggetto DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player,OGGETTO DVD
- Windows Media Player a oggetti, oggetto DVD
- modello a oggetti, oggetto DVD
- Windows Media Player ActiveX, oggetto DVD
- ActiveX, oggetto DVD
- Windows Media Player Mobile ActiveX control,DVD object
- Windows Media Player Mobile, oggetto DVD
- Oggetto DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109587f30e7df0ff49b1cdbe5b45d818decb1a3f50ffe4a4ba9cde53d00833f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583763"
---
# <a name="about-the-dvd-object"></a>Informazioni sull'oggetto DVD

**L'oggetto DVD** aggiunge funzionalità specifiche ai supporti DVD. In generale, i supporti DVD vengono trattati come altri supporti digitali in Windows Media Player. Ad esempio, le unità DVD vengono enumerate usando l'oggetto **CdromCollection** e i titoli e i capitoli dei DVD vengono manipolati usando oggetti **Playlist** e **oggetti** multimediali. Alcune funzionalità, tuttavia, sono specifiche del DVD e **l'oggetto DVD** lo fornisce. Ad esempio, DVD ha un concetto denominato dominio. Per recuperare il dominio corrente per i supporti DVD, digitare quanto segue:


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> <dt>

[**Modello a oggetti del lettore per linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




