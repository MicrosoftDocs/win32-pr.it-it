---
description: Esecuzione di query sulle informazioni del cluster dall'host Hyper-V al Guest.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Metodo QueryGuestClusterInformation della classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525177"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a>Metodo QueryGuestClusterInformation della classe MSVM \_ VssService

Esecuzione di query sulle informazioni del cluster dall'host Hyper-V al Guest.

## <a name="syntax"></a>Sintassi


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*GuestClusterInformation* \[ out\]
</dt> <dd>

Se l'operazione ha esito positivo, contiene un [**\_ GuestClusterInformation MSVM**](msvm-guestclusterinformation.md) che descrive il cluster guest.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 (completa senza errori) o 4096 (processo avviato); in caso contrario, viene restituito un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VssService MSVM**](msvm-vssservice.md)
</dt> </dl>

 

 




