---
description: Il metodo CreateObject dell'oggetto Microsoft. Windows. ActCtx crea un oggetto nel contesto del manifesto corrente.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: Metodo ActCtx. CreateObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232049"
---
# <a name="actctxcreateobject-method"></a>Metodo ActCtx. CreateObject

Il metodo **CreateObject** dell'oggetto [**Microsoft. Windows. ACTCTX**](microsoft-windows-actctx-object.md) crea un oggetto nel contesto del manifesto corrente.

## <a name="syntax"></a>Sintassi


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objectId* 
</dt> <dd>

Stringa che specifica il tipo di oggetto da creare. Ad esempio, un ProgID COM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx è definito come 8FA7728F-B69B-4ee5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo GetObject**](getobject.md)
</dt> </dl>

 

 




