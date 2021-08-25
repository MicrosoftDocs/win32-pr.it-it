---
description: Rappresenta i parametri per impostare l'origine di avvio di una macchina virtuale.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Msvm_BootSourceSettingData classe
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
ms.openlocfilehash: d7319c8df8c8f9b98ae39ed94f620445d4cc80b32f2c7b45189ce636c1c020dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995038"
---
# <a name="msvm_bootsourcesettingdata-class"></a>Classe Msvm \_ BootSourceSettingData

Rappresenta i parametri per impostare l'origine di avvio di una macchina virtuale. Questa classe deriva da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

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

La **classe Msvm \_ BootSourceSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ BootSourceSettingData** ha queste proprietà.

<dl> <dt>

**BootSourceDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'origine di avvio fornita dal firmware.

</dd> <dt>

**BootSourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore di enumerazione che specifica il tipo dell'origine di avvio.

Questi sono valori validi:

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

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** ( 64 )
</dt> </dl>

Breve descrizione testuale dell'oggetto.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto .

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per questa istanza di SettingData. Inoltre, il nome visualizzato può essere usato come proprietà di indice per una ricerca o una query. Nota: il nome non deve essere univoco all'interno di uno spazio dei nomi.

</dd> <dt>

**FirmwareDevicePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso nativo utilizzato dal firmware per descrivere il dispositivo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Nell'ambito dello spazio dei nomi di creazione dell'istanza, InstanceID identifica in modo opaco e univoco un'istanza di questa classe. Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente: *OrgID:**LocalID* Dove *OrgID* e *LocalID* sono separati da due punti (:) e dove *OrgID* deve includere un nome protetto da copyright, marchio o altrimenti univoco di proprietà dell'entità aziendale che crea o definisce InstanceID o che è un ID registrato assegnato all'entità aziendale da un'autorità globale riconosciuta. Questo requisito è simile a *SchemaName* \_ *Struttura ClassName* dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, *OrgID* non deve contenere i due punti (:). Quando si usa questo algoritmo, i primi due punti da visualizzare in InstanceID devono essere compresi tra *OrgID* e *LocalID*. *LocalID* viene scelto dall'entità business e non deve essere riutilizzato per identificare diversi elementi sottostanti (reali). Se l'algoritmo preferito precedente non viene usato, l'entità di definizione deve garantire che l'InstanceID risultante non viene riutilizzato in alcun InstanceID prodotto da questo o da altri provider per lo spazio dei nomi di questa istanza. Per le istanze definite da DMTF, l'algoritmo "preferito" deve essere usato con *OrgID* impostato su CIM.

</dd> <dt>

**Dati facoltativi**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Dati facoltativi forniti dal firmware.

> [!Note]  
> Proprietà aggiunta in Windows 10.

 

</dd> <dt>

**OtherLocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Le altre informazioni sulla posizione, se presenti, che il firmware usa per identificare ulteriormente in modo univoco l'origine di avvio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

