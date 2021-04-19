---
title: PLAYLIST. rightStatus
description: L'attributo rightStatus specifica o Recupera il testo di stato visualizzato sul lato destro e sulla parte inferiore dell'elemento PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- PLAYLIST. rightStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326717"
---
# <a name="playlistrightstatus"></a>PLAYLIST. rightStatus

L'attributo **rightStatus** specifica o Recupera il testo di stato visualizzato sul lato destro e sulla parte inferiore dell'elemento **playlist** .

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Questo attributo può combinare qualsiasi testo con parole chiave specifiche che visualizzeranno le informazioni desiderate, ad esempio la durata totale della playlist. Le parole chiave sono racchiuse tra simboli di percentuale (%) per mantenerli distinti dal testo normale.

È possibile utilizzare le parole chiave seguenti.



| Parola chiave               | Descrizione                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Numero di elementi nella playlist.                                                                                                                                                                             |
| size                  | Dimensioni totali della playlist.                                                                                                                                                                                  |
| duration              | Durata totale della playlist.                                                                                                                                                                              |
| *XXX*                 | Esegue un **GetItemInfo** nella playlist con *xxx* che è l'elemento da ricevere.                                                                                                                                 |
| SelectedSize          | Dimensioni totali delle voci selezionate nella playlist.                                                                                                                                                          |
| SelectedCount         | Numero totale di voci selezionate nella playlist.                                                                                                                                                            |
| SelectedDuration      | Durata totale delle voci selezionate nella playlist.                                                                                                                                                      |
| CheckedCount          | Numero totale di tracce selezionate nella playlist.                                                                                                                                                              |
| CheckedDuration       | Durata totale delle tracce selezionate nella playlist.                                                                                                                                                        |
| CheckedSize           | Dimensioni totali delle tracce selezionate nella playlist.                                                                                                                                                            |
| DurationString        | Visualizza il testo che descrive la durata "tempo totale" o "tempo stimato", a seconda che i valori totali siano noti. Il testo è seguito da "% Duration%".                                       |
| CheckedDurationString | Visualizza il testo che descrive la durata di tutti gli elementi selezionati nella playlist come "tempo totale" o "tempo stimato", a seconda che i valori totali siano noti o meno. Il testo è seguito da "% Duration%". |



 

Il valore "tempo totale:% Duration%" per una playlist che contiene una durata totale di sette minuti visualizzerà "tempo totale: 07:00".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> </dl>

 

 





