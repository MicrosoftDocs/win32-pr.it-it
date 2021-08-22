---
description: Calcola la quantità di memoria video necessaria per una RemoteFX virtuale.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Metodo CalculateVideoMemoryRequirements della Msvm_Synth3dVideoPool classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2fd1485cdd4e96155db6540a5f07344add5f413514a92c420fcac78a008e7aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950080"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Metodo CalculateVideoMemoryRequirements della classe \_ Msvm Synth3dVideoPool

Calcola la quantità di memoria video necessaria per una RemoteFX virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*monitorResolution* \[ Pollici\]
</dt> <dd>

Risoluzione massima del monitoraggio per la macchina virtuale. Deve essere uno dei valori seguenti.



| Valore                                                                        | Significato                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La risoluzione massima è 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | La risoluzione massima è 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | La risoluzione massima è 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | La risoluzione massima è 1920 1200.<br/> |



 

</dd> <dt>

*numberOfMonitors* \[ Pollici\]
</dt> <dd>

Numero massimo di monitoraggi per la macchina virtuale. Il numero minimo di monitor è uno e il massimo dipende dalla risoluzione massima dello schermo. Nella tabella seguente viene definito il numero massimo di monitoraggi consentiti per risoluzioni diverse.



| Risoluzione             | Numero massimo di monitoraggi |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[ Cambio\]
</dt> <dd>

Riceve la quantità di memoria video richiesta, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice di stato, che può essere uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Completata senza errori**</dt> <dt>0</dt> </dl>                    | Successo.<br/>                                |
| <dl> <dt>**Parametri del metodo verificati - Processo avviato**</dt> <dt>4096</dt> </dl> | Processo avviato.<br/>                               |
| <dl> <dt>**Errore**</dt> <dt>32768</dt> </dl>                                 | non riuscito.<br/>                                    |
| <dl> <dt>**Accesso negato**</dt> <dt>32769</dt> </dl>                          | Accesso negato.<br/>                             |
| <dl> <dt>**Non supportato**</dt> <dt>32770</dt> </dl>                          | Non supportata.<br/>                             |
| <dl> <dt>**Lo stato è sconosciuto**</dt> <dt>32771</dt> </dl>                      | Lo stato è sconosciuto.<br/>                         |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Timeout.<br/>                                   |
| <dl> <dt>**Parametro**</dt> <dt>32773 non valido</dt> </dl>                      | Un parametro non è valido.<br/>                  |
| <dl> <dt>**Sistema in uso**</dt> <dt>32774</dt> </dl>                      | Il sistema è in uso.<br/>                          |
| <dl> <dt>**Stato non valido per questa operazione**</dt> <dt>32775</dt> </dl>       | Lo stato non è valido per questa operazione.<br/> |
| <dl> <dt>**Tipo di dati**</dt> <dt>32776 non corretto</dt> </dl>                    | Tipo di dati non corretto.<br/>                       |
| <dl> <dt>**Il sistema non è disponibile**</dt> <dt>32777</dt> </dl>                | Il sistema non è disponibile.<br/>                   |
| <dl> <dt>**Memoria insufficiente**</dt> <dt>32778</dt> </dl>                          | Memoria insufficiente.<br/>                             |



 

## <a name="remarks"></a>Commenti

Questo metodo viene in genere chiamato nel sistema host per determinare se l'host dispone di memoria video sufficiente per ospitare una RemoteFX virtuale. A tale scopo, confrontare la quantità di memoria video calcolata da questo metodo con la proprietà [**\_ Msvm PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) per determinare se la memoria video disponibile nel computer host è sufficiente. È possibile usare queste informazioni per determinare se una macchina virtuale può essere spostata nel sistema host.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ PhysicalGPUInfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**Msvm \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




