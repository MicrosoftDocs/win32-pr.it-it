---
description: La classe Mount CIM \_ rappresenta un'associazione tra un file system e una directory a cui è collegato.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: CIM_Mount classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1298c695237ac40097b0c081d313769ee4e4e1190571b1bdd58137e25d53c10a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821021"
---
# <a name="cim_mount-class"></a>Classe Mount CIM \_

La **classe \_ Mount CIM** rappresenta un'associazione tra un file system e una directory a cui è collegato.

La semantica di questa relazione richiede che la directory montata sia contenuta in un file system (tramite l'associazione di archiviazione file) diverso dal file system a cui si fa riferimento come dipendente. La directory che contiene file system può essere locale o remota. Ad esempio, un file system locale in un computer Solaris può montare una directory dal file system a cui si accede tramite l'unità CDROM del computer,ovvero un'altra file system. D'altra parte, in un caso "remoto", la directory viene prima esportata dal relativo file system, che è ospitato in un altro computer che agisce, ad esempio, come file server. Per distinguere i due montamenti, è necessario definire sempre un'associazione [**cim \_ export**](cim-export.md) per le directory a cui si accede in remoto o montate.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe \_ Mount CIM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM Mount** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ directory CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Directory [**CIM \_ che**](cim-directory.md) descrive la directory montata.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ NFS**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

[**NFS \_ CIM**](cim-nfs.md) che descrive il file system in cui è montata la directory.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ Il** montaggio deriva dalla [**dipendenza CIM \_**](cim-dependency.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

