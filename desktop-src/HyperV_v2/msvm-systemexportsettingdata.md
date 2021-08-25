---
description: Associa una macchina virtuale e i relativi dati delle impostazioni di esportazione.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData classe
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
ms.openlocfilehash: 39e096c466dd4accc1a2c87ececd6ce23ba27cb173e6b5fa0d6728852ad59cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811871"
---
# <a name="msvm_systemexportsettingdata-class"></a>Classe \_ Msvm SystemExportSettingData

Associa una macchina virtuale e i relativi dati delle impostazioni di esportazione. Prima di chiamare [**il metodo ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService,**](msvm-virtualsystemmanagementservice.md) è possibile recuperare un'istanza di [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) usando questa associazione.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe \_ Msvm SystemExportSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SystemExportSettingData** dispone di queste proprietà.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'impostazione a cui si fa riferimento è attualmente in uso nell'operazione dell'elemento o se queste informazioni sono sconosciute. Questa proprietà viene ereditata da [**\_ ElementSettingData CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Valore                                                                        | Significato                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Sconosciuto<br/>     |
| <dl> <dt>1</dt> </dl> | Corrente<br/>     |
| <dl> <dt>2</dt> </dl> | Non corrente<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'impostazione a cui si fa riferimento è un'impostazione predefinita per l'elemento o se queste informazioni sono sconosciute. Questa proprietà viene ereditata da [**\_ ElementSettingData CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Valore                                                                        | Significato                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Sconosciuto<br/>     |
| <dl> <dt>1</dt> </dl> | Predefinito<br/>     |
| <dl> <dt>2</dt> </dl> | Non predefinito<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'impostazione a cui si fa riferimento è l'impostazione successiva da applicare. Ad esempio, l'applicazione potrebbe avere luogo in una richiesta di reiniezione, reimpostazione e riconfigurazione. Può trattarsi di un'impostazione permanente o di un'impostazione usata una sola volta, come indicato dal flag . Se si tratta di un'impostazione permanente, l'impostazione viene applicata ogni volta che l'elemento gestito viene reinizializzato, fino a quando questo flag non viene reimpostato manualmente. Tuttavia, se si tratta di un singolo utilizzo, il flag viene cancellato automaticamente dopo l'applicazione delle impostazioni. Inoltre, se questo flag viene specificato (ad esempio, impostato su un valore diverso da 0 (sconosciuto),ha la precedenza su tutti i dati di impostazione che potrebbero essere stati specificati come predefiniti. Ad esempio: se l'elemento gestito è un computer e il valore di questo flag è 1 (è successivo), l'impostazione sarà effettiva al successivo ripristino del sistema. E, a meno che questo flag non venga modificato, verrà mantenuto per le successive reimpostazioni del sistema. Tuttavia, se questo flag è impostato su 3 (è successivo per uso singolo), questa impostazione verrà usata una sola volta e il flag verrà reimpostato dopo su 2 (Non successivo). Pertanto, nell'esempio precedente, se il sistema viene riavviato in rapida successione, l'impostazione non verrà usata al secondo riavvio.

Questa proprietà viene ereditata da [**\_ ElementSettingData CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)



| Valore                                                                        | Significato                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Sconosciuto<br/>                |
| <dl> <dt>1</dt> </dl> | Is Next<br/>                |
| <dl> <dt>2</dt> </dl> | Non è successivo<br/>            |
| <dl> <dt>3</dt> </dl> | Is Next For Single Use<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData.ManagedElement")
</dt> </dl>

Riferimento alla macchina virtuale. Questa proprietà viene ereditata da [**\_ ElementSettingData CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)

</dd> <dt>

**Impostazione dei dati**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData.SettingData")
</dt> </dl>

Riferimento ai dati delle impostazioni di esportazione per la macchina virtuale. Questa proprietà viene ereditata da [**\_ ElementSettingData CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ SystemExportSettingData** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

