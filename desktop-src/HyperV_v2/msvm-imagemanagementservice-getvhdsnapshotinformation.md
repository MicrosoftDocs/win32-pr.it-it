---
description: Recupera informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Metodo GetVHDSnapshotInformation della Msvm_ImageManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: faac0c7b52d8e066ffa658a539a18d6423b50c861b772e536abca2aca010ea47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046631"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Metodo GetVHDSnapshotInformation della classe Msvm \_ ImageManagementService

Recupera informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VHDSetPath* \[ Pollici\]
</dt> <dd>

Percorso completo che specifica il percorso del file del set di dischi rigidi virtuali.

</dd> <dt>

*SnapshotIds* \[ Pollici\]
</dt> <dd>

Elenco di GUID che rappresentano gli ID snapshot di ogni snapshot per cui vengono richieste informazioni. Se questo parametro è NULL, verranno recuperate le informazioni per tutti gli snapshot.

</dd> <dt>

*Informazioni aggiuntive* \[ Pollici\]
</dt> <dd>

Matrice che specifica le informazioni aggiuntive da raccogliere su ogni snapshot del disco rigido virtuale. Ogni voce nella matrice è un tipo di informazioni aggiuntive. Se questo parametro è NULL, non verranno recuperate informazioni aggiuntive.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

**Percorsi padre** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SnapshotInformation* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, matrice di informazioni su ogni snapshot richiesto. Ogni elemento è un'istanza incorporata [**di Msvm \_ VHDSnapshotInformation.**](msvm-vhdsnapshotinformation.md)

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento al processo (può essere Null se l'attività viene completata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
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

**Il sistema è in uso** (32774)
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

 

 




