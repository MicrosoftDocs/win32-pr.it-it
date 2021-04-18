---
description: Indica un MCA, un controllo del computer corretto (CMC) o una voce di informazioni di errore della piattaforma (CPE) corretta. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Classe MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316591"
---
# <a name="msmcainfo_entry-class"></a>\_Classe entry MSMCAInfo

La classe di **\_ immissione MSMCAInfo** indica un MCA, un controllo del computer corretto (CMC) o una voce di informazioni di errore della piattaforma (CPE) corretta. Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Members

La **classe \_ entry MSMCAInfo** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ entry di MSMCAInfo** dispone di queste proprietà.

<dl> <dt>

**Dati**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di interi che contiene un record di errore MCA completo come riportato da System Abstraction Layer (SAL). SAL è il codice bruciato in ROM che il sistema operativo chiama per eseguire operazioni dipendenti dalla piattaforma. È simile al BIOS su una piattaforma x86.

</dd> <dt>

**Length**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di byte nel record di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ entry MSMCAInfo** deriva da [**MSMCAInfo**](msmcainfo.md).

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

 

 




