---
description: Associa una macchina virtuale e i dati delle impostazioni di esportazione.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Classe Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306024"
---
# <a name="msvm_systemexportsettingdata-class"></a>\_Classe MSVM SystemExportSettingData

Associa una macchina virtuale e i dati delle impostazioni di esportazione. Prima di chiamare il metodo [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) , è possibile recuperare un'istanza di [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) utilizzando questa associazione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a>Members

La **classe \_ SystemExportSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SystemExportSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'impostazione a cui si fa riferimento è attualmente utilizzata nell'operazione dell'elemento o se queste informazioni sono sconosciute. Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valore                                                                        | Significato                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Sconosciuto<br/>     |
| <dl> <dt>1</dt> </dl> | Corrente<br/>     |
| <dl> <dt>2</dt> </dl> | Non corrente<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'impostazione a cui si fa riferimento è un'impostazione predefinita per l'elemento o che queste informazioni sono sconosciute. Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valore                                                                        | Significato                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Sconosciuto<br/>     |
| <dl> <dt>1</dt> </dl> | Predefinito<br/>     |
| <dl> <dt>2</dt> </dl> | Non predefinito<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'impostazione a cui si fa riferimento è l'impostazione successiva da applicare. È ad esempio possibile che l'applicazione venga eseguita in una richiesta di reinizializzazione, reimpostazione o riconfigurazione. Potrebbe trattarsi di un'impostazione permanente o di un'impostazione utilizzata solo una volta, come indicato dal flag. Se si tratta di un'impostazione permanente, l'impostazione viene applicata ogni volta che l'elemento gestito viene reinizializzato, finché questo flag non viene reimpostato manualmente. Tuttavia, se è monouso, il flag viene cancellato automaticamente dopo l'applicazione delle impostazioni. Inoltre, se questo flag è specificato (ad esempio, impostato su un valore diverso da 0 (sconosciuto)), questo ha la precedenza su tutti i dati di impostazione che potrebbero essere stati specificati come predefiniti. Ad esempio, se l'elemento gestito è un computer e il valore di questo flag è 1 (è successivo), l'impostazione sarà effettiva al successivo ripristino del sistema. A meno che il flag non venga modificato, verrà mantenuto per le successive reimpostazioni di sistema. Tuttavia, se questo flag è impostato su 3 (è Next per l'uso singolo), questa impostazione verrà usata una sola volta e il flag verrebbe reimpostato dopo tale operazione su 2 (non è successivo). Nell'esempio precedente, se il sistema viene riavviato in una rapida successione, l'impostazione non verrà usata al secondo riavvio.

Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valore                                                                        | Significato                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Sconosciuto<br/>                |
| <dl> <dt>1</dt> </dl> | Successivo<br/>                |
| <dl> <dt>2</dt> </dl> | Non è successivo<br/>            |
| <dl> <dt>3</dt> </dl> | È Next per uso singolo<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. Managed")
</dt> </dl>

Riferimento alla macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")
</dt> </dl>

Riferimento ai dati delle impostazioni di esportazione per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ SystemExportSettingData di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

