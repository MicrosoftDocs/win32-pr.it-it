---
description: Associa un'unità di archiviazione al supporto inserito nell'unità.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Classe Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886024"
---
# <a name="msvm_mediapresent-class"></a>\_Classe MSVM MediaPresent

Associa un'unità di archiviazione al supporto inserito nell'unità. Questa associazione viene utilizzata per tutti gli oggetti unità di archiviazione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a>Members

La **classe \_ MediaPresent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ MediaPresent di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al dispositivo di accesso multimediale. Questa proprietà viene ereditata da [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'extent di archiviazione a cui si accede con il dispositivo di accesso multimediale. Questa proprietà viene ereditata da [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> <dt>

**FixedMedia**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'extent di archiviazione a cui si accede è fisso e non può essere rimosso. Il valore è **true** per i dischi rigidi e **false** in caso contrario. Questa proprietà viene ereditata da [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ MediaPresent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dt>

[**\_MEDIAPRESENT CIM**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[Classi di archiviazione](storage-classes.md)
</dt> </dl>

 

