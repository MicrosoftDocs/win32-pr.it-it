---
description: Rappresenta le impostazioni di un Component Object Model (COM).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSetting classe
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
ms.openlocfilehash: 4aa3a60b68902bbcf7728866d24e5cedd831eac35ba629a3e2516a885a28efaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418242"
---
# <a name="win32_classiccomclasssetting-class"></a>Classe Win32 \_ ClassicCOMClassSetting

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ClassicCOMClassSetting** rappresenta le impostazioni di un Component Object Model (COM).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe Win32 \_ ClassicCOMClassSetting** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ ClassicCOMClassSetting** ha queste proprietà.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")
</dt> </dl>

Identificatore univoco globale (GUID) per l'applicazione COM che usa questo componente COM.

</dd> <dt>

**AutoConvertToClsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo Default \[ \] ")
</dt> </dl>

GUID della classe COM in cui verrà convertito automaticamente questo componente COM.

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoTreatAs Default \[ \] ")
</dt> </dl>

GUID per il componente COM che emulerà automaticamente le istanze di questa classe.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} Default \[ \] ")
</dt> </dl>

GUID di questo componente COM.

</dd> <dt>

**Controllo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Control")
</dt> </dl>

Il componente COM è un controllo OLE.

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon Default \[ \] ")
</dt> </dl>

Percorso del file eseguibile e dell'identificatore di risorsa dell'icona predefinita usata dalla classe .

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**InprocHandler**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler Default \[ \] ")
</dt> </dl>

Percorso completo che include il nome file o solo il nome file di un gestore personalizzato a 16 bit per il componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 Default \[ \] ")
</dt> </dl>

Percorso completo che include il nome file o solo il nome file di un gestore personalizzato a 32 bit per il componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer Default \[ \] ")
</dt> </dl>

Percorso completo che include il nome file o solo il nome file di una DLL del server in-process a 16 bit per questo componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 Default \[ \] ")
</dt> </dl>

Percorso completo che include il nome file o solo il nome file di una DLL del server in-process a 32 bit per questo componente COM. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**Inseribile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")
</dt> </dl>

Il componente COM può essere inserito nelle applicazioni contenitore OLE.

</dd> <dt>

**JavaClass**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] ")
</dt> </dl>

Il componente COM è un componente Java.

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer Default \[ \] ")
</dt> </dl>

Percorso completo che include il nome file o solo il nome file di un'applicazione server locale a 16 bit. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 Default \[ \] ")
</dt> </dl>

Percorso completo che include nome file o solo nome file per un'applicazione server locale a 32 bit. Il provider non restituisce sempre il percorso completo.

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 Default \[ \] ")
</dt> </dl>

Nome completo dell'applicazione COM. Viene usato in aree come il campo **Risultati** della finestra di dialogo **Incolla speciale OLE.**

</dd> <dt>

**Progid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID Default \[ \] ")
</dt> </dl>

Identificatore a livello di codice associato al componente COM. Il formato di un ProgID è <Vendor.<Component.<Version. Non è garantito che questo identificatore sia univoco.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 Default \[ \] ")
</dt> </dl>

Nome breve dell'applicazione COM (usato nei menu e nei popup).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")
</dt> </dl>

Modello di threading usato dalle classi COM in-process. Se questa proprietà è **NULL,** non viene usato alcun modello di threading. Il componente viene creato nel thread principale del client e viene effettuato il marshalling delle chiamate da altri thread a questo thread.

Il modello Apartment specifica che i componenti possono essere immessi da un solo thread. I dati comuni contenuti in questi tipi di server oggetti devono essere protetti da conflitti di thread perché il server oggetti supporta più componenti. Ogni componente può essere immesso contemporaneamente da thread diversi.

Il modello Free specifica che i componenti non inserisce alcuna restrizione sui thread o sul numero di thread che possono immettere l'oggetto. L'oggetto non può contenere dati specifici del thread e deve proteggere i dati dall'accesso simultaneo da parte di più thread. I componenti a thread libero, tuttavia, non sono accessibili direttamente dai thread apartment e viene effettuato il marshalling delle chiamate a tali componenti dall'apartment client.

Se si imposta both, i componenti possono essere usati in modalità a thread apartment o a thread libero. Questi componenti possono essere immessi da più thread, proteggere i dati da conflitti di thread e non contengono dati specifici del thread.

I valori possibili sono:

<dl> <dd>"Apartment"</dd> <dd>"Gratuito"</dd> <dd>"Both"</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Apartment** ("Apartment")


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Gratuito** ("Gratuito")


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Both** ("Both")


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 Default \[ \] ")
</dt> </dl>

Nome del modulo e identificatore di risorsa per una piccola bitmap (16x16) usata per il viso di una barra degli strumenti o di un pulsante della casella degli strumenti. Utilizzato quando il componente COM è un controllo OLE o ActiveX controllo.

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs Default \[ \] ")
</dt> </dl>

GUID di un componente COM che può emulare le istanze di questo componente.

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib Default \[ \] ")
</dt> </dl>

GUID per la libreria dei tipi per questo componente COM.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} Version Default \\ \\ \[ \] ")
</dt> </dl>

Numero di versione di questa classe COM.

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId Default \[ \] ")
</dt> </dl>

Identificatore di programma coerente per tutte le versioni dello stesso programma.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe Win32 \_ ClassicCOMClassSetting** è derivata da [**WIN32 \_ COMSetting**](win32-comsetting.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ COMSetting**](win32-comsetting.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

