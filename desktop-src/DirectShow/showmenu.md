---
description: L'evento ShowMenu viene inviato quando il disco abilita o disabilita la visualizzazione di un menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56eb6767a8144bab3de832570db63bc4e2cdc012490f776f52b6c8977cce9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050451"
---
# <a name="showmenu"></a>ShowMenu

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

`ShowMenu`L'evento viene inviato quando il disco abilita o disabilita la visualizzazione di un menu.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

Specifica quale menu è stato abilitato o disabilitato come valore Number.



| Valore | Descrizione |
|-------|-------------|
| 2     | Titolo       |
| 3     | Radice        |
| 4     | Immagine secondaria  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Capitolo     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Specifica se l'operazione è abilitata o disabilitata come valore booleano.

</dd> </dl>

 

 



