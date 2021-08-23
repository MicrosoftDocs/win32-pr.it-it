---
description: Usato nel metodo QueryGuestClusterInformation nella classe Msvm VssService per recuperare informazioni sul cluster guest di cui \_ fa parte la macchina virtuale.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed353e0d9c4d3049e120b00a11bc3d1bf85e3a0b42e52deb4ed277b9bde9b96b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523296"
---
# <a name="msvm_guestclusterinformation-class"></a>Classe Msvm \_ GuestClusterInformation

Usato nel [**metodo QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) nella [**classe Msvm \_ VssService**](msvm-vssservice.md) per recuperare informazioni sul cluster guest di cui fa parte la macchina virtuale.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ GuestClusterInformation** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ GuestClusterInformation** ha queste proprietà.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

L'identificatore del cluster di failover di cui fa parte il sistema operativo guest della macchina virtuale.

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di nodi nel cluster di cui fa parte il sistema operativo guest della macchina virtuale.

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è condivisa tra macchine virtuali in modalità attiva/attiva.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se il disco corrispondente è una risorsa cluster nel cluster guest.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è online.

</dd> <dt>

**IsOwned**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è di proprietà di questa macchina virtuale.

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Conteggio dei tick dell'orologio quando una delle risorse disco condiviso è stata spostata per l'ultima volta.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato")
</dt> </dl>

Matrice di percorsi di dischi rigidi virtuali condivisi connessi alla macchina virtuale.

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato")
</dt> </dl>

Matrice di dati di impostazione di allocazione risorse (RASD, Resource Allocation Setting Data) che rappresentano i dischi rigidi virtuali condivisi connessi alla macchina virtuale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

