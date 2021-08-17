---
title: Metodo WSMan.EnumerationFlagHierarchyDeep (WSManDisp.h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagHierarchyDeep da usare nel parametro flags di Session.Enumerate.
ms.assetid: b84b82fa-0b2e-418e-850f-6d7a4749fdc1
ms.tgt_platform: multiple
keywords:
- Metodo EnumerationFlagHierarchyDeep Windows gestione remota
- Metodo EnumerationFlagHierarchyDeep Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo EnumerationFlagHierarchyDeep
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeep
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ccd7aa4884a916a9b8ae8d364679263fa0b217dccef1065c58c332678b9f07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742594"
---
# <a name="wsmanenumerationflaghierarchydeep-method"></a>Metodo WSMan.EnumerationFlagHierarchyDeep

Il **metodo EnumerationFlagHierarchyDeep** restituisce il valore del flag di enumerazione **EnumerationFlagHierarchyDeep** da usare nel parametro *flags* di [**Session.Enumerate.**](session-enumerate.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione.](session-constants.md)

**EnumerationFlagHierarchyDeep** è una costante **\_ nell'enumerazione WSManEnumFlags** ed è descritta in [**Costanti di enumerazione**](enumeration-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.EnumerationFlagHierarchyDeep( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Cambio\]
</dt> <dd>

Valore della costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 





