---
title: Metodo WSMan.EnumerationFlagHierarchyShallow (WSManDisp.h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagHierarchyShallow da usare nel parametro flags di Session.Enumerate.
ms.assetid: 18b564e6-dda1-44b9-b445-26c6183b6af9
ms.tgt_platform: multiple
keywords:
- Metodo EnumerationFlagHierarchyShallow Windows gestione remota
- Metodo EnumerationFlagHierarchyShallow Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo EnumerationFlagHierarchyShallow
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyShallow
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f894c252de856a6845b1d98b475a51e92dc1d95b054eb77449617f6fc36bf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742300"
---
# <a name="wsmanenumerationflaghierarchyshallow-method"></a>Metodo WSMan.EnumerationFlagHierarchyShallow

Il **metodo EnumerationFlagHierarchyShallow** restituisce il valore del flag di enumerazione **EnumerationFlagHierarchyShallow** da usare nel parametro *flags* di [**Session.Enumerate.**](session-enumerate.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione.](session-constants.md)

**EnumerationFlagHierarchyShallow** è una costante **\_ nell'enumerazione WSManEnumFlags** ed è descritta in [**Costanti di enumerazione.**](enumeration-constants.md)

## <a name="syntax"></a>Sintassi


```VB
WSMan.EnumerationFlagHierarchyShallow( _
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

 

 





