---
description: La \_ classe WMI dell'associazione SessionProcess Win32 rappresenta un'associazione tra una sessione di accesso e i processi associati a tale sessione.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Classe Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304470"
---
# <a name="win32_sessionprocess-class"></a>Win32 \_ SessionProcess (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SessionProcess Win32** rappresenta un'associazione tra una sessione di accesso e i processi associati a tale sessione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SessionProcess** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SessionProcess** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ LogonSession**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**chiave**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) che rappresenta la sessione correlata al processo.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ processo Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**chiave**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ Processo Win32**](win32-processor.md) che rappresenta il processo associato alla sessione.

</dd> </dl>

## <a name="remarks"></a>Commenti

**Win32 \_ SessionProcess** restituisce tutte le sessioni per l'amministratore in caso di accesso con privilegi elevati o quando viene eseguito in modalità remota. Si tratta di un'estensione del comportamento della classe.

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

[**\_SessionResource Win32**](win32-sessionresource.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
