---
description: La classe CIM \_ MemoryWithMedia associa la memoria fisica a un supporto fisico e alla relativa cartuccia. La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: CIM_MemoryWithMedia classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eff54c8ac48c9e6e998e720815a9a3529f5484f8a089e8ea510559d2e7cfa488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921411"
---
# <a name="cim_memorywithmedia-class"></a>Classe CIM \_ MemoryWithMedia

La **classe CIM \_ MemoryWithMedia** associa la memoria fisica a un supporto fisico e alla relativa cartuccia. La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ MemoryWithMedia** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ MemoryWithMedia** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalMemory**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Oggetto [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) che descrive la memoria associata ai supporti fisici.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalMedia**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

[**CiM \_ PhysicalMedia che**](cim-physicalmedia.md) descrive i supporti fisici.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ MemoryWithMedia** viene ereditato dalla [**dipendenza CIM. \_**](cim-dependency.md)

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

 

