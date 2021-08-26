---
title: Proprietà PreceivedType IResultType (WdsSharedIDL.h)
description: Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Proprietà PreceivedType Legacy Windows Environment Features
- Proprietà PreceivedType Legacy Windows Environment Features , interfaccia IResultType
- Interfaccia IResultType Legacy Windows Environment Features , proprietà PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765a770dc07f1fc0287e861ca79fc2aa941ea7cc425fff29e5e4c5772410c06e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014617"
---
# <a name="iresulttypepreceivedtype-property"></a>Proprietà IResultType::P receivedType

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

restituisce l'indirizzo della stringa che identifica il tipo nell'indice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





