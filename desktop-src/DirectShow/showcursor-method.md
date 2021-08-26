---
description: Il metodo ShowCursor rende visibile il cursore quando l'oggetto MSWebDVD è in modalità schermo intero.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Metodo ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3013392a5dcea2b3c4c9af8ee94d54c540814b5f4221563429ee7c837dcdddd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050521"
---
# <a name="showcursor-method"></a>Metodo ShowCursor

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `ShowCursor` metodo rende visibile il cursore quando l'oggetto **MSWebDVD** è in modalità schermo intero.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*Bshow*
</dt> <dd>

Specifica se visualizzare il cursore come valore booleano.



| Valore | Descrizione            |
|-------|------------------------|
| true  | Mostra il cursore        |
| false | Non visualizzare il cursore |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando lo schermo DVD passa alla modalità schermo intero, il cursore scompare entro 3-5 secondi. Usare questo metodo per rendere nuovamente visibile il cursore se i pulsanti di controllo dell'applicazione sono visibili in modalità schermo intero.

 

 



