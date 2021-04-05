---
title: Proprietà IPropertyFilterCollection RemoveItem (WdsSharedIDL. h)
description: Rimuove un filtro specifico per la raccolta.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà RemoveItem
- Proprietà RemoveItem caratteristiche dell'ambiente Windows legacy, interfaccia IPropertyFilterCollection
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilterCollection, proprietà RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742327"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>Proprietà IPropertyFilterCollection:: RemoveItem

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Rimuove un filtro specifico per la raccolta.

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a>Valore proprietà

Accetta un puntatore all'indice per il filtro da rimuovere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





