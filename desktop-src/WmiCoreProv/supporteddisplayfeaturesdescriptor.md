---
description: Rappresenta le funzionalità di visualizzazione supportate del monitoraggio.
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
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308855"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>Classe SupportedDisplayFeaturesDescriptor

**SupportedDisplayFeaturesDescriptor** rappresenta le funzionalità di visualizzazione supportate del monitoraggio. Le informazioni contenute in questa classe corrispondono ai dati nella definizione di input video dello standard EDID (video Electronics Standard Association) Enhanced Extended Display Data (VESA).

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

La classe **SupportedDisplayFeaturesDescriptor** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SupportedDisplayFeaturesDescriptor** dispone di queste proprietà.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Supporto per il risparmio di energia attivo e molto basso. La visualizzazione consuma meno energia quando riceve un segnale temporale che non rientra nell'intervallo operativo attivo dichiarato. Se il segnale di temporizzazione torna al normale intervallo operativo, verrà ripristinata l'operazione normale. Esempi di segnali di temporizzazione al di fuori dell'intervallo operativo normale non sono segnali di sincronizzazione o nessun segnale.

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di visualizzazione per il monitoraggio. Nella tabella seguente sono elencati i valori possibili.



| Valore                                                                              | Significato                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Visualizzazione monocromatico/scala di grigi<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Visualizzazione colori RGB<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Visualizzazione multicolore non RGB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la visualizzazione dispone del supporto GTF. Se **true**, la visualizzazione supporta le tempistiche basate sullo standard GTF usando i valori predefiniti del parametro GTF.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la visualizzazione ha una modalità temporizzata preferita. Se **true**, il primo blocco di intervallo dettagliato contiene la modalità di temporizzazione preferita del monitoraggio. L'uso della modalità di temporizzazione preferita è richiesto da EDID v. 1.3 e versioni successive.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, la visualizzazione supporta sRGB.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la visualizzazione supporta la modalità standby per la segnalazione di risparmio energia DPMS (VESA). Se è **true**, DPMS standby è supportato.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la visualizzazione supporta la sospensione di DPMS (Display Power Management Signaling). Se è **true**, DPMS Suspend è supportato.

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

 

 




