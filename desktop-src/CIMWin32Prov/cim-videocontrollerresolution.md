---
description: La \_ classe CIM VideoControllerResolution rappresenta le varie modalità video che un controller video può supportare.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: Classe CIM_VideoControllerResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878326"
---
# <a name="cim_videocontrollerresolution-class"></a>CIM \_ VideoControllerResolution (classe)

La classe **CIM \_ VideoControllerResolution** rappresenta le varie modalità video che un controller video può supportare. Le modalità video sono definite in base alle possibili risoluzioni orizzontali e verticali, alla frequenza di aggiornamento, alla modalità di analisi e al numero di impostazioni del colore supportate da un controller. Le risoluzioni effettive in uso sono i valori specificati nell'oggetto [**\_ VideoController CIM**](cim-videocontroller.md) .

L'hardware non compatibile con Windows Display Driver Model (WDDM) restituisce valori di proprietà non accurati per le istanze di questa classe.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a>Members

La classe **CIM \_ VideoControllerResolution** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ VideoControllerResolution** dispone di queste proprietà.

<dl> <dt>

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

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")
</dt> </dl>

Risoluzione orizzontale in pixel.

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Frequenza di aggiornamento massima quando un intervallo di frequenze è supportato alle risoluzioni specificate, in Hertz.

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,6 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Frequenza di aggiornamento minima quando un intervallo di frequenze è supportato alle risoluzioni specificate, in Hertz.

</dd> <dt>

**NumberOfColors**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")
</dt> </dl>

Numero di colori supportati nella risoluzione corrente.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")
</dt> </dl>

Frequenza di aggiornamento, in Hertz. Se è supportato un intervallo di frequenze, usare le proprietà **MinRefreshRate** e **MaxRefreshRate** e impostare questa proprietà su 0.

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Risoluzioni di \| monitoraggio DMTF \| 002,5 ")
</dt> </dl>

Modalità di analisi in cui opera il controller.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (3)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operazione non interlacciata** (4)


</dt> <dd>

Operazione non interlacciata

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operazione interlacciata** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("settingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

ID che funge da parte della chiave per l'istanza corrente.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,3 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")
</dt> </dl>

Risoluzione verticale del controller, in pixel.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI implementa la classe **CIM \_ VideoControllerResolution** . La classe **CIM \_ VideoControllerResolution** è una classe dinamica.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

Si noti che questa classe è una classe di base. Se si sta tentando di accedere al controller video tramite WMI, è possibile utilizzare [**Win32 \_ VideoController**](win32-videocontroller.md) .

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

 

