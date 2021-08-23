---
description: L'evento UpdateOverlay viene inviato quando la superficie di sovrapposizione è stata spostata o ridimensionata o la relativa chiave di colore è stata modificata.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (Ddraw.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205b4ca002ec06862b006dc3e3b6facec2f5cb7f0ffb92f3e5a65bc2bb0a161c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650826"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

**L'evento UpdateOverlay** viene inviato quando la superficie di sovrapposizione è stata spostata o ridimensionata o la relativa chiave di colore è stata modificata.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Commenti

Le applicazioni non devono mai preoccuparsi del ridimensionamento o dello spostamento della superficie di sovrapposizione. Tutto questo viene gestito internamente. Ma questo evento viene inviato anche quando cambia la chiave di colore. Ciò significa che se un'applicazione ospita MSWebDVD come controllo senza finestra e visualizza pulsanti mobili sulla superficie video in modalità schermo intero, deve rispondere a questo evento ottenendo il nuovo valore della proprietà **ColorKey** in modo che possa disegnare correttamente i pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ddraw.h</dt> </dl> |



 

 




