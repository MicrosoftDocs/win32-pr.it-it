---
description: Calcola la quantità di memoria video necessaria per una macchina virtuale RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Metodo CalculateVideoMemoryRequirements della classe Msvm_Synth3dVideoPool
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
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129746"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Metodo CalculateVideoMemoryRequirements della classe MSVM \_ Synth3dVideoPool

Calcola la quantità di memoria video necessaria per una macchina virtuale RemoteFX.

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

*monitorResolution* \[ in\]
</dt> <dd>

Risoluzione massima del monitor per la macchina virtuale. Deve essere uno dei valori seguenti.



| Valore                                                                        | Significato                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | La risoluzione massima è 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | La risoluzione massima è 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | La risoluzione massima è 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | La risoluzione massima è 1920 1200.<br/> |



 

</dd> <dt>

*numberOfMonitors* \[ in\]
</dt> <dd>

Numero massimo di monitoraggi per la macchina virtuale. Il numero minimo di monitoraggi è uno e il valore massimo dipende dalla risoluzione massima dello schermo. La tabella seguente definisce il numero massimo di monitoraggi consentiti per diverse risoluzioni.



| Soluzione             | Numero massimo di monitoraggi |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[ out\]
</dt> <dd>

Riceve la quantità di memoria video richiesta, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice di stato, che può essere uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                                | Descrizione                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl>                    | Successo.<br/>                                |
| <dl> <dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt> </dl> | Il processo è stato avviato.<br/>                               |
| <dl> <dt>**Errore**</dt> <dt>32768</dt> </dl>                                 | non riuscito.<br/>                                    |
| <dl> <dt>**Accesso negato**</dt> <dt>32769</dt> </dl>                          | Accesso negato.<br/>                             |
| <dl> <dt>**Non supportato**</dt> <dt>32770</dt> </dl>                          | Non supportata.<br/>                             |
| <dl> <dt>**Stato sconosciuto**</dt> <dt>32771</dt> </dl>                      | Lo stato è sconosciuto.<br/>                         |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Timeout.<br/>                                   |
| <dl> <dt>**Parametro non valido**</dt> <dt>32773</dt> </dl>                      | Un parametro non è valido.<br/>                  |
| <dl> <dt>**Sistema in uso**</dt> <dt>32774</dt> </dl>                      | Il sistema è in uso.<br/>                          |
| <dl> <dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt> </dl>       | Lo stato non è valido per questa operazione.<br/> |
| <dl> <dt>**Tipo di dati non corretto**</dt> <dt>32776</dt> </dl>                    | Tipo di dati non corretto.<br/>                       |
| <dl> Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt> </dl>                | Il sistema non è disponibile.<br/>                   |
| <dl> <dt>**Memoria insufficiente**</dt> <dt>32778</dt> </dl>                          | Memoria insufficiente.<br/>                             |



 

## <a name="remarks"></a>Commenti

Questo metodo viene in genere chiamato sul sistema host per determinare se l'host dispone di memoria video disponibile sufficiente per ospitare una macchina virtuale RemoteFX. A tale scopo, confrontare la quantità di memoria video calcolata da questo metodo con la proprietà [**MSVM \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) per determinare se il computer host dispone di memoria video disponibile sufficiente. È possibile utilizzare queste informazioni per determinare se una macchina virtuale può essere spostata nel sistema host.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_PhysicalGPUInfo MSVM**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**\_Synth3dVideoPool MSVM**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




