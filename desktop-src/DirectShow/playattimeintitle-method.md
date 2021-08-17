---
description: Il metodo PlayAtTimeInTitle avvia la riproduzione all'ora specificata all'interno del titolo specificato.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Metodo PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33640733f7333395a4affc4dedc0ae8db3e3558bf066584cb603dfc5f906f73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291270"
---
# <a name="playattimeintitle-method"></a>Metodo PlayAtTimeInTitle

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `PlayAtTimeInTitle` metodo avvia la riproduzione all'ora specificata all'interno del titolo specificato.

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*
</dt> <dd>

Specifica l'ora in cui avviare la riproduzione come stringa. La stringa deve essere nel formato "hh:mm:ss:ff" (specificando ore, minuti, secondi, fotogrammi).

</dd> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Specifica l'indice del titolo come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CurrentTitle**](currenttitle-property.md)
</dt> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**TitlesAvailable**](titlesavailable-property.md)
</dt> </dl>

 

 



