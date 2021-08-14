---
description: Rappresenta le funzionalità di visualizzazione supportate del monitor.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Classe SupportedDisplayFeaturesDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a9e71eeda4ab47cba5e88a548421c89815b7d0d87d511709b9a73573e2582077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321537"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>Classe SupportedDisplayFeaturesDescriptor

**SupportedDisplayFeaturesDescriptor rappresenta** le funzionalità di visualizzazione supportate del monitor. Le informazioni in questa classe corrispondono ai dati nella definizione di input video dello standard VESA (Video Electronics Standard Association) Enhanced Extended Display Identification Data (E-EDID).

## <a name="syntax"></a>Sintassi

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a>Members

La **classe SupportedDisplayFeaturesDescriptor** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SupportedDisplayFeaturesDescriptor** ha queste proprietà.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Supporto per alimentazione attiva disattivata e a potenza molto bassa. Lo schermo consuma meno potenza quando riceve un segnale di temporizzazione non compreso nell'intervallo operativo attivo dichiarato. Lo schermo tornerà al normale funzionamento se il segnale temporale torna all'intervallo operativo normale. Esempi di segnali di temporizzazione al di fuori dell'intervallo operativo normale sono i segnali di sincronizzazione o nessun segnale DE.

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di visualizzazione per il monitoraggio. Nella tabella seguente sono elencati i valori possibili.



| Valore                                                                              | Significato                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Schermo monocromatico/in scala di grigi<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Visualizzazione dei colori RGB<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Visualizzazione multicolore non RGB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la visualizzazione dispone del supporto GTF. Se **True,** la visualizzazione supporta intervalli basati sullo standard GTF usando i valori predefiniti dei parametri GTF.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la visualizzazione ha una modalità di temporizzazione preferita. Se **True,** il primo blocco di temporizzazione dettagliato contiene la modalità di temporizzazione preferita del monitoraggio. L'uso della modalità di temporizzazione preferita è richiesto da EDID v.1.3 e versioni successive.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** la visualizzazione supporta sRGB.

</dd> <dt>

**Standby Supportato**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se lo schermo supporta lo standby DISA Display Power Management Signaling (DPMS). Se **True,** dpms standby è supportato.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la visualizzazione supporta la sospensione di VESA Display Power Management Signaling (DPMS). Se **True,** DPMS sospende è supportato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




