---
description: Esporta il punto di riferimento del sistema virtuale.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Metodo ExportReferencePoint della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3273c4781858b02e60b632ae491b1694068a32f5feaddea885576dade6876989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147954"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Metodo ExportReferencePoint della classe Msvm \_ VirtualSystemReferencePointService

Esporta il punto di riferimento del sistema virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ReferencePoint* \[ Pollici\]
</dt> <dd>

Riferimento [**all'istanza di Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento da esportare.

</dd> <dt>

*ExportDirectory* \[ Pollici\]
</dt> <dd>

Percorso completo della directory in cui esportare il punto di riferimento.

</dd> <dt>

*ExportSettingData* \[ Pollici\]
</dt> <dd>

Istanza di [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene usato se non è stato possibile eseguire il metodo in modo sincrono. Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 (completato senza errori) o 4096 (processo avviato); In caso contrario, restituisce un errore.

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

 

 




