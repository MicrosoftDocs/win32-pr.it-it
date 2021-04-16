---
description: Il metodo zoom consente di ingrandire o ridurre la visualizzazione del video, centrata su un determinato set di coordinate dello schermo.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom (metodo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485637"
---
# <a name="zoom-method"></a>Zoom (metodo)

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `Zoom` metodo consente di ingrandire o ridurre la visualizzazione del video, centrata su un determinato set di coordinate dello schermo.

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*
</dt> <dd>

Specifica la coordinata x al centro dell'area di zoom rettangolare come valore integer.

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*
</dt> <dd>

Specifica la coordinata y al centro del rettangolo da ingrandire come Integer.

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*
</dt> <dd>

Specifica il fattore di ingrandimento applicato al valore di zoom corrente come intero. Il valore massimo totale dipende da ciò che la sovrimpressione hardware può supportare. si tratta in genere di un fattore da 32 a 64 volte le dimensioni originali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il nuovo rapporto di zoom rimane attivo fino a quando non viene ripristinato alla dimensione originale o nuovamente modificato. In altre parole, due chiamate a questo metodo che specificano un *iZoomRatio* di due comporteranno un rapporto di zoom quattro volte maggiore delle dimensioni del video originale. Se l'utente tenta di ingrandire i dati che l'hardware può supportare, questo metodo avrà esito positivo, ma non eseguirà alcuna operazione.

Il metodo [**SetClipVideoRect**](setclipvideorect-method.md) è un altro modo per eseguire lo zoom avanti; l'unica differenza tra i due metodi è il modo in cui viene specificato il rettangolo di zoom.

 

 



