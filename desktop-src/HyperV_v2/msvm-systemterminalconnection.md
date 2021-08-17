---
description: Associa una macchina virtuale a una connessione terminale.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Msvm_SystemTerminalConnection classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 280c8c6489e831bf9342e8e19699fb56fcdc6b15d1088a53796af28e45651d8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810596"
---
# <a name="msvm_systemterminalconnection-class"></a>Classe \_ Msvm SystemTerminalConnection

Associa una macchina virtuale a una connessione terminale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SystemTerminalConnection** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SystemTerminalConnection** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Macchina virtuale a cui è collegata la connessione.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ TerminalConnection**](msvm-terminalconnection.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Connessione alla macchina virtuale.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ SystemTerminalConnection** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> <dt>

[**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))
</dt> <dt>

[Classi video](video-classes.md)
</dt> </dl>

 

