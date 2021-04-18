---
description: Rappresenta un dispositivo di tastiera sintetico.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306028"
---
# <a name="msvm_synthetickeyboard-class"></a>\_Classe MSVM SyntheticKeyboard

Rappresenta un dispositivo di tastiera sintetico.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a>Members

La **classe \_ SyntheticKeyboard di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ SyntheticKeyboard di MSVM** dispone di questi metodi.



| Metodo                                                                  | Descrizione                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-synthetickeyboard-requeststatechange.md) | Richiede una modifica dello stato.<br/> |
| [**Reset**](msvm-synthetickeyboard-reset.md)                           | Reimposta il dispositivo.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_USERDEVICE CIM**](cim-userdevice.md)
</dt> </dl>

 

 




