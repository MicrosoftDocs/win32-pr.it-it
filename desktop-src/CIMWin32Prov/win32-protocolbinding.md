---
description: La \_ classe WMI Association Protocol associazione di Win32 mette in correlazione un driver a livello di sistema, un protocollo di rete e una scheda di rete.
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Classe Win32_ProtocolBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877337"
---
# <a name="win32_protocolbinding-class"></a>\_Classe di protocollo Win32

La [classe WMI](../wmisdk/retrieving-a-class.md) Association **\_ Protocol** associazione di Win32 mette in correlazione un driver a livello di sistema, un protocollo di rete e una scheda di rete.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a>Members

La classe di **\_ protocollo Win32** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ protocollo Win32** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ NetworkProtocol**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkProtocol")
</dt> </dl>

Riferimento all'istanza di che rappresenta il protocollo utilizzato con il driver di sistema e nella scheda di rete.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ SystemDriver**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

Riferimento all'istanza di che rappresenta il driver di sistema che utilizza la scheda di rete tramite il protocollo di rete di questa classe.

</dd> <dt>

**Dispositivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ NetworkAdapter**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapter")
</dt> </dl>

Proprietà della scheda di rete utilizzata nel computer.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
