---
description: La proprietà AnglesAvailable Recupera il numero di angoli attualmente disponibili.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Proprietà AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304152"
---
# <a name="anglesavailable-property"></a>Proprietà AnglesAvailable

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `AnglesAvailable` proprietà recupera il numero di angoli attualmente disponibili.

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero compreso tra 1 e 9 che rappresenta il numero di angoli attualmente disponibili. Se


```
iAngles
```



= 1, nessun blocco angolo nella posizione corrente.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. Un *blocco Angle* è un segmento video che è stato ripreso da più di un angolo della fotocamera. In un blocco angolo possono essere presenti fino a nove angoli, numerati da 1 a 9. Quando il navigatore DVD passa per la prima volta a un blocco angolo, invia all'applicazione una \_ \_ \_ notifica degli eventi disponibili per gli angoli di DVD EC con il numero di angoli in *lParam1*. È possibile creare un disco per visualizzare automaticamente un menu per gli angoli disponibili quando entra in un blocco angolo, ma in genere un'applicazione deve determinare il numero di angoli disponibili e fornire all'utente un modo per selezionarne uno.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CurrentAngle**](currentangle-property.md)
</dt> </dl>

 

 



