---
description: Il metodo PlayForwards avvia la riproduzione dalla posizione corrente alla velocità specificata.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Metodo PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746794"
---
# <a name="playforwards-method"></a>Metodo PlayForwards

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayForwards` metodo inizia la riproduzione dalla posizione corrente alla velocità specificata.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Specifica la velocità di riproduzione come valore intero. Questo valore è un moltiplicatore: 1.0 è la velocità di riproduzione normale; 2,0 è una doppia velocità, 0,5 è la metà della velocità e così via. Quando **nSpeed** non è uguale a 1,0, l'audio viene disattivato e la sottoimmagine è disattivata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



