---
description: Trova un \_ oggetto MSVM MountedStorageImage per un determinato percorso di immagine disco.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Metodo FindMountedStorageImageInstance della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526833"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Metodo FindMountedStorageImageInstance della classe MSVM \_ servizio

Trova un oggetto [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) per un determinato percorso di immagine disco.

## <a name="syntax"></a>Sintassi


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SelectionCriterion* \[ in\]
</dt> <dd>

Percorso completo che specifica il percorso di un file di immagine disco.

</dd> <dt>

*CriterionType* \[ in\]
</dt> <dd>

Tipo di criterio da cercare quando si trova l'immagine del disco.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Percorso** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Immagine* \[ di out\]
</dt> <dd>

Riferimento a [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) (può essere null se l'immagine non è montata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Completato senza errori** (0)
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
</dt> <dt>

**File non trovato** (32779)
</dt> <dt>

**Oggetto non trovato** (32789)
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

[**\_Servizio MSVM**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




