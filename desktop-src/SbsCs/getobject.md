---
description: Il metodo GetObject recupera un'istanza di un oggetto Microsoft. Windows. ActCtx esistente.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject, metodo
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
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750962"
---
# <a name="actctxgetobject-method"></a>ActCtx. GetObject, metodo

Il metodo **GetObject** recupera un'istanza di un oggetto [**Microsoft. Windows. ACTCTX**](microsoft-windows-actctx-object.md) esistente.

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

Stringa obbligatoria che indica l'oggetto. Il nome deve trovarsi nel registro di sistema in **HKEY \_ \_ computer locale** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.

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

[**Metodo CreateObject**](createobject.md)
</dt> </dl>

 

 




