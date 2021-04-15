---
title: Proprietà PerformanceFlags di IMsRdpClientAdvancedSettings
description: Specifica un set di funzionalità che è possibile impostare nel server per migliorare le prestazioni.
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PerformanceFlags
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400445"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a>IMsRdpClientAdvancedSettings::P proprietà erformanceFlags

Specifica un set di funzionalità che è possibile impostare nel server per migliorare le prestazioni.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a>Valore proprietà

Nuovi flag. Il valore predefinito è 0 (le **prestazioni di Servizi terminal \_ \_ \_ non sono valide**).

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**Servizi terminal \_ \_ \_ Non disabilitare le prestazioni** (0x00000000)


</dt> <dd>

Nessuna funzionalità è disabilitata.

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**Servizi terminal \_ \_ \_ Sfondo prestazioni disabilitato** (0x00000001)


</dt> <dd>

Lo sfondo sul desktop non viene visualizzato.

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**Servizi terminal \_ PERF \_ Disable \_ FULLWINDOWDRAG** (0x00000002)


</dt> <dd>

Il trascinamento della finestra completa è disabilitato; Quando la finestra viene spostata, viene visualizzata solo la struttura della finestra.

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**Servizi terminal \_ PERF \_ Disable \_ MENUANIMATIONS** (0x00000004)


</dt> <dd>

Le animazioni dei menu sono disabilitate.

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**Servizi terminal \_ PERF \_ Disable \_** (0x00000008)


</dt> <dd>

I temi sono disabilitati.

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**Servizi terminal \_ \_Abilitazione della \_ funzionalità grafica migliorata** (0x00000010)


</dt> <dd>

Abilita la grafica migliorata.

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**Servizi terminal \_ \_Disattiva \_ \_ ombreggiatura cursore** (0x00000020)


</dt> <dd>

Per il cursore non viene visualizzata alcuna ombreggiatura.

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**Servizi terminal \_ PERF \_ Disable \_ CURSORSETTINGS** (0x00000040)


</dt> <dd>

Il cursore lampeggiante è disabilitato.

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**Servizi terminal \_ PRESTAZIONI \_ Abilita \_ \_ smussatura carattere** (0x00000080)


</dt> <dd>

Abilitare la smussatura dei caratteri.

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**Servizi terminal \_ PERF \_ enable \_ Desktop \_ Composition** (0x00000100)


</dt> <dd>

Abilitare composizione desktop.

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**Servizi terminal \_ \_Impostazione di \_ NONPERFCLIENT \_ default Perf** (0x40000000)


</dt> <dd>

Impostare internamente per i client che non sono in grado di riconoscere questa impostazione.

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**Servizi terminal \_ PRESTAZIONI \_ RESERVED1** (0x80000000)


</dt> <dd>

Riservato e usato internamente dal client.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                  |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





