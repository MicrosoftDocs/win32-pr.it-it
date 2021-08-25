---
description: Il metodo GetObject ottiene un'istanza di microsoft esistente. Windows. Oggetto ActCtx.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: Metodo ActCtx.GetObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: a102fdae74232fa9a67c4b9455050bcdba32a219d8a66180ae8bc6ce6cb96c8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885281"
---
# <a name="actctxgetobject-method"></a>Metodo ActCtx.GetObject

Il **metodo GetObject** ottiene un'istanza di un [**oggetto Microsoft.Windows. Oggetto ActCtx.**](microsoft-windows-actctx-object.md)

## <a name="syntax"></a>Sintassi


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* 
</dt> <dd>

Stringa obbligatoria che indica l'oggetto. Il nome deve essere nel Registro di sistema in **HKEY \_ LOCAL \_ MACHINE** \\ **Microsoft** \\ **Visual Studio** \\ **6.0** \\ **<package>** \\ **Automation.**

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

[**Metodo CreateObject**](createobject.md)
</dt> </dl>

 

 




