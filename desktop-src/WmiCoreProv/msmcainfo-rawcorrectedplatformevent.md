---
description: Contiene un evento di piattaforma con correzione (CPE). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Classe MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316588"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a>\_Classe MSMCAInfo RawCorrectedPlatformEvent

La **classe \_ RawCorrectedPlatformEvent di MSMCAInfo** contiene un evento di piattaforma corretto (CPE). Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Members

La **classe \_ RawCorrectedPlatformEvent di MSMCAInfo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ RawCorrectedPlatformEvent di MSMCAInfo** dispone di queste proprietà.

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

**Record**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSMCAInfo \_ entry** Array
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di record degli errori MCA. Il numero di record di errore MCA nella matrice viene specificato dalla proprietà **count** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **MSMCAInfo \_ RawCorrectedPlatformEvent** è derivata da [**WmiEvent**](wmievent.md).

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

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




