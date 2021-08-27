---
title: Proprietà UID IResultProperty (WdsSharedIDL.h)
description: Identificatore univoco della proprietà.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- Proprietà UID Funzionalità dell'ambiente Windows legacy
- Proprietà UID Legacy Windows Environment Features , interfaccia IResultProperty
- Interfaccia IResultProperty Legacy Windows Environment Features , proprietà UID
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d413a81d6b18091d2e21b4572f5f8e01693829c17942d3e395e2c03a71d467d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754720"
---
# <a name="iresultpropertyuid-property"></a>Proprietà IResultProperty::UID

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Identificatore univoco della proprietà.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Valore proprietà

restituisce un puntatore all'identificatore univoco della proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





