---
description: La \_ classe Win32 VideoConfiguration non è attiva. Non verrà restituita alcuna istanza perché non è presente alcun provider sottostante.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Classe Win32_VideoConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523194"
---
# <a name="win32_videoconfiguration-class"></a>Win32 \_ VideoConfiguration (classe)

La classe **Win32 \_ VideoConfiguration** non è attiva. Non verrà restituita alcuna istanza perché non è presente alcun provider sottostante.

La classe **Win32 \_ VideoConfiguration** rappresenta una configurazione di un sottosistema video. Questa classe è stata deprecata a favore delle proprietà contenute nelle classi [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ VideoConfiguration** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ VideoConfiguration** dispone di queste proprietà.

<dl> <dt>

**ActualColorResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**unità**](../wmisdk/standard-qualifiers.md) ("bits per pixel")
</dt> </dl>

Indica la profondità di colore corrente della visualizzazione video.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterChipType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| ChipType")
</dt> </dl>

Contiene il nome del chip dell'adapter.

Esempio: S3

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Specifica il nome del produttore dell'adapter. Questo nome può essere utilizzato per confrontare la compatibilità del dispositivo con le esigenze del computer.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| DACType")
</dt> </dl>

Indica il nome del chip da digitale a analogico (DAC) utilizzato nell'adapter.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Contiene una descrizione o un nome descrittivo della scheda video.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| VideoMemory"), [**unità**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Indica le dimensioni della memoria della scheda video.

Esempio: 16777216

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \\ \\ DisplayController \\ \\ 0 \\ \\ Identifier")
</dt> </dl>

Indica il tipo di scheda video.

Set di caratteri: alfanumerico

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")
</dt> </dl>

Indica il numero effettivo di bit per pixel che rappresenta la visualizzazione. Questo può essere ridimensionato in base all'impostazione video corrente (rappresentata dalla proprietà ActualColorResolution) dell'utente.

Esempio: 8

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**ColorPlanes**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| Planes")
</dt> </dl>

Indica il numero corrente di piani di colore utilizzati nella visualizzazione video. Un piano colori rappresenta un altro modo per rappresentare i colori del pixel; anziché assegnare un singolo valore RGB a ogni pixel, i piani dei colori separano il grafico in ogni componente del colore principale (blu verde) e li archiviano nei propri piani. In questo modo è possibile ottenere una profondità di colore maggiore nei sistemi video a 8 e 16 bit. I sistemi grafici presenti hanno bitwidth dimensioni sufficienti per archiviare le informazioni relative alla profondità dei colori, rendendo necessario solo un piano di colore.

Esempio: 1

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")
</dt> </dl>

Indica il numero di indici di colore in una tabella dei colori per una visualizzazione video. Questa proprietà viene usata se il dispositivo ha una profondità di colore non superiore a 8 bit per pixel. Per i dispositivi con profondità dei colori maggiori, viene restituito-1.

Esempio: 256

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")
</dt> </dl>

Indica il numero corrente di penne specifiche del dispositivo. Il valore 0xFFFFFFFF indica che il dispositivo non supporta le penne. Le penne vengono utilizzate per creare linee e theborders di oggetti poligonali.

Esempio: 3

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| DriverDate")
</dt> </dl>

Indica la data e l'ora in cui è stato installato il driver video corrente.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")
</dt> </dl>

Indica il numero corrente di pixel nella direzione orizzontale (asse X) dello schermo.

Esempio: 1024

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfPath")
</dt> </dl>

Specifica il percorso del file. inf del driver video.

Esempio: C: \\ Windows \\ system32 \\ drivers

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection")
</dt> </dl>

Indica la sezione del file con estensione inf in cui si trovano le informazioni sul video Win32.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Defaule \| drv")
</dt> </dl>

Indica il nome del driver video installato.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**MonitorManufacturer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Indica il nome del produttore del dispositivo di visualizzazione.

Esempio: NEC

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Monitoraggio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \\ \\ MonitorPeripheral \\ \\ 0 \| Identifier")
</dt> </dl>

Indica il nome del modello del dispositivo di visualizzazione.

Esempio: NEC 5FGp

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Contiene un nome identificativo per la classe di configurazione video.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**PixelsPerXLogicalInch**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")
</dt> </dl>

Indica il numero di pixel per pollice logico lungo l'asse X (direzione orizzontale) dello schermo.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**PixelsPerYLogicalInch**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")
</dt> </dl>

Indica il numero di pixel per pollice logico lungo l'asse Y (direzione verticale) dello schermo.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")
</dt> </dl>

Indica la frequenza di aggiornamento della configurazione video. Il valore 0 o 1 indica che è in uso una frequenza predefinita.

Esempio: 72

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. Interlaced")
</dt> </dl>

Indica se il dispositivo di visualizzazione è interlacciato.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**Non interlacciato** ("non interlacciato")


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

**Interlacciato** ("interlacciato")


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**unità**](../wmisdk/standard-qualifiers.md) ("millimetri")
</dt> </dl>

Specifica l'altezza della schermata fisica.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**ScreenWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unità**](../wmisdk/standard-qualifiers.md) ("millimetri")
</dt> </dl>

Specifica la larghezza della schermata fisica.

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")
</dt> </dl>

Indicates il numero corrente di voci di indice dei colori riservate per l'utilizzo da parte del sistema. Questo valore è valido solo per le impostazioni di visualizzazione che usano una tavolozza indicizzata. Le tavolozze indicizzate non vengono usate per le profondità dei colori maggiori di 8 bit per pixel. Se la profondità del colore è maggiore di 8 bit per pixel, questo valore viene impostato su **null**.

Esempio: 20

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")
</dt> </dl>

Indica il numero corrente di pixel nella direzione verticale (asse Y) dello schermo.

Esempio: 768

Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> </dl>

 

 
