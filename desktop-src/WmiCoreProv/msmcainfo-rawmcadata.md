---
description: Specifica i log MCA (RAW Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: Classe MSMCAInfo_RawMCAData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526101"
---
# <a name="msmcainfo_rawmcadata-class"></a>\_Classe MSMCAInfo RawMCAData

Il **\_ RawMCAData MSMCAInfo** specifica i log dell'architettura di controllo del computer (MCA) non elaborati. Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Members

La **classe \_ RawMCAData di MSMCAInfo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ RawMCAData di MSMCAInfo** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

TRUE se questa istanza della classe è attiva; in caso contrario, **false**.

</dd> <dt>

**Count**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di record degli errori.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificatore univoco di questa istanza della classe.

</dd> <dt>

**Record**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSMCAInfo \_ entry** Array
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di record degli errori MCA. Il numero di record di errore MCA nella matrice viene specificato dalla proprietà **count** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **MSMCAInfo \_ RawMCAData** è derivata da [**MSMCAInfo**](msmcainfo.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

