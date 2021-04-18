---
description: Usato nel metodo QueryGuestClusterInformation nella \_ classe MSVM VssService per recuperare informazioni sul cluster guest di cui fa parte la macchina virtuale.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Classe Msvm_GuestClusterInformation
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
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307910"
---
# <a name="msvm_guestclusterinformation-class"></a>\_Classe MSVM GuestClusterInformation

Usato nel metodo [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) nella classe [**MSVM \_ VssService**](msvm-vssservice.md) per recuperare informazioni sul cluster guest di cui fa parte la macchina virtuale.

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

La **classe \_ GuestClusterInformation di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ GuestClusterInformation di MSVM** dispone di queste proprietà.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del cluster di failover di cui fa parte il sistema operativo guest della macchina virtuale.

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di nodi del cluster di cui fa parte il sistema operativo guest della macchina virtuale.

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è condivisa tra le macchine virtuali in modalità attiva/attiva.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se il disco corrispondente è una risorsa cluster nel cluster guest.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è online.

</dd> <dt>

**Proprietario**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **booleana**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Matrice di valori booleani corrispondenti a ogni disco rigido virtuale condiviso che indica se la risorsa disco corrispondente nel cluster guest è attualmente di proprietà di questa macchina virtuale.

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di tick dell'orologio quando una delle risorse disco condivise è stata spostata più di recente.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Una matrice di percorsi di dischi rigidi virtuali condivisi connessi alla macchina virtuale.

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Una matrice di dati di impostazione di allocazione risorse (RASD) che rappresentano i dischi rigidi virtuali condivisi connessi alla macchina virtuale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

