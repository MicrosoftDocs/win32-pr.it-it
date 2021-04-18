---
description: Recupera le informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set VHD.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Metodo GetVHDSnapshotInformation della classe Msvm_ImageManagementService
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
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307895"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Metodo GetVHDSnapshotInformation della classe MSVM \_ servizio

Recupera le informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set VHD.

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

*VHDSetPath* \[ in\]
</dt> <dd>

Percorso completo che specifica il percorso del file di set VHD.

</dd> <dt>

*SnapshotIds* \[ in\]
</dt> <dd>

Elenco di GUID che rappresentano gli ID snapshot di ogni snapshot per cui vengono richieste informazioni. Se questo parametro è NULL, verranno recuperate le informazioni per tutti gli snapshot.

</dd> <dt>

*AdditionalInformation* \[ in\]
</dt> <dd>

Matrice che specifica le informazioni aggiuntive da raccogliere per ogni snapshot del disco rigido virtuale. Ogni voce nella matrice è un tipo di informazioni aggiuntive. Se questo parametro è NULL, non verranno recuperate informazioni aggiuntive.

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

*SnapshotInformation* \[ out\]
</dt> <dd>

In caso di esito positivo, una matrice di informazioni su ogni snapshot richiesto. Ogni elemento è un'istanza incorporata di [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento al processo (può essere null se l'attività è stata completata).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

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
</dt> <dt>

**File non trovato** (32779)
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

 

 




