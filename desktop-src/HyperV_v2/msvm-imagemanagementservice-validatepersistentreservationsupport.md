---
description: Convalida se un file system può supportare un disco rigido virtuale con prenotazioni persistenti abilitate.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Metodo ValidatePersistentReservationSupport della Msvm_ImageManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f1384ca9b56c24a40925a08fb87595fd57acef3e50c1d5d09593d9cfd7f545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147723"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a>Metodo ValidatePersistentReservationSupport della classe Msvm \_ ImageManagementService

Convalida se un file system può supportare un disco rigido virtuale con prenotazioni persistenti abilitate.

## <a name="syntax"></a>Sintassi


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* \[ Pollici\]
</dt> <dd>

Percorso completo che specifica il percorso di un file di immagine disco o di una directory in cui potrebbe essere inserito un file di immagine del disco.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento al processo (può essere Null se l'attività viene completata correttamente).

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
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




