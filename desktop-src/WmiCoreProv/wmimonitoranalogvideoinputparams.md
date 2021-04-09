---
description: Rappresenta i parametri di input video analogici di un monitor del computer.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Classe WmiMonitorAnalogVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967852"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a>Classe WmiMonitorAnalogVideoInputParams

La classe WMI **WmiMonitorAnalogVideoInputParams** rappresenta i parametri di input video analogici di un monitor computer. I dati in questa classe corrispondono ai dati nella definizione del video di input di video Electronics Standard Association (VESA) Enhanced Extended Display Data (E-EDID) standard. Un'istanza di questa classe è disponibile solo se il valore della proprietà **VideoInputType** della classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) è "analogico".

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a>Members

La classe **WmiMonitorAnalogVideoInputParams** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **WmiMonitorAnalogVideoInputParams** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**CompositeSyncSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la sincronizzazione composita è supportata.



| Valore                                                                              | Significato                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La sincronizzazione composita sulla linea di sincronizzazione orizzontale è supportata.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | La sincronizzazione composita sulla linea di sincronizzazione orizzontale non è supportata.<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**SeparateSyncsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se sono supportate sincronizzazioni separate.



| Valore                                                                              | Significato                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Sono supportate le sincronizzazioni separate.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Le sincronizzazioni separate non sono supportate.<br/> |



 

</dd> <dt>

**SerrationOfVsyncRequired**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è necessaria la seghettazione dell'impulso di sincronizzazione verticale.



| Valore                                                                              | Significato                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La seghettazione dell'impulso di sincronizzazione verticale è obbligatoria quando si usa la sincronizzazione composita o il video Sync-on-Green.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | La seghettazione dell'impulso di sincronizzazione verticale non è necessaria quando si usa la sincronizzazione composita o il video Sync-on-Green.<br/> |



 

</dd> <dt>

**SetupExpected**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se è previsto il programma di installazione.



| Valore                                                                              | Significato                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Il monitoraggio prevede una configurazione vuota o un piedistallo per ogni livello di segnale standard appropriato.<br/>                      |
| <dl> <dt>1 (0x1)</dt> </dl> | Il monitoraggio non prevede una configurazione o un piedistallo da zero a vuoto in base allo standard del livello di segnale appropriato.<br/> |



 

</dd> <dt>

**SignalLevelStandard**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Livello di segnale standard per le connessioni a Enhanced Video Connector (EVC).



| Valore                                                                              | Significato                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | 0.7, 0.3 \[ V\]<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | 0.714, 0.286 \[ V\]<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | 1.0, 0.4 \[ V\]<br/>     |
| <dl> <dt>3 (0x3)</dt> </dl> | 0.7, 0,0 \[ V\]<br/>     |



 

</dd> <dt>

**SyncOnGreenVideoSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la sincronizzazione in verde è supportata.



| Valore                                                                              | Significato                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La sincronizzazione su un video verde è supportata.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | La sincronizzazione su un video verde non è supportata.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




