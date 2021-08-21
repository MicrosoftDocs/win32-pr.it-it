---
description: Rappresenta i parametri per la copia di un file dall'host nel guest.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData classe
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
ms.openlocfilehash: 6eb011ec8d03153bd5f1b7d956775327d2582410e9ca12591e19a39ddb4af5fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148840"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>Classe \_ Msvm CopyFileToGuestSettingData

Rappresenta i parametri per la copia di un file dall'host nel guest. Questa classe deriva da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

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

La **classe Msvm \_ CopyFileToGuestSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ CopyFileToGuestSettingData** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** ( 64 )
</dt> </dl>

Breve descrizione testuale dell'oggetto .

</dd> <dt>

**CreateFullPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è necessario creare directory mancanti nel percorso del file di destinazione prima di copiare il file.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto .

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo del file di destinazione da copiare. Questo file di destinazione deve essere accessibile al guest e può contenere variabili di ambiente espanse dal guest. Se il percorso specificato è una directory esistente nel guest, il file di destinazione viene creato in questa directory. In questo caso, il nome file da **SourcePath** viene usato come nome del file di destinazione.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per questa istanza di SettingData. Inoltre, il nome visualizzato può essere usato come proprietà di indice per una ricerca o una query. Nota: il nome non deve essere univoco all'interno di uno spazio dei nomi.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nell'ambito dello spazio dei nomi che crea un'istanza, InstanceID identifica in modo opaco e univoco un'istanza di questa classe. Per garantire l'univocità all'interno di NameSpace, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente: *OrgID:**LocalID* Dove *OrgID* e *LocalID* sono separati da due punti (:) e dove *OrgID* deve includere un nome protetto da copyright, con marchio o altrimenti univoco di proprietà dell'entità aziendale che crea o definisce InstanceID o che è un ID registrato assegnato all'entità aziendale da un'autorità globale riconosciuta. Questo requisito è simile a *SchemaName* \_ *Struttura ClassName* dei nomi delle classi schema. Inoltre, per garantire l'univocità, *OrgID* non deve contenere i due punti (:). Quando si usa questo algoritmo, i primi due punti da visualizzare in InstanceID devono essere compresi tra *OrgID* e *LocalID*. *LocalID* viene scelto dall'entità business e non deve essere riutilizzato per identificare diversi elementi sottostanti (reali). Se l'algoritmo preferito precedente non viene usato, l'entità di definizione deve garantire che l'InstanceID risultante non viene riutilizzato in alcun InstanceID prodotto da questo o da altri provider per NameSpace di questa istanza. Per le istanze definite da DMTF, l'algoritmo "preferito" deve essere usato con *OrgID* impostato su CIM.

</dd> <dt>

**OverwriteExisting**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se un file di destinazione esistente deve essere sovrascritto.

</dd> <dt>

**SourcePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo del file di origine da copiare. Questo file di origine deve essere accessibile all'host Hyper-V e può contenere variabili di ambiente espanse dall'host Hyper-V.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

