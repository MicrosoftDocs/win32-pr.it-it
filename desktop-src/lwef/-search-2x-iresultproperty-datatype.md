---
title: Proprietà DataType IResultProperty (WdsSharedIDL.h)
description: Tipo di dati properties.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- Proprietà DataType Funzionalità dell'Windows legacy
- Proprietà DataType Legacy Windows Environment Features , interfaccia IResultProperty
- Interfaccia IResultProperty Legacy Windows funzionalità dell'ambiente, proprietà DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f669fdbb01459e99edb0ccc9ba75fed1cbd60ebfe789fdb4393d217239cdc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755260"
---
# <a name="iresultpropertydatatype-property"></a>Proprietà IResultProperty::D ataType

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Tipo di dati properties.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a>Valore proprietà

restituisce un puntatore al tipo di dati properties.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





