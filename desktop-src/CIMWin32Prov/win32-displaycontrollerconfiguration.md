---
description: La \_ classe WMI DisplayControllerConfiguration Win32 rappresenta le informazioni di configurazione della scheda video di un sistema di computer che esegue Windows.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Classe Win32_DisplayControllerConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127335"
---
# <a name="win32_displaycontrollerconfiguration-class"></a>Win32 \_ DisplayControllerConfiguration (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DisplayControllerConfiguration Win32** rappresenta le informazioni di configurazione della scheda video di un sistema di computer che esegue Windows.

Questa classe è obsoleta. Al posto di questa classe, è necessario usare le proprietà nelle classi [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ DisplayControllerConfiguration** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ DisplayControllerConfiguration** dispone di queste proprietà.

<dl> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")
</dt> </dl>

Il numero di bit utilizzato per rappresentare il colore in questa configurazione o i bit in ogni pixel.

Esempio: 8

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
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

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| Planes")
</dt> </dl>

Numero corrente di piani di colore utilizzati nella configurazione di visualizzazione. Un piano colori rappresenta un altro modo per rappresentare i colori pixel. Anziché assegnare un singolo valore RGB a ogni pixel, i piani dei colori separano il grafico in ogni componente del colore primario (rosso, verde, blu) e li archivia nei propri piani. Questo consente una maggiore profondità dei colori nei sistemi video a 8 e 16 bit. I sistemi grafici presenti hanno bitwidth dimensioni sufficienti per archiviare le informazioni relative alla profondità dei colori, vale a dire che è necessario solo un piano di colore.

Esempio: 1

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

**DeviceEntriesInAColorTable**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")
</dt> </dl>

Numero di indici colori in una tabella dei colori di un dispositivo di visualizzazione (se il dispositivo ha una profondità di colore di non più di 8 bit per pixel). Per i dispositivi con profondità dei colori maggiori, viene restituito-1.

Esempio: 256

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")
</dt> </dl>

Numero corrente di penne specifiche del dispositivo. Il valore 0xFFFFFFFF indica che il dispositivo non supporta le penne. Le penne sono proprietà logiche che possono essere assegnate dal controller di visualizzazione per visualizzare i dispositivi e vengono usate per creare linee, bordi di poligoni e testo.

Esempio: 3

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Numero corrente di pixel nella direzione orizzontale (asse x) dello schermo.

Esempio: 1024

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Nome dell'adapter utilizzato in questa configurazione.

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")
</dt> </dl>

Frequenza di aggiornamento della scheda video. Il valore 0 (zero) o 1 (uno) indica che è in uso una frequenza predefinita. Il valore-1 indica che viene utilizzata una velocità ottimale.

Esempio: 72

</dd> <dt>

**ReservedSystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")
</dt> </dl>

Numero corrente di voci di indice dei colori riservate per l'utilizzo da parte del sistema. Questo valore è valido solo per le impostazioni di visualizzazione che usano una tavolozza indicizzata. Le tavolozze indicizzate non vengono usate per le profondità dei colori maggiori di 8 bit per pixel. Se la profondità del colore è maggiore di 8 bit per pixel, questo valore viene impostato su **null**.

Esempio: 20

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
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

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")
</dt> </dl>

Numero corrente di voci di indice dei colori riservate per l'utilizzo da parte del sistema. Questo valore è valido solo per le impostazioni di visualizzazione che usano una tavolozza indicizzata. Le tavolozze indicizzate non vengono usate per le profondità dei colori maggiori di 8 bit per pixel. Se la profondità del colore è maggiore di 8 bit per pixel, questo valore viene impostato su **null**.

Esempio: 20

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Numero corrente di pixel nella direzione verticale (asse y) dello schermo.

Esempio: 768

</dd> <dt>

**VideoMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Descrizione leggibile dall'utente della risoluzione dello schermo e dell'impostazione del colore correnti della visualizzazione.

Esempio: "1024 768 con colori 256"

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ DisplayControllerConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).

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
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

