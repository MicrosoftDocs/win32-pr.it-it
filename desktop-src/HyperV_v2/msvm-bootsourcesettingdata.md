---
description: Rappresenta i parametri per impostare l'origine di avvio di una macchina virtuale.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Classe Msvm_BootSourceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308340"
---
# <a name="msvm_bootsourcesettingdata-class"></a>\_Classe MSVM BootSourceSettingData

Rappresenta i parametri per impostare l'origine di avvio di una macchina virtuale. Questa classe deriva da [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a>Members

La **classe \_ BootSourceSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ BootSourceSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**BootSourceDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'origine di avvio fornita dal firmware.

</dd> <dt>

**BootSourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di enumerazione che specifica il tipo di origine di avvio.

Valori validi:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

**Unità** (1)


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

**Rete** (2)


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

**File** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **maxlen** (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per questa istanza di SettingData. Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query. Nota: non è necessario che il nome sia univoco all'interno di uno spazio dei nomi.

</dd> <dt>

**FirmwareDevicePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso nativo usato dal firmware per descrivere il dispositivo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

All'interno dell'ambito dello spazio dei nomi di creazione di istanze, InstanceID indica in modo opaco e univoco un'istanza di questa classe. Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente: *OrgID*:*localizzato* in cui *OrgID* e *LocalId* sono separati da due punti (:) e dove *OrgID* deve includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità di business da un'autorità globale riconosciuta. (Questo requisito è simile a *SchemaName* \_ Struttura *ClassName* dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, *OrgID* non deve contenere i due punti (:). Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono comparire tra *OrgID* e *localizzato*. *Localizzato* viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti. Se non viene utilizzato l'algoritmo preferenziale precedente, l'entità di definizione deve garantire che il InstanceID risultante non venga riutilizzato in alcun InstanceID prodotto da questo o da altri provider per lo spazio dei nomi di questa istanza. Per le istanze definite da DMTF, è necessario usare l'algoritmo "preferenziale" con *OrgID* impostato su CIM.

</dd> <dt>

**OptionalData**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Dati facoltativi forniti dal firmware.

> [!Note]  
> Proprietà aggiunta in Windows 10.

 

</dd> <dt>

**OtherLocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altre informazioni sulla posizione, se presenti, utilizzate dal firmware per identificare in modo univoco l'origine di avvio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

