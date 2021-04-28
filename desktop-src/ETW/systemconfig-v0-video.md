---
description: 'SystemConfig_V0_Video: questa classe è la classe del tipo di evento per gli eventi di configurazione video.'
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: SystemConfig_V0_Video classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94fb9e50344cfbdde4be67815b80e4074ab1a878
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105919"
---
# <a name="systemconfig_v0_video-class"></a>Classe SystemConfig \_ V0 \_ Video

Questa classe è la classe del tipo di evento per gli eventi di configurazione video.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>Members

La **classe SystemConfig \_ V0 \_ Video** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SystemConfig \_ V0 \_ Video** ha queste proprietà.

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8), **Max** (256)
</dt> </dl>

Nome o descrizione dell'adattatore.

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9), **Max** (256)
</dt> </dl>

Nome BIOS della scheda.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (4)
</dt> </dl>

Numero di bit utilizzati per visualizzare ogni pixel.

</dd> <dt>

**ChipType**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **Max** (256)
</dt> </dl>

Nome del chip dell'adapter.

</dd> <dt>

**Dactype**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (7), **Max** (256)
</dt> </dl>

Nome del chip del convertitore da digitale ad analogico (DAC) dell'adapter.

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (1)
</dt> </dl>

Quantità massima di memoria supportata, in byte.

</dd> <dt>

**StateFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11)
</dt> </dl>

Flag di stato del dispositivo. Può essere qualsiasi combinazione ragionevole di quanto segue.



| Valore                                                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ COLLEGATO \_ AL \_ DESKTOP**</dt> <dt>1 (0x1)</dt> </dl> | Il dispositivo fa parte del desktop.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**VISUALIZZAZIONE \_ \_DRIVER MIRRORING DEL \_ DISPOSITIVO**</dt> <dt>8 (0x8)</dt> </dl>           | Rappresenta una pseudo-periferica utilizzata per eseguire il mirroring del disegno dell'applicazione per la connessione a un computer remoto o ad altri scopi. A questo dispositivo è associato uno pseudo monitor invisibile. Ad esempio, Viene utilizzato da NetMeeting.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**VISUALIZZAZIONE \_ DEVICE \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | Il dispositivo ha più modalità di visualizzazione di quelle supportate dai dispositivi di output.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ PRIMARIO \_ DISPOSITIVO**</dt> <dt>4 (0x4)</dt> </dl>                 | Il desktop primario si trova nel dispositivo. Per un sistema con una singola scheda video, questa opzione è sempre impostata. Per un sistema con più schede video, questo set può essere impostato su un solo dispositivo.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ RIMOVIBILE**</dt> <dt>32 (0x20)</dt> </dl>                               | Il dispositivo è rimovibile. non può essere la visualizzazione principale.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ COMPATIBILE \_ VGA**</dt> <dt>16 (0x10)</dt> </dl>               | Il dispositivo è compatibile con VGA.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (5)
</dt> </dl>

Frequenza di aggiornamento corrente, in hertz.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (2)
</dt> </dl>

Numero corrente di pixel orizzontali.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (3)
</dt> </dl>

Numero corrente di pixel verticali.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




