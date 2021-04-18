---
description: Rappresenta un'associazione tra un elemento gestito e i dati di impostazione associati. Questa associazione descrive anche se si tratta di un'impostazione predefinita o corrente.
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: Classe CIM_ElementSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312932"
---
# <a name="cim_elementsettingdata-class"></a>CIM \_ ElementSettingData (classe)

Rappresenta un'associazione tra un elemento gestito e i dati di impostazione associati. Questa associazione descrive anche se si tratta di un'impostazione predefinita o corrente.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ElementSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ElementSettingData** dispone di queste proprietà.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'impostazione a cui si fa riferimento è attualmente utilizzata dall'elemento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

**È corrente** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

**Non è corrente** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Che indica se l'impostazione è un'impostazione predefinita per l'elemento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

**È il valore predefinito** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

**Non è predefinito** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Flag che indica quando e con quale frequenza applicare l'impostazione.

Ad esempio, l'impostazione può essere applicata a una richiesta di reinizializzazione, reimpostazione o riconfigurazione. Potrebbe trattarsi di un'impostazione permanente o di un'impostazione utilizzata solo una volta, come indicato dal flag. Se si tratta di un'impostazione permanente, l'impostazione viene applicata ogni volta che l'elemento gestito viene reinizializzato, finché questo flag non viene reimpostato manualmente. Tuttavia, se è monouso, il flag viene cancellato automaticamente dopo l'applicazione delle impostazioni. Inoltre, se questo flag è impostato su un valore diverso da 0 (sconosciuto), ha la precedenza su una proprietà **SettingData** impostata su "default".

Se l'elemento gestito è un computer e il valore di questo flag è "Next", l'impostazione sarà valida al successivo ripristino del sistema. A meno che il flag non venga modificato, verrà mantenuto per le successive reimpostazioni di sistema. Tuttavia, se questo flag è impostato su "è successivo per l'uso singolo", questa impostazione verrà usata una sola volta e il flag verrà reimpostato dopo tale operazione su 2 (non è successivo). Nell'esempio precedente, se il sistema viene riavviato in una rapida successione, l'impostazione non verrà usata al secondo riavvio.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

**Successivo** (1)


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

**Non è Next** (2)


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

**È successivo per uso singolo** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento gestito.

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Dati dell'impostazione associati all'elemento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

