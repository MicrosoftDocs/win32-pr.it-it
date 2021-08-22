---
description: Metodo CreateObject di Microsoft. Windows. L'oggetto ActCtx crea un oggetto nel contesto del manifesto corrente.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: Metodo ActCtx.CreateObject
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
ms.openlocfilehash: 4161ccdcc2562405123d8cb5276aa1f849121c0271b6c6e3f23a32551f6f3dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142394"
---
# <a name="actctxcreateobject-method"></a>Metodo ActCtx.CreateObject

Metodo **CreateObject** dell'oggetto [**Microsoft.Windows. L'oggetto ActCtx**](microsoft-windows-actctx-object.md) crea un oggetto nel contesto del manifesto corrente.

## <a name="syntax"></a>Sintassi


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Objectid* 
</dt> <dd>

Stringa che specifica il tipo di oggetto da creare. Ad esempio, un ProgID COM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx è definito come 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo GetObject**](getobject.md)
</dt> </dl>

 

 




