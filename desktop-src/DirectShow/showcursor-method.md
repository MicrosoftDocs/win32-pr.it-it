---
description: Il metodo ShowCursor rende visibile il cursore quando l'oggetto MSWebDVD è in modalità schermo intero.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Metodo ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876642"
---
# <a name="showcursor-method"></a>Metodo ShowCursor

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `ShowCursor` metodo rende il cursore visibile quando l'oggetto **mswebdvd** è in modalità schermo intero.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*
</dt> <dd>

Specifica se mostrare il cursore come valore booleano.



| Valore | Descrizione            |
|-------|------------------------|
| true  | Mostra il cursore        |
| false | Non visualizzare il cursore |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando la visualizzazione DVD passa alla modalità schermo intero, il cursore scompare tra 3 e 5 secondi. Utilizzare questo metodo per rendere nuovamente visibile il cursore se i pulsanti di controllo dell'applicazione sono visibili in modalità schermo intero.

 

 



