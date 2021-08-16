---
title: PLAYLIST.rightStatus
description: L'attributo rightStatus specifica o recupera il testo di stato visualizzato sul lato destro e nella parte inferiore dell'elemento PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- PLAYLIST.rightStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29b79b0f4e3ad18ed4e044f894d63ec5059477f80999a8b96dc461d9499b29cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336564"
---
# <a name="playlistrightstatus"></a>PLAYLIST.rightStatus

**L'attributo rightStatus** specifica o recupera il testo di stato visualizzato sul lato destro e nella parte inferiore dell'elemento **PLAYLIST.**

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Questo attributo può combinare qualsiasi testo con parole chiave specifiche che visualizzano le informazioni desiderate, ad esempio la durata totale della playlist. Le parole chiave sono racchiuse tra simboli percentuali (%) per mantenerle distinte dal testo normale.

È possibile usare le parole chiave seguenti.



| Parola chiave               | Descrizione                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Numero di elementi nella playlist.                                                                                                                                                                             |
| size                  | Dimensioni totali della playlist.                                                                                                                                                                                  |
| duration              | Durata totale della playlist.                                                                                                                                                                              |
| *Xxx*                 | Esegue **un'operazione getItemInfo** nella playlist con *XXX* come elemento da ricevere.                                                                                                                                 |
| SelectedSize          | Dimensioni totali delle voci selezionate nella playlist.                                                                                                                                                          |
| SelectedCount         | Numero totale di voci selezionate nella playlist.                                                                                                                                                            |
| SelectedDuration      | Durata totale delle voci selezionate nella playlist.                                                                                                                                                      |
| CheckedCount          | Numero totale di tracce selezionate nella playlist.                                                                                                                                                              |
| CheckedDuration       | Durata totale delle tracce selezionate nella playlist.                                                                                                                                                        |
| CheckedSize           | Dimensioni totali delle tracce selezionate nella playlist.                                                                                                                                                            |
| DurationString        | Visualizza il testo che descrive la durata come "Tempo totale" o "Tempo stimato", a seconda che i valori totali siano noti. Questo testo è seguito da "%duration%".                                       |
| CheckedDurationString | Visualizza il testo che descrive la durata di tutti gli elementi selezionati nella playlist come "Total Time" o "Estimated Time", a seconda che i valori totali siano noti. Questo testo è seguito da "%duration%". |



 

Il valore "Total Time: %duration%" per una playlist che contiene una durata totale di sette minuti visualizza "Total Time: 07:00".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





