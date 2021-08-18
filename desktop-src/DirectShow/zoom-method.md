---
description: Il metodo Zoom consente di ingrandire o ridurre la visualizzazione video, centrata su un determinato set di coordinate dello schermo.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Metodo Zoom
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0c260e5a5404b65f4e0d0595a87ee78103c5acccedd32abf50fc5706c6b42f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632700"
---
# <a name="zoom-method"></a>Metodo Zoom

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo esegue lo zoom avanti o indietro della visualizzazione `Zoom` video, centrata su un determinato set di coordinate dello schermo.

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*
</dt> <dd>

Specifica la coordinata x al centro dell'area di zoom rettangolare come integer.

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*
</dt> <dd>

Specifica la coordinata y al centro del rettangolo da ingrandire come integer.

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*
</dt> <dd>

Specifica il fattore di ingrandimento applicato al valore di zoom corrente come Integer. Il valore massimo totale dipende da ciò che la sovrimpressione hardware può supportare; si tratta in genere di un fattore da 32 a 64 volte la dimensione originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il nuovo rapporto di zoom rimane attivo fino a quando non viene ripristinato alle dimensioni originali o modificato di nuovo. In altre parole, due chiamate a questo metodo che specificano *un oggetto iZoomRatio* di due avranno un rapporto di zoom quattro volte superiore alle dimensioni del video originale. Se l'utente tenta di eseguire lo zoom oltre ciò che l'hardware può supportare, questo metodo avrà esito positivo ma non esegue alcuna operazione.

Il [**metodo SetClipVideoRect**](setclipvideorect-method.md) è un altro modo per eseguire lo zoom avanti. l'unica differenza tra i due metodi è il modo in cui viene specificato il rettangolo di zoom.

 

 



