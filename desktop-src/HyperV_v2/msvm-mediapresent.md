---
description: Associa un'unità di archiviazione al supporto inserito nell'unità.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Msvm_MediaPresent classe
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
ms.openlocfilehash: 7044cfed5a4affd628ea8008c89b4aabeee3499d65f03abf815e68d73d06a773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521721"
---
# <a name="msvm_mediapresent-class"></a>Classe \_ Msvm MediaPresent

Associa un'unità di archiviazione al supporto inserito nell'unità. Questa associazione viene usata per tutti gli oggetti unità di archiviazione.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe \_ Msvm MediaPresent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ MediaPresent** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al dispositivo di accesso ai supporti. Questa proprietà viene ereditata da [**CIM \_ MediaPresent.**](/windows/desktop/CIMWin32Prov/cim-mediapresent)

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'extent di archiviazione a cui si accede con il dispositivo di accesso ai supporti. Questa proprietà viene ereditata da [**CIM \_ MediaPresent.**](/windows/desktop/CIMWin32Prov/cim-mediapresent)

</dd> <dt>

**Correzione dell'oggettoMedia**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'extent di archiviazione a cui si accede è fisso e non può essere espulso. Il valore è **True per** i dischi rigidi e False in **caso contrario.** Questa proprietà viene ereditata da [**CIM \_ MediaPresent.**](/windows/desktop/CIMWin32Prov/cim-mediapresent)

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ MediaPresent** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dt>

[**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[Archiviazione Classi](storage-classes.md)
</dt> </dl>

 

