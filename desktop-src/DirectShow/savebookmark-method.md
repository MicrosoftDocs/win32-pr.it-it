---
description: Il metodo SaveBookmark salva la posizione del disco corrente e lo stato dell'oggetto MSWebDVD in modo che l'utente possa tornare nella stessa posizione in un secondo momento.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Metodo SaveBookmark (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fec3a109b97c0ccbcb9a98736a01bba625537f1369fa7986cb6b5a669d35b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072715"
---
# <a name="savebookmark-method"></a>Metodo SaveBookmark

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo salva la posizione del disco corrente e lo stato `SaveBookmark` **dell'oggetto MSWebDVD** in modo che l'utente possa tornare nella stessa posizione in un secondo momento.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un segnalibro è uno snapshot dello stato corrente dello strumento di navigazione DVD. Sono incluse informazioni come la posizione in cui viene riprodotto sul disco e i flussi audio e secondari selezionati. Salvando un segnalibro, l'utente può chiudere l'applicazione, arrestare il computer e tornare in un secondo momento per continuare a visualizzare il disco proprio dove si è spento, con tutte le impostazioni esattamente come prima. È possibile salvare un solo segnalibro in un determinato momento. Quando si chiama `SaveBookmark` , il segnalibro precedente viene sovrascritto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




