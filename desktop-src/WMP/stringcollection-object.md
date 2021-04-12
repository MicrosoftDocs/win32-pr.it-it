---
title: StringCollection (oggetto)
description: L'oggetto StringCollection fornisce un modo per modificare una raccolta di stringhe.
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- Oggetto StringCollection Media Player Windows
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104334959"
---
# <a name="stringcollection-object"></a>StringCollection (oggetto)

L'oggetto **StringCollection** fornisce un modo per modificare una raccolta di stringhe.

L'oggetto **StringCollection** supporta la proprietà seguente.



| Proprietà                            | Descrizione                                             |
|-------------------------------------|---------------------------------------------------------|
| [count](stringcollection-count.md) | Recupera il numero di elementi nell'insieme di stringhe. |



 

L'oggetto **StringCollection** supporta i metodi seguenti.



| Metodo                                                                  | Descrizione                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](stringcollection-getattributecountbytype.md) | Recupera il numero di attributi associati all'indice dell'elemento **StringCollection** , al nome dell'attributo e alla lingua specificati. |
| [getItemInfo](stringcollection-getiteminfo.md)                         | Recupera la stringa corrispondente all'indice e al nome dell'elemento **StringCollection** specificato.                                   |
| [getItemInfoByType](stringcollection-getiteminfobytype.md)             | Recupera la stringa corrispondente all'indice dell'elemento **StringCollection** , al nome, alla lingua e all'indice dell'attributo specificati.       |
| [Identico](stringcollection-isidentical.md)                         | Recupera un valore che indica se l'oggetto fornito è uguale a quello corrente.                                        |
| [item](stringcollection-item.md)                                       | Recupera la stringa in corrispondenza dell'indice specificato.                                                                                    |



 

È possibile accedere all'oggetto **StringCollection** tramite il metodo seguente.



| Oggetto                                        | Metodo                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [Mediacollection](mediacollection-object.md) | [getAttributeStringCollection](mediacollection-getattributestringcollection.md) |



 

Ai fini dell'illustrazione, *Player*. *mediacollection*. **getAttributeStringCollection**(*attribute*, *mediaType*) viene usato nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




