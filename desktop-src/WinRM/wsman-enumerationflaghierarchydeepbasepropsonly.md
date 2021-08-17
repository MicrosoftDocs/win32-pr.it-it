---
title: Metodo WSMan.EnumerationFlagHierarchyDeepBasePropsOnly (WSManDisp.h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagHierarchyDeepBasePropsOnly da usare nel parametro flags di Session.Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- Metodo EnumerationFlagHierarchyDeepBasePropsOnly Windows Remote Management
- Metodo EnumerationFlagHierarchyDeepBasePropsOnly Windows gestione remota , oggetto WSMan
- Metodo WSMan Windows gestione remota , EnumerationFlagHierarchyDeepBasePropsOnly
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeepBasePropsOnly
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197c615b8d805fc142fa8afb2cf4fbb56ef22eec76caf63f03c27f3d9f131b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742459"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a>Metodo WSMan.EnumerationFlagHierarchyDeepBasePropsOnly

Il metodo **WSMan.EnumerationFlagHierarchyDeepBasePropsOnly** restituisce il valore del flag di enumerazione **EnumerationFlagHierarchyDeepBasePropsOnly** da usare nel parametro *flags* di [**Session.Enumerate.**](session-enumerate.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione](session-constants.md).

**EnumerationFlagHierarchyDeepBasePropsOnly** è una costante nell'enumerazione **\_ WSManEnumFlags** ed è descritta in [**Costanti di enumerazione**](enumeration-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
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

 

 





