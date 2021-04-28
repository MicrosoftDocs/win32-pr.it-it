---
description: 'SystemConfig_Video classe: questa classe è la classe del tipo di evento per gli eventi di configurazione video.'
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: SystemConfig_Video classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716194eb9ceb67b609f886482393795eaef2ef09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105899"
---
# <a name="systemconfig_video-class"></a>Classe Video \_ SystemConfig

Questa classe è la classe del tipo di evento per gli eventi di configurazione video.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
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

La **classe SystemConfig \_ Video** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SystemConfig \_ Video** ha queste proprietà.

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (8), **Max** (256), **Format("s")**
</dt> </dl>

Nome o descrizione dell'adapter.

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (9), **Max** (256), **Format("s")**
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

Numero di bit usati per visualizzare ogni pixel.

</dd> <dt>

**ChipType**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (6), **Max** (256), **Format("s")**
</dt> </dl>

Nome del chip dell'adattatore.

</dd> <dt>

**Dactype**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (7), **Max** (256), **Format("s")**
</dt> </dl>

Nome del chip daC (Digital-to-Analog Converter) dell'adattatore.

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice char16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (10), **Max** (256), **Format("s")**
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

**Flag di stato**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **WmiDataId** (11), **Format("x")**
</dt> </dl>

Flag di stato del dispositivo. Può essere qualsiasi combinazione ragionevole di quanto segue.



| Valore                                                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ COLLEGATO \_ A \_ DESKTOP**</dt> <dt>1 (0x1)</dt> </dl> | Il dispositivo fa parte del desktop.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**VISUALIZZAZIONE \_ DRIVER \_ DI \_ MIRRORING DEL**</dt> DISPOSITIVO <dt>8 (0x8)</dt> </dl>           | Rappresenta uno pseudo dispositivo usato per eseguire il mirroring del disegno dell'applicazione per la connessione a un computer remoto o ad altri scopi. A questo dispositivo è associato uno pseudo monitor invisibile. Ad esempio, Viene utilizzato da NetMeeting.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**VISUALIZZAZIONE \_ DEVICE \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | Il dispositivo ha più modalità di visualizzazione di quelle supportate dai dispositivi di output.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ PRIMARIO \_ DISPOSITIVO**</dt> <dt>4 (0x4)</dt> </dl>                 | Il desktop primario si trova nel dispositivo. Per un sistema con una singola scheda di visualizzazione, questa opzione è sempre impostata. Per un sistema con più schede video, solo un dispositivo può avere questo set.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ RIMOVIBILE**</dt> <dt>32 (0x20)</dt> </dl>                               | Il dispositivo è rimovibile. non può essere la visualizzazione primaria.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**VISUALIZZAZIONE \_ COMPATIBILE \_ CON VGA \_ DEL DISPOSITIVO**</dt> <dt>16 (0x10)</dt> </dl>               | Il dispositivo è compatibile con VGA.<br/>                                                                                                                                                                                     |



 

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
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




