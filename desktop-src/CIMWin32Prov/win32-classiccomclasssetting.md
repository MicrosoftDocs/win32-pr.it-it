---
description: Rappresenta le impostazioni di un componente Component Object Model (COM).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305098"
---
# <a name="win32_classiccomclasssetting-class"></a>Win32 \_ ClassicCOMClassSetting (classe)

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClassSetting Win32** rappresenta le impostazioni di un componente Component Object Model (com).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ ClassicCOMClassSetting** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ ClassicCOMClassSetting** dispone di queste proprietà.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")
</dt> </dl>

Identificatore univoco globale (GUID) per l'applicazione COM che utilizza questo componente COM.

</dd> <dt>

**AutoConvertToClsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo \[ default \] ")
</dt> </dl>

GUID della classe COM in cui verrà convertito automaticamente il componente COM.

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ autotreats \[ default \] ")
</dt> </dl>

GUID per il componente COM che emula automaticamente le istanze di questa classe.

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

**ComponentId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Class \\ \\ CLSID \\ \\ {GUID} \[ default \] ")
</dt> </dl>

GUID di questo componente COM.

</dd> <dt>

**Controllo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ controllo")
</dt> </dl>

Il componente COM è un controllo OLE.

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ default \] ")
</dt> </dl>

Percorso del file eseguibile e dell'identificatore di risorsa dell'icona predefinita utilizzata dalla classe.

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

**InprocHandler**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ default \] ")
</dt> </dl>

Percorso completo, incluso FileName o solo filename, per un gestore personalizzato a 16 bit per il componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ default \] ")
</dt> </dl>

Percorso completo, incluso FileName o solo filename, per un gestore personalizzato a 32 bit per il componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ default \] ")
</dt> </dl>

Percorso completo, incluso il nome file o solo il nome file, a una DLL del server in-process a 16 bit per questo componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ default \] ")
</dt> </dl>

Percorso completo, incluso FileName o solo filename, in una DLL del server in-process a 32 bit per questo componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**Inseribile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")
</dt> </dl>

Il componente COM può essere inserito in applicazioni contenitore OLE.

</dd> <dt>

**JavaClass**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] ")
</dt> </dl>

Il componente COM è un componente Java.

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ default \] ")
</dt> </dl>

Percorso completo, incluso FileName o solo filename, in un'applicazione server locale a 16 bit. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ default \] ")
</dt> </dl>

Percorso completo, incluso FileName o solo filename, in un'applicazione server locale a 32 bit. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ default \] ")
</dt> </dl>

Nome completo dell'applicazione COM. Viene utilizzato in aree come il campo dei **risultati** della finestra di dialogo **OLE Incolla speciale** .

</dd> <dt>

**ProgId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ default \] ")
</dt> </dl>

Identificatore a livello di codice associato al componente COM. Il formato di un ProgID è <vendor. <Component. <Version. Questo identificatore non è necessariamente univoco.

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

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ default \] ")
</dt> </dl>

Nome breve dell'applicazione COM (usato nei menu e nei popup).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")
</dt> </dl>

Modello di threading utilizzato dalle classi COM in-process. Se questa proprietà è **null**, non viene utilizzato alcun modello di Threading. Il componente viene creato nel thread principale del client e viene effettuato il marshalling di chiamate da altri thread a questo thread.

Il modello di Apartment specifica che i componenti possono essere immessi da un solo thread. I dati comuni utilizzati da questi tipi di server degli oggetti devono essere protetti da conflitti di thread perché il server oggetti supporta più componenti. Ogni componente può essere inserito simultaneamente da thread diversi.

Il modello gratuito specifica che i componenti non inseriscono alcuna restrizione sui thread o sul numero di thread che possono accedere all'oggetto. L'oggetto non può contenere dati specifici dei thread e deve proteggere i dati dall'accesso simultaneo da parte di più thread. Non è tuttavia possibile accedere ai componenti a thread libero direttamente dai thread di Apartment e viene effettuato il marshalling delle chiamate a tali componenti dall'Apartment client.

Quando si specifica both, i componenti possono essere utilizzati in modalità con threading Apartment o a thread libero. Questi componenti possono essere immessi da più thread, proteggere i dati dai conflitti di thread e non contengono dati specifici del thread.

I valori possibili sono:

<dl> <dd>Apartment</dd> <dd>Libero</dd> <dd>Sia</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Apartment** ("Apartment")


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Gratuito** ("gratuito")


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Both** ("both")


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolboxBitmap32 \[ default \] ")
</dt> </dl>

Nome del modulo e identificatore di risorsa per una bitmap piccola (16x16) usata per la superficie di un pulsante della barra degli strumenti o della casella degli strumenti. Utilizzato quando il componente COM è un controllo OLE o ActiveX.

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Treats \[ default \] ")
</dt> </dl>

GUID di un componente COM in grado di emulare le istanze di questo componente.

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ typelib \[ default \] ")
</dt> </dl>

GUID della libreria dei tipi per il componente COM.

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ versione \[ predefinita \] ")
</dt> </dl>

Numero di versione della classe COM.

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgID \[ default \] ")
</dt> </dl>

Identificatore del programma coerente per tutte le versioni dello stesso programma.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ ClassicCOMClassSetting** è derivata dalla [**\_ comimpostazione Win32**](win32-comsetting.md).

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

[**Comimpostazioni Win32 \_**](win32-comsetting.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

