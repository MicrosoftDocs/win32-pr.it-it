---
description: Il metodo PlayForwards avvia la riproduzione in avanti dalla posizione corrente alla velocità specificata.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Metodo PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e607779147ba057b9cfd747ebfe827a25e294e2b04cdfa7e61a0691ecf293c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830631"
---
# <a name="playforwards-method"></a>Metodo PlayForwards

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayForwards` metodo avvia la riproduzione in avanti dalla posizione corrente alla velocità specificata.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Specifica la velocità alla quale eseguire la riproduzione come valore Integer. Questo valore è un moltiplicatore, ovvero 1,0 è la velocità di riproduzione normale. 2.0 è a doppia velocità, 0,5 è a metà velocità e così via. Quando **nSpeed** non è uguale a 1.0, l'audio viene disattivato e l'immagine secondaria viene disattivata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



