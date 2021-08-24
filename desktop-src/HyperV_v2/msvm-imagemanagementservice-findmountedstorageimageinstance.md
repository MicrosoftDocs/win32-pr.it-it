---
description: Trova un oggetto Msvm \_ MountedStorageImage per un percorso di immagine del disco specificato.
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
ms.openlocfilehash: de205cb729b9ad53674808523cc640b9aaccb2adfaf6fba0b8a06c8a0d8952f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522631"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Metodo FindMountedStorageImageInstance della classe Msvm \_ ImageManagementService

Trova un [**oggetto Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) per un percorso di immagine del disco specificato.

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

*SelectionCriterion* \[ Pollici\]
</dt> <dd>

Percorso completo che specifica il percorso di un file di immagine disco.

</dd> <dt>

*CriterionType* \[ Pollici\]
</dt> <dd>

Tipo di criterio da cercare quando si trova l'immagine del disco.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Percorso** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Immagine* \[ Cambio\]
</dt> <dd>

Riferimento a [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) (può essere Null se l'immagine non è montata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Operazione non** riuscita (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
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
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




