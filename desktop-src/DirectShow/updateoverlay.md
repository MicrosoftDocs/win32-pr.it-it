---
description: L'evento UpdateOverlay viene inviato quando la superficie di sovrapposizione è stata spostata o ridimensionata o la chiave di colore è cambiata.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333303"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

L'evento **UpdateOverlay** viene inviato quando la superficie di sovrapposizione è stata spostata o ridimensionata o la chiave di colore è cambiata.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Commenti

Le applicazioni non dovrebbero mai preoccuparsi della superficie sovrapposta ridimensionata o spostata. Questa operazione viene gestita internamente. Questo evento viene tuttavia inviato anche quando cambia la chiave di colore. Ciò significa che se un'applicazione ospita MSWebDVD come controllo senza finestra e Visualizza i pulsanti mobili nella parte superiore della superficie video in modalità schermo intero, deve rispondere a questo evento ottenendo il nuovo valore della proprietà **ColorKey** in modo da poter creare correttamente i pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

 




