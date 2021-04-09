---
description: L'evento ShowMenu viene inviato quando il disco Abilita o Disabilita la visualizzazione di un menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965713"
---
# <a name="showmenu"></a>ShowMenu

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

L' `ShowMenu` evento viene inviato quando il disco Abilita o Disabilita la visualizzazione di un menu.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

Specifica quale menu è stato abilitato o disabilitato come valore numerico.



| Valore | Descrizione |
|-------|-------------|
| 2     | Titolo       |
| 3     | Radice        |
| 4     | Sottoimmagine  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Capitolo     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Specifica se l'operazione è abilitata o disabilitata come valore booleano.

</dd> </dl>

 

 



