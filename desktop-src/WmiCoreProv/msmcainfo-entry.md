---
description: Indica una voce di informazioni relativa a mca, controllo del computer corretto o errore di piattaforma (CPE). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: MSMCAInfo_Entry classe
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
ms.openlocfilehash: 8f6146d629678c1ee209738095fea901f0edb865bccb9aff2d4eeab02d18e773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640903"
---
# <a name="msmcainfo_entry-class"></a>Classe MSMCAInfo \_ Entry

La **classe MSMCAInfo \_ Entry** indica una voce di informazioni MCA, CMC (Corrected Machine Check) o CPE (Platform Error). Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Members

La **classe MSMCAInfo \_ Entry** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSMCAInfo \_ Entry** ha queste proprietà.

<dl> <dt>

**Dati**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di interi che contiene un record di errore MCA completo, come segnalato dal livello di astrazione di sistema (SAL). SAL è un codice inserito nella ROM che il sistema operativo chiama per eseguire operazioni dipendenti dalla piattaforma. È simile al BIOS in una piattaforma x86.

</dd> <dt>

**Length**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di byte nel record di errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MSMCAInfo \_ Entry** è derivata da [**MSMCAInfo**](msmcainfo.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[**MSMCAInfo**](msmcainfo.md)
</dt> </dl>

 

 




