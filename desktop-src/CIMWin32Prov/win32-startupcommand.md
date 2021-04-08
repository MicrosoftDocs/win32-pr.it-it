---
description: Win32 \_ StartupCommand&\# 8194; La classe WMI rappresenta un comando che viene eseguito automaticamente quando un utente accede al computer.
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Classe Win32_StartupCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878225"
---
# <a name="win32_startupcommand-class"></a>Win32 \_ StartupCommand (classe)

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ StartupCommand Win32** rappresenta un comando che viene eseguito automaticamente quando un utente accede al computer.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ StartupCommand** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ StartupCommand** dispone di queste proprietà.

<dl> <dt>

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

**Comando**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")
</dt> </dl>

Comando eseguito dal comando di avvio.

WMI ottiene questi dati dalla chiave del registro di sistema

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Run**

Esempio: "C: \\ Windows \\notepad.exe myfile.txt"

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

**Posizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Windows")
</dt> </dl>

Percorso in cui si trova il comando di avvio sul disco file system.

Ad esempio: HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**Startup** ("Startup")


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**Avvio comune** ("avvio comune")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run")


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**\\ HKLM \\ SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices** ("HKLM \\ \\ software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ RunServices")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| file Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName")
</dt> </dl>

Nome file del comando di avvio.

Esempio: "FindFast"

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

**Utente**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Nome utente per il quale verrà eseguito il comando di avvio.

Esempio: "nome dominio \\ "

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

La proprietà UserSID indica il SID dell'utente per il quale verrà eseguito il comando di avvio. Tale proprietà utente può essere vuota, ma UserSID ancora un valore se non è possibile risolvere il nome utente (ad esempio, nel caso di un utente eliminato). La proprietà è utile per distinguere tra i comandi associati a due utenti diversi con nomi non risolti. Può essere NULL se il comando è associato a elementi che non identificano effettivamente un utente come tutti gli utenti.

Esempio: S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ StartupCommand** deriva dall' [**\_ impostazione CIM**](cim-setting.md).

L'avvio del computer non termina dopo il caricamento del sistema operativo. Al contrario, è possibile configurare il sistema operativo Windows in modo che i comandi di avvio vengano eseguiti ogni volta che viene avviato Windows. I comandi di avvio vengono archiviati nel registro di sistema o come parte del profilo utente e vengono usati per avviare automaticamente gli script o le applicazioni specificati ogni volta che viene caricato Windows.

Nella maggior parte dei casi, i programmi di avvio automatico sono utili. assicurano che alcune applicazioni, ad esempio gli strumenti antivirus, vengano avviate automaticamente ed eseguite ogni volta che viene caricato Windows. Tuttavia, i programmi di avvio automatico possono anche essere responsabili di problemi quali:

-   Computer che importano un tempo eccezionalmente lungo per l'avvio. Questo potrebbe essere il risultato di un numero elevato di applicazioni che devono essere avviate ogni volta che viene avviato Windows.
-   Applicazioni rappresentate nella barra delle applicazioni o in Gestione attività, anche se non sono state avviate dall'utente. Anche se queste applicazioni non causano necessariamente problemi, possono comportare chiamate di help desk da parte di utenti confusi da dove provengono questi programmi e perché sono in esecuzione.
-   Computer che riscontrano problemi anche quando sembrano inattivi. Questi problemi vengono spesso tracciati per i comandi di avvio che sono in esecuzione quando nessuno è consapevole che sono in esecuzione.

Identificare le applicazioni e gli script che vengono eseguiti automaticamente all'avvio è un'attività amministrativa importante, ma complessa, perché i comandi di avvio possono essere archiviati in molte posizioni diverse:

-   HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKLM \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   SystemDrive \\ Documents and Settings \\ tutti gli utenti \\ Start menu \\ programs \\ Startup
-   \\documenti SystemDrive e impostazioni \\ nome utente avvio \\ \\ programmi \\ menu Start

È possibile utilizzare la classe WMI Win32 \_ StartupCommand per enumerare i programmi di avvio automatico indipendentemente dalla posizione in cui sono archiviate le informazioni.

Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema. Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio. Per altre informazioni, vedere [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).

È possibile modificare i valori del registro di sistema in cui **Win32 \_ StartupCommand** ottiene i dati chiamando i metodi del [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI nello script o in C++. Per ulteriori informazioni, vedere [modifica del registro di sistema](../wmisdk/modifying-the-system-registry.md).

## <a name="examples"></a>Esempio

Il codice VBScript seguente enumera i comandi di avvio in un computer.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
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

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
