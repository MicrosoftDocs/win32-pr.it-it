---
description: Rappresenta un dispositivo da tastiera sintetica.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Msvm_SyntheticKeyboard classe
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
ms.openlocfilehash: 86ee3a7835349ab47082627f98020f84084b4b86e9c6b4ce4a37ba2f455497cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582221"
---
# <a name="msvm_synthetickeyboard-class"></a>Classe Msvm \_ SyntheticKeyboard

Rappresenta un dispositivo da tastiera sintetica.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SyntheticKeyboard** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe Msvm \_ SyntheticKeyboard** include questi metodi.



| Metodo                                                                  | Descrizione                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-synthetickeyboard-requeststatechange.md) | Richiede una modifica dello stato.<br/> |
| [**Reset**](msvm-synthetickeyboard-reset.md)                           | reimposta il dispositivo.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> </dl>

 

 




