---
description: 'Metodo RemoveAssociatedData della Msvm_VirtualSystemReferencePointService: rimuove il log dei dati associato al punto di riferimento.'
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Metodo RemoveAssociatedData della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3f8cef79e55379df1f91a0e1291144a7f4fdf92378e44cd9ed3588c83b3a3d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147904"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Metodo RemoveAssociatedData della classe Msvm \_ VirtualSystemReferencePointService

Rimuove il log di dati associato al punto di riferimento.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedReferencePoint* \[ Pollici\]
</dt> <dd>

Riferimento [**all'istanza di Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento da rimuovere.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene utilizzato se non è stato possibile eseguire il metodo in modo sincrono. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 (completo senza errori) o 4096 (processo avviato). In caso contrario, restituisce un errore.

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

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
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

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




