---
title: Proprietà IPropertyFilterCollection RemoveItem (WdsSharedIDL.h)
description: Rimuove un filtro specifico per la raccolta.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- Proprietà RemoveItem Funzionalità dell'Windows legacy
- Proprietà RemoveItem Legacy Windows Environment Features , interfaccia IPropertyFilterCollection
- Interfaccia IPropertyFilterCollection Legacy Windows Environment Features , proprietà RemoveItem
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
ms.openlocfilehash: 54822e95e2ea7d6e10fdd5bbf833adb63b51cb01e8d860ce77f550432b41e926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755420"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>Proprietà IPropertyFilterCollection::RemoveItem

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

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
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





