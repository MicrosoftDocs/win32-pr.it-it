---
description: La \_ classe Win32 DesktopWMI rappresenta le caratteristiche comuni del desktop di un utente. Le proprietà di questa classe possono essere modificate dall'utente per personalizzare il desktop.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Classe Win32_Desktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878362"
---
# <a name="win32_desktop-class"></a>\_Classe desktop Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) per **\_ desktop Win32** rappresenta le caratteristiche comuni del desktop di un utente. Le proprietà di questa classe possono essere modificate dall'utente per personalizzare il desktop.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a>Members

La **classe \_ desktop Win32** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ desktop Win32** dispone di queste proprietà.

<dl> <dt>

**SpessoreBordo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| BorderWidth ")
</dt> </dl>

Larghezza dei bordi intorno a tutte le finestre con bordi regolabili.

Esempio: 3

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

**CoolSwitch**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| CoolSwitch")
</dt> </dl>

Il cambio rapido delle attività è attivato. Il cambio rapido attività consente all'utente di spostarsi tra le finestre utilizzando la combinazione di tasti **ALT + TAB** .

</dd> <dt>

**CursorBlinkRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| CursorBlinkRate"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")
</dt> </dl>

Intervallo di tempo tra il cursore successivo lampeggia.

Esempio: 530

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

**DragFullWindows**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| DragFullWindows")
</dt> </dl>

Il contenuto di una finestra viene visualizzato quando un utente sposta la finestra.

</dd> <dt>

**GridGranularity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| GridGranularity"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixel")
</dt> </dl>

Spaziatura della griglia a cui sono associate le finestre sul desktop. In questo modo l'organizzazione di Windows risulta più semplice. La spaziatura è in genere sufficiente per evitare che l'utente lo noti.

Esempio: 1

</dd> <dt>

**IconSpacing**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")
</dt> </dl>

Spaziatura tra le icone.

Esempio: 75

</dd> <dt>

**IconTitleFaceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| IconFont ")
</dt> </dl>

Tipo di carattere utilizzato per i nomi delle icone.

Esempio: "MS San Serif"

</dd> <dt>

**IconTitleSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| font and text Structures \| [**Campo LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Point")
</dt> </dl>

Dimensioni del carattere dell'icona.

Esempio: 9

</dd> <dt>

**IconTitleWrap**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap ")
</dt> </dl>

Il testo del titolo dell'icona viene incapsulato nella riga successiva.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Nome che identifica il profilo desktop corrente.

Esempio: "MainProf"

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Modello di desktop predefinito del \\ \\ Pannello di controllo \\ \\ \| ")
</dt> </dl>

Nome del modello utilizzato come sfondo per il desktop.

</dd> <dt>

**ScreenSaverActive**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| ScreenSaveActive ")
</dt> </dl>

Lo screen saver è attivo.

</dd> <dt>

**ScreenSaverExecutable**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\SCRNSAVE.EXE desktop del pannello di controllo predefinito \\ \\ \| ")
</dt> </dl>

Nome del file eseguibile screen saver corrente.

Esempio: "LOGON. SCR

</dd> <dt>

**ScreenSaverSecure**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| ScreenSaverIsSecure ")
</dt> </dl>

La password è abilitata per la screen saver.

</dd> <dt>

**ScreenSaverTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| ScreenSaveTimeOut "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondi ")
</dt> </dl>

Quantità di tempo che trascorre prima dell'avvio del screen saver.

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

**Wallpaper**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Sfondo del desktop del pannello di controllo predefinito \\ \\ \| ")
</dt> </dl>

Nome del file per la progettazione dello sfondo sullo sfondo del desktop.

Esempio: "WINNT.BMP"

</dd> <dt>

**WallpaperStretched**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| WallpaperStyle ")
</dt> </dl>

Lo sfondo è allungato per riempire l'intera schermata. Microsoft Plus deve essere installato prima che questa opzione sia disponibile. Se **false**, lo sfondo mantiene le dimensioni originali sullo sfondo del desktop.

</dd> <dt>

**WallpaperTiled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| TileWallpaper ")
</dt> </dl>

Lo sfondo è affiancato o centrato.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ desktop Win32** è derivata dall' [**\_ impostazione CIM**](cim-setting.md).

Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema. Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio. Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene descritto come recuperare le informazioni sul desktop.


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

