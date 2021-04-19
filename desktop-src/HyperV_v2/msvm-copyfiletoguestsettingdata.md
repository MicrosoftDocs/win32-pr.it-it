---
description: Rappresenta i parametri per la copia di un file dall'host nel guest.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Classe Msvm_CopyFileToGuestSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317193"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>\_Classe MSVM CopyFileToGuestSettingData

Rappresenta i parametri per la copia di un file dall'host nel guest. Questa classe deriva da [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a>Members

La **classe \_ CopyFileToGuestSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CopyFileToGuestSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

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

**CreateFullPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è necessario creare directory mancanti nel percorso del file di destinazione prima di copiare il file.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto.

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo del file di destinazione da copiare. Il file di destinazione deve essere accessibile al Guest e può contenere variabili di ambiente, che vengono espanse dal Guest. Se il percorso specificato è una directory esistente nel guest, il file di destinazione viene creato in questa directory. In questo caso, il nome del file da **SourcePath** viene usato come nome del file di destinazione.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per questa istanza di SettingData. Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query. Nota: non è necessario che il nome sia univoco all'interno di uno spazio dei nomi.

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

**OverwriteExisting**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è necessario sovrascrivere un file di destinazione esistente.

</dd> <dt>

**SourcePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo del file di origine da copiare. Questo file di origine deve essere accessibile all'host Hyper-V e può contenere variabili di ambiente, che vengono espanse dall'host Hyper-V.

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

 

