---
description: Il metodo PlayBackwards avvia la riproduzione all'indietro dalla posizione corrente alla velocità specificata.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Metodo PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7236c225858d9508da0074ea64d104a50632b772302f42362dae373a987c352
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748361"
---
# <a name="playbackwards-method"></a>Metodo PlayBackwards

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayBackwards` metodo avvia la riproduzione all'indietro dalla posizione corrente alla velocità specificata.

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Specifica la velocità di riproduzione come numero. Questo numero è un moltiplicatore: 1,0 è la velocità di riproduzione normale; 2.0 è a doppia velocità, 0,5 è a metà velocità e così via. Quando **nSpeed non** è uguale a 1.0, l'audio viene disattivato e l'immagine secondaria viene disattivata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayForwards**](playforwards-method.md)
</dt> </dl>

 

 



