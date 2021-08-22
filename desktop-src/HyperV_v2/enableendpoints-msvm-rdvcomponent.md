---
description: Richiede al Servizi Desktop remoto virtuale di avviare una connessione pipe con la macchina virtuale.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Metodo EnableEndPoints della classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8a23f39ee46cb41c5941be3d9632fbe15901dfffd35078e680ebe61d46fdb131
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532531"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a>Metodo EnableEndPoints della classe Msvm \_ RdvComponent

Richiede al Servizi Desktop remoto virtuale di avviare una connessione pipe con la macchina virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
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

**Memoria insufficiente** (32774)
</dt> <dt>

**File non trovato** (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> <dt>

 (32779)
</dt> <dt>

 (32780)
</dt> <dt>

 (32781)
</dt> <dt>

 (32782)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ RdvComponent**](msvm-rdvcomponent.md)
</dt> </dl>

 

 




