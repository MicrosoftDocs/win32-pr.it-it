---
description: Il metodo SaveBookmark salva la posizione del disco corrente e lo stato dell'oggetto MSWebDVD in modo che l'utente possa tornare alla stessa posizione in un secondo momento.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Metodo SaveBookmark (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326988"
---
# <a name="savebookmark-method"></a>Metodo SaveBookmark

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SaveBookmark` metodo salva la posizione del disco corrente e lo stato dell'oggetto **mswebdvd** in modo che l'utente possa tornare alla stessa posizione in un secondo momento.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un segnalibro è uno snapshot dello stato corrente del navigatore DVD. Sono incluse informazioni quali la posizione di riproduzione sul disco e i flussi audio e immagini secondarie selezionate. Salvando un segnalibro, l'utente può chiudere l'applicazione, arrestare il computer e tornare più tardi per continuare a visualizzare il disco da dove è stato interrotto, con tutte le impostazioni esattamente come prima. È possibile salvare un solo segnalibro in un determinato momento. Quando si chiama `SaveBookmark` , il segnalibro precedente viene sovrascritto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




