---
description: Rappresenta un Windows sistema operativo basato su sistema operativo installato in un computer.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1df0da4cadf0cd610803b2f456f22049471b28bc5653bc400f4c730cb0c47de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972531"
---
# <a name="win32_operatingsystem-class"></a>Classe OperatingSystem Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 OperatingSystem** rappresenta Windows sistema operativo basato su sistema operativo installato in un computer.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a>Members

La **classe \_ OperatingSystem Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ OperatingSystem Win32** include questi metodi.



| Metodo                                                                                     | Descrizione                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reboot**](reboot-method-in-class-win32-operatingsystem.md)                             | Arresta e riavvia il computer.<br/>                                                                                                                                                                                                           |
| [**SetDateTime**](setdatetime-method-in-class-win32-operatingsystem.md)                   | Consente di impostare la data e l'ora del computer.<br/>                                                                                                                                                                                                                |
| [**Arresto**](shutdown-method-in-class-win32-operatingsystem.md)                         | Scarica programmi e DLL fino al punto in cui è sicuro spegnere il computer.<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | Fornisce il set completo di opzioni di arresto supportate Windows sistemi operativi.<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | Fornisce lo stesso set di opzioni di arresto supportate dal metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) nel sistema operativo **Win32, \_** ma consente anche di specificare commenti, un motivo per l'arresto o un timeout.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ OperatingSystem Win32** ha queste proprietà.

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| DRIVE MAP INFO \_ \_ \| btInt13Unit")
</dt> </dl>

Nome dell'unità disco da cui viene avviato Windows sistema operativo.

Esempio: " \\ \\ Device \\ Harddisk0"

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information strutture \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")
</dt> </dl>

Numero di build di un sistema operativo. Può essere usato per informazioni più precise sulla versione rispetto ai numeri di versione del prodotto.

Esempio: "1381"

</dd> <dt>

**BuildType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows \\ \\ \\ \\ \\ \\ CurrentVersion \| CurrentType")
</dt> </dl>

Tipo di compilazione utilizzato per un sistema operativo.

Esempi: ""retail build"", ""checked build""

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto, ovvero una stringa di una riga. La stringa include la versione del sistema operativo. Ad esempio, "Microsoft Windows 7 Enterprise ". Questa proprietà può essere localizzata.

**Windows Vista e Windows 7:** Questa proprietà può contenere caratteri finali. Ad esempio, la stringa "Microsoft Windows 7 Enterprise " (spazio finale incluso) potrebbe essere necessaria per recuperare informazioni usando questa proprietà.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)LOCALE \| \_ IDEFAULTANSICODEPAGE")
</dt> </dl>

Valore della tabella codici utilizzato da un sistema operativo. Una tabella codici contiene una tabella caratteri che un sistema operativo usa per tradurre stringhe per lingue diverse. Il American National Standards Institute (ANSI) elenca i valori che rappresentano le code pages definite. Se un sistema operativo non usa una tabella codici ANSI, questo membro viene impostato su 0 (zero). La **stringa CodeSet** può usare un massimo di sei caratteri per definire il valore della tabella codici.

Esempio: "1255"

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)LOCALE \| \_ ICOUNTRY")
</dt> </dl>

Codice per il paese/area geografica utilizzato da un sistema operativo. I valori si basano sui prefissi di composizione telefonica internazionale, definiti anche codici paese/area geografica IBM. Questa proprietà può usare un massimo di sei caratteri per definire il valore del codice paese/area geografica.

Esempio: "1" (Stati Uniti)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata nella creazione di un'istanza di . Se usata con altre proprietà chiave della classe , questa proprietà consente l'identificazione univoca di tutte le istanze di questa classe e delle relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem.**](cim-operatingsystem.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della classe di creazione del computer di ambito.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem.**](cim-operatingsystem.md)

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information strutture \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")
</dt> </dl>

**Stringa** con terminazione NULL che indica il Service Pack più recente installato in un computer. Se non è installato alcun Service Pack, la stringa è **NULL.**

Esempio: "Service Pack 3"

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM \_ Key,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome del computer di ambito.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")
</dt> </dl>

Numero, in minuti, un sistema operativo viene compensato dall'ora media di Greenwich (GMT). Il numero è positivo, negativo o zero.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**DataExecutionPrevention \_ 32BitApplications**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Quando la funzionalità hardware di prevenzione dell'esecuzione dei dati è disponibile, questa proprietà indica che la funzionalità è impostata per funzionare per le applicazioni a 32 bit se **True**. Nei computer a 64 bit la funzionalità di prevenzione dell'esecuzione dei dati è configurata nell'archivio [dati configurazione di avvio (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) e le proprietà nel sistema operativo **Win32 \_** vengono impostate di conseguenza.

</dd> <dt>

**DataExecutionPrevention \_ Disponibile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

La prevenzione dell'esecuzione dei dati è una funzionalità hardware per impedire attacchi di sovraccarico del buffer arrestando l'esecuzione di codice nelle pagine di memoria di tipo dati. Se **True,** questa funzionalità è disponibile. Nei computer a 64 bit la funzionalità di prevenzione dell'esecuzione dei dati è configurata nell'archivio BCD e le proprietà nel sistema operativo **Win32 \_** vengono impostate di conseguenza.

</dd> <dt>

**Driver DataExecutionPrevention \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Quando la funzionalità hardware di prevenzione dell'esecuzione dei dati è disponibile, questa proprietà indica che la funzionalità è impostata per funzionare per i driver se **True**. Nei computer a 64 bit la funzionalità di prevenzione dell'esecuzione dei dati è configurata nell'archivio BCD e le proprietà nel sistema operativo **Win32 \_** vengono impostate di conseguenza.

</dd> <dt>

**Supporto di DataExecutionPreventionPolicy \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Indica l'impostazione di Protezione esecuzione programmi applicata. L'impostazione DEP specifica la misura in cui DEP si applica alle applicazioni a 32 bit nel sistema. DEP viene sempre applicato al kernel di Windows.

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)


</dt> <dd>

Dep è disattivato per tutte le applicazioni a 32 bit nel computer senza eccezioni. Questa impostazione non è disponibile per l'interfaccia utente.

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)


</dt> <dd>

Dep è abilitato per tutte le applicazioni a 32 bit nel computer. Questa impostazione non è disponibile per l'interfaccia utente.

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Consenso esplicito** (2)


</dt> <dd>

DEP è abilitato per un numero limitato di file binari, il kernel e tutti i Windows basati su applicazioni. Tuttavia, è disattivata per impostazione predefinita per tutte le applicazioni a 32 bit. Un utente o un amministratore deve scegliere  in modo esplicito **l'impostazione Always On** o Rifiuta esplicitamente prima che DEP possa essere applicato alle applicazioni a 32 bit.

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Rifiutare esplicitamente** (3)


</dt> <dd>

DEP è abilitato per impostazione predefinita per tutte le applicazioni a 32 bit. Un utente o un amministratore può rimuovere in modo esplicito il supporto per un'applicazione a 32 bit aggiungendo l'applicazione a un elenco di eccezioni.

</dd> </dl>

</dd> <dt>

**Eseguire il debug**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ DEBUG")
</dt> </dl>

Il sistema operativo è una build verificata (debug). Se **True**, viene installata la versione di debug. Le compilazioni controllate forniscono il controllo degli errori, la verifica degli argomenti e il codice di debug del sistema. Il codice aggiuntivo in un file binario controllato genera un messaggio di errore del debugger del kernel ed esegue l'interruzione nel debugger. Ciò consente di determinare immediatamente la causa e la posizione dell'errore. Le prestazioni possono essere influenzate da una compilazione controllata a causa del codice aggiuntivo eseguito.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Descrizione del Windows operativo. Alcune interfacce utente, ad esempio quelle che consentono la modifica di questa descrizione, ne limitano la lunghezza a 48 caratteri.

</dd> <dt>

**Distribuito**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True**, il sistema operativo viene distribuito tra più nodi del sistema informatico. In tal caso, questi nodi devono essere raggruppati come cluster.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Livello di crittografia per le transazioni protette: 40 bit, 128 bit *o n*-bit.

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

**40 bit** (0)


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

**128 bit** (1)


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

**n bit** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ForegroundApplicationBoost**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

L'aumento della priorità viene assegnato all'applicazione in primo piano. La boost dell'applicazione viene implementata offrendo a un'applicazione più sezioni di tempo di esecuzione (lunghezze quantistiche).

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (0)


</dt> <dd>

Il sistema aumenta la lunghezza quantistica di 6.

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimo** (1)


</dt> <dd>

Il sistema aumenta la lunghezza quantistica di 12.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (2)


</dt> <dd>

Il sistema aumenta la lunghezza quantistica di 18.

</dd> </dl>

</dd> <dt>

**FreePhysicalMemory**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Numero, in kilobyte, di memoria fisica attualmente inutilizzata e disponibile.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**FreeSpaceInPagingFiles**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| System Memory Impostazioni \| 001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Numero, in kilobyte, di cui è possibile eseguire il mapping nei file di paging del sistema operativo senza causare lo scambio di altre pagine.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**FreeVirtualMemory**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Numero, in kilobyte, di memoria virtuale attualmente inutilizzata e disponibile.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")
</dt> </dl>

L'oggetto Date è stato installato. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LargeSystemCache**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **DEPRECATO**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Questa proprietà è obsoleta e non è supportata.

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Ottimizzazione per le applicazioni** (0)


</dt> <dd>

Ottimizzare la memoria per le applicazioni.

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Ottimizzare per le prestazioni del** sistema (1)


</dt> <dd>

Ottimizzare la memoria per le prestazioni del sistema.

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultimo riavvio del sistema operativo.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**LocalDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemDate", "MIF. DmTF \| General Information \| 001.6")
</dt> </dl>

Versione del sistema operativo della data e dell'ora locali del giorno.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Impostazioni locali**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)LOCALE \| \_ ILANGUAGE")
</dt> </dl>

Identificatore di lingua usato dal sistema operativo. Un identificatore di lingua è un'abbreviazione numerica internazionale standard per un paese o un'area geografica. Ogni lingua ha un identificatore di lingua univoco (LANGID), un valore a 16 bit costituito da un identificatore di lingua primario e un identificatore di lingua secondario.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Nome del produttore del sistema operativo. Per Windows basati su server, questo valore è "Microsoft Corporation".

</dd> <dt>

**MaxNumberOfProcesses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemMaxProcesses")
</dt> </dl>

Numero massimo di contesti di processo che il sistema operativo può supportare. Il valore predefinito impostato dal provider è 4294967295 (0xFFFFFFFF). Se non è presente alcun valore massimo fisso, il valore deve essere 0 (zero). Nei sistemi con un valore massimo fisso, questo oggetto consente di diagnosticare gli errori che si verificano quando viene raggiunto il valore massimo. Se sconosciuto, immettere 4294967295 (0xFFFFFFFF).

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**MaxProcessMemorySize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Numero massimo, in kilobyte, di memoria che può essere allocata a un processo. Per i sistemi operativi senza memoria virtuale, questo valore è in genere uguale alla quantità totale di memoria fisica meno la memoria usata dal BIOS e dal sistema operativo. Per alcuni sistemi operativi, questo valore può essere infinito, nel qual caso è necessario immettere 0 (zero). In altri casi, questo valore può essere una costante, ad esempio 2G o 4G.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**MUILanguages**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

interfaccia utente multilingue Lingue pack (MUI Pack) installate nel computer. Ad esempio, "en-us". Le lingue di MUI Pack sono file di risorse che possono essere installati nella versione inglese del sistema operativo. Quando viene installato un MUI Pack, è possibile modificare la lingua dell'interfaccia utente in una delle 33 lingue supportate.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza del sistema operativo all'interno di un sistema computer.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfLicensedUsers**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di licenze utente per il sistema operativo. Se illimitato, immettere 0 (zero). Se sconosciuto, immettere -1.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfProcesses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemProcesses")
</dt> </dl>

Numero di contesti di processo attualmente caricati o in esecuzione nel sistema operativo.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**NumberOfUsers**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| HOST-RESOURCES-MIB.hrSystemNumUsers")
</dt> </dl>

Numero di sessioni utente per le quali il sistema operativo archivia attualmente le informazioni sullo stato.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**OperatingSystemSKU**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Numero SKU (Stock Keeping Unit) per il sistema operativo. Questi valori sono gli stessi delle costanti **PRODUCT \_ \** _ definite in WinNT.h usate con la [funzione _ *GetProductInfo.* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo)

L'elenco seguente elenca i possibili valori SKU.

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODOTTO \_ UNDEFINED** (0)


</dt> <dd>

Non definito

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODOTTO \_ ULTIMATE** (1)


</dt> <dd>

Ultimate Edition, ad esempio Windows Vista Ultimate.

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODOTTO \_ HOME \_ BASIC** (2)


</dt> <dd>

Home Basic Edition

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODOTTO \_ HOME \_ PREMIUM** (3)


</dt> <dd>

Home Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODOTTO \_ ENTERPRISE** (4)


</dt> <dd>

Enterprise Edition

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODOTTO \_ BUSINESS** (6)


</dt> <dd>

Business Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODOTTO \_ \_SERVER STANDARD** (7)


</dt> <dd>

Windows Server edizione Standard (installazione dell'esperienza desktop)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODOTTO \_ SERVER \_ DATACENTER** (8)


</dt> <dd>

Windows Server Datacenter Edition (installazione dell'esperienza desktop)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODOTTO \_ SMALLBUSINESS \_ SERVER** (9)


</dt> <dd>

Small Business Server Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODOTTO \_ ENTERPRISE \_ SERVER** (10)


</dt> <dd>

Enterprise Edizione server

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODOTTO \_ STARTER** (11)


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODOTTO \_ DATACENTER \_ SERVER \_ CORE** (12)


</dt> <dd>

Datacenter Server Core Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODOTTO \_ SERVER \_ \_ CORE STANDARD** (13)


</dt> <dd>

Standard Server Core Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODOTTO \_ ENTERPRISE \_ SERVER \_ CORE** (14)


</dt> <dd>

Enterprise Server Core Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODOTTO \_ \_SERVER WEB** (17)


</dt> <dd>

Edizione server Web

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODOTTO \_ HOME \_ SERVER** (19)


</dt> <dd>

Home Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODOTTO \_ STORAGE \_ EXPRESS \_ SERVER** (20)


</dt> <dd>

Archiviazione Express Server Edition

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODOTTO \_ SERVER \_ STANDARD \_ DI ARCHIVIAZIONE** (21)


</dt> <dd>

Windows Archiviazione Server edizione Standard (installazione dell'esperienza desktop)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODOTTO \_ SERVER \_ DEL GRUPPO DI LAVORO \_ DI** ARCHIVIAZIONE (22)


</dt> <dd>

Windows Archiviazione Server Workgroup Edition (installazione dell'esperienza desktop)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODOTTO \_ STORAGE \_ ENTERPRISE \_ SERVER** (23)


</dt> <dd>

Archiviazione Enterprise Server Edition

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODOTTO \_ SERVER \_ PER \_ SMALLBUSINESS** (24)


</dt> <dd>

Server For Small Business Edition

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODOTTO \_ SMALLBUSINESS \_ SERVER \_ PREMIUM** (25)


</dt> <dd>

Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODOTTO \_ ENTERPRISE \_ N** (27)


</dt> <dd>

Windows edizione Enterprise

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODOTTO \_ ULTIMATE \_ N** (28)


</dt> <dd>

Windows Ultimate Edition

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODOTTO \_ SERVER \_ \_ WEB CORE** (29)


</dt> <dd>

Windows Server Web Server Edition (installazione server core)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODOTTO \_ SERVER \_ \_ STANDARD V** (36)


</dt> <dd>

Windows Server edizione Standard senza Hyper-V

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODOTTO \_ DATACENTER \_ SERVER \_ V** (37)


</dt> <dd>

Windows Server Datacenter Edition senza Hyper-V (installazione completa)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODOTTO \_ ENTERPRISE \_ SERVER \_ V** (38)


</dt> <dd>

Windows Server edizione Enterprise senza Hyper-V (installazione completa)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODOTTO \_ DATACENTER \_ SERVER \_ CORE \_ V** (39)


</dt> <dd>

Windows Server Datacenter Edition senza Hyper-V (installazione server Core)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODOTTO \_ STANDARD \_ SERVER \_ CORE \_ V** (40)


</dt> <dd>

Windows Server edizione Standard senza Hyper-V (installazione server Core)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODOTTO \_ ENTERPRISE \_ SERVER \_ CORE \_ V** (41)


</dt> <dd>

Windows Server edizione Enterprise senza Hyper-V (installazione server Core)

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODOTTO \_ HYPERV** (42)


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODOTTO \_ STORAGE \_ EXPRESS \_ SERVER \_ CORE** (43)


</dt> <dd>

Archiviazione Server Express Edition (installazione server core)

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODOTTO \_ STORAGE \_ STANDARD \_ SERVER \_ CORE** (44)


</dt> <dd>

Archiviazione Server edizione Standard (installazione server core)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODOTTO \_ STORAGE \_ WORKGROUP \_ SERVER \_ CORE** (45)


</dt> <dd>

Archiviazione Server Workgroup Edition (installazione server core)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODOTTO \_ STORAGE \_ ENTERPRISE \_ SERVER \_ CORE** (46)


</dt> <dd>

Archiviazione Server Workgroup Edition (installazione server core)

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODOTTO \_ PROFESSIONAL** (48)


</dt> <dd>

Windows Professional

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODOTTO \_ SERVER DELLA SOLUZIONE SB \_ \_** (50)


</dt> <dd>

Windows Server Essentials (installazione dell'esperienza desktop)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODOTTO \_ SMALLBUSINESS \_ SERVER \_ PREMIUM \_ CORE** (63)


</dt> <dd>

Small Business Server Premium (installazione di Server Core)

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODOTTO \_ CLUSTER \_ SERVER \_ V** (64)


</dt> <dd>

Windows Server del cluster di calcolo senza Hyper-V

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODOTTO \_ CORE \_ ARM** (97)


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODOTTO \_ CORE** (101)


</dt> <dd>

Windows Casa

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODOTTO \_ WMC \_ PROFESSIONALE** (103)


</dt> <dd>

Windows Professional con Media Center

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODOTTO \_ MOBILE \_ CORE** (104)


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODOTTO \_ IOTUAP** (123)


</dt> <dd>

Windows IoT (Internet delle cose) Core

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODOTTO \_ DATACENTER \_ NANO \_ SERVER** (143)


</dt> <dd>

Windows Server Datacenter Edition (installazione di Nano Server)

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODOTTO \_ NANO \_ \_ SERVER STANDARD** (144)


</dt> <dd>

Windows Server edizione Standard (installazione di Nano Server)

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODOTTO \_ DATACENTER \_ WS \_ SERVER \_ CORE** (147)


</dt> <dd>

Windows Server Datacenter Edition (installazione server core)

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODOTTO \_ SERVER \_ CORE WS \_ \_ STANDARD** (148)


</dt> <dd>

Windows Server edizione Standard (installazione server core)

</dd> </dl>

</dd> <dt>

**Organizzazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows \\ \\ \\ \\ \\ \\ CurrentVersion \| RegisteredOrganization")
</dt> </dl>

Nome della società per l'utente registrato del sistema operativo.

Esempio: "Microsoft Corporation"

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Architettura del sistema operativo, anziché del processore. Questa proprietà può essere localizzata.

Esempio: 32 bit

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| DEFAULT Pannello di controllo International \\ \\ \\ \\ \| Locale")
</dt> </dl>

Versione in lingua del sistema operativo installata. Nell'elenco seguente sono elencati i valori possibili. Esempio: 0x0807 (tedesco, Svizzera).

<dt>

1 (0x1)
</dt> <dd>

Arabo

</dd> <dt>

4 (0x4)
</dt> <dd>

Cinese (semplificato)- Cina

</dd> <dt>

9 (0x9)
</dt> <dd>

Inglese

</dd> <dt>

1025 (0x401)
</dt> <dd>

Arabo - Arabia Saudita

</dd> <dt>

1026 (0x402)
</dt> <dd>

Bulgaro

</dd> <dt>

1027 (0x403)
</dt> <dd>

Catalano

</dd> <dt>

1028 (0x404)
</dt> <dd>

Cinese (tradizionale) - Taiwan

</dd> <dt>

1029 (0x405)
</dt> <dd>

Ceco

</dd> <dt>

1030 (0x406)
</dt> <dd>

Danese

</dd> <dt>

1031 (0x407)
</dt> <dd>

Tedesco (Germania)

</dd> <dt>

1032 (0x408)
</dt> <dd>

Greco

</dd> <dt>

1033 (0x409)
</dt> <dd>

Inglese - Stati Uniti

</dd> <dt>

1034 (0x40A)
</dt> <dd>

Spagnolo - Ordinamento tradizionale

</dd> <dt>

1035 (0x40B)
</dt> <dd>

Finlandese

</dd> <dt>

1036 (0x40C)
</dt> <dd>

Francese (Francia)

</dd> <dt>

1037 (0x40D)
</dt> <dd>

Ebraico

</dd> <dt>

1038 (0x40E)
</dt> <dd>

Ungherese

</dd> <dt>

1039 (0x40F)
</dt> <dd>

Islandese

</dd> <dt>

1040 (0x410)
</dt> <dd>

Italiano (Italia)

</dd> <dt>

1041 (0x411)
</dt> <dd>

Giapponese

</dd> <dt>

1042 (0x412)
</dt> <dd>

Coreano

</dd> <dt>

1043 (0x413)
</dt> <dd>

Olandese (Paesi Bassi)

</dd> <dt>

1044 (0x414)
</dt> <dd>

Norvegese - Bokmal

</dd> <dt>

1045 (0x415)
</dt> <dd>

Polacco

</dd> <dt>

1046 (0x416)
</dt> <dd>

Portoghese (Brasile)

</dd> <dt>

1047 (0x417)
</dt> <dd>

Rhaeto-Romanic

</dd> <dt>

1048 (0x418)
</dt> <dd>

Romeno

</dd> <dt>

1049 (0x419)
</dt> <dd>

Russo

</dd> <dt>

1050 (0x41A)
</dt> <dd>

Croato

</dd> <dt>

1051 (0x41B)
</dt> <dd>

Slovacco

</dd> <dt>

1052 (0x41C)
</dt> <dd>

Albanese

</dd> <dt>

1053 (0x41D)
</dt> <dd>

Svedese

</dd> <dt>

1054 (0x41E)
</dt> <dd>

Thai

</dd> <dt>

1055 (0x41F)
</dt> <dd>

Turco

</dd> <dt>

1056 (0x420)
</dt> <dd>

Urdu

</dd> <dt>

1057 (0x421)
</dt> <dd>

Indonesiano

</dd> <dt>

1058 (0x422)
</dt> <dd>

Ucraino

</dd> <dt>

1059 (0x423)
</dt> <dd>

Bielorusso

</dd> <dt>

1060 (0x424)
</dt> <dd>

Sloveno

</dd> <dt>

1061 (0x425)
</dt> <dd>

Estone

</dd> <dt>

1062 (0x426)
</dt> <dd>

Lettone

</dd> <dt>

1063 (0x427)
</dt> <dd>

Lituano

</dd> <dt>

1065 (0x429)
</dt> <dd>

Persiano

</dd> <dt>

1066 (0x42A)
</dt> <dd>

Vietnamita

</dd> <dt>

1069 (0x42D)
</dt> <dd>

Basco (Basco)

</dd> <dt>

1070 (0x42E)
</dt> <dd>

Serbo

</dd> <dt>

1071 (0x42F)
</dt> <dd>

Macedone (Macedonia settentrionale)

</dd> <dt>

1072 (0x430)
</dt> <dd>

Sutu

</dd> <dt>

1073 (0x431)
</dt> <dd>

Tsonga

</dd> <dt>

1074 (0x432)
</dt> <dd>

Tswana

</dd> <dt>

1076 (0x434)
</dt> <dd>

Xhosa

</dd> <dt>

1077 (0x435)
</dt> <dd>

Zulù

</dd> <dt>

1078 (0x436)
</dt> <dd>

Afrikaans

</dd> <dt>

1080 (0x438)
</dt> <dd>

Faeroese

</dd> <dt>

1081 (0x439)
</dt> <dd>

Hindi

</dd> <dt>

1082 (0x43A)
</dt> <dd>

Maltese

</dd> <dt>

1084 (0x43C)
</dt> <dd>

Gaelico scoziale (Regno Unito)

</dd> <dt>

1085 (0x43D)
</dt> <dd>

Yiddish

</dd> <dt>

1086 (0x43E)
</dt> <dd>

Malese - Malesia

</dd> <dt>

2049 (0x801)
</dt> <dd>

Arabo - Iraq

</dd> <dt>

2052 (0x804)
</dt> <dd>

Cinese (semplificato) - RPC

</dd> <dt>

2055 (0x807)
</dt> <dd>

Tedesco - Svizzera

</dd> <dt>

2057 (0x809)
</dt> <dd>

Inglese - Regno Unito

</dd> <dt>

2058 (0x80A)
</dt> <dd>

Spagnolo - Messico

</dd> <dt>

2060 (0x80C)
</dt> <dd>

Francese - Belgio

</dd> <dt>

2064 (0x810)
</dt> <dd>

Italiano - Svizzera

</dd> <dt>

2067 (0x813)
</dt> <dd>

Olandese - Belgio

</dd> <dt>

2068 (0x814)
</dt> <dd>

Norvegese - Nynorsk

</dd> <dt>

2070 (0x816)
</dt> <dd>

Portoghese (Portogallo)

</dd> <dt>

2072 (0x818)
</dt> <dd>

Romeno - Moldova

</dd> <dt>

2073 (0x819)
</dt> <dd>

Russo - Moldova

</dd> <dt>

2074 (0x81A)
</dt> <dd>

Serbo - Alfabeto latino

</dd> <dt>

2077 (0x81D)
</dt> <dd>

Svedese - Spagna

</dd> <dt>

3073 (0xC01)
</dt> <dd>

Arabo - Arabo - Ebraico

</dd> <dt>

3076 (0xC04)
</dt> <dd>

Cinese (tradizionale) - Hong Kong SAR

</dd> <dt>

3079 (0xC07)
</dt> <dd>

Tedesco - Germania - Germania

</dd> <dt>

3081 (0xC09)
</dt> <dd>

Inglese - Australia

</dd> <dt>

3082 (0xC0A)
</dt> <dd>

Spagnolo - Ordinamento internazionale

</dd> <dt>

3084 (0xC0C)
</dt> <dd>

Francese - Canada

</dd> <dt>

3098 (0xC1A)
</dt> <dd>

Serbo - Cirillico

</dd> <dt>

4097 (0x1001)
</dt> <dd>

Arabo - Libia

</dd> <dt>

4100 (0x1004)
</dt> <dd>

Cinese (semplificato) - Singapore

</dd> <dt>

4103 (0x1007)
</dt> <dd>

Tedesco - Avamburgo

</dd> <dt>

4105 (0x1009)
</dt> <dd>

Inglese - Canada

</dd> <dt>

4106 (0x100A)
</dt> <dd>

Spagnolo - Guatemala

</dd> <dt>

4108 (0x100C)
</dt> <dd>

Francese - Svizzera

</dd> <dt>

5121 (0x1401)
</dt> <dd>

Arabo - Araba - Arabica

</dd> <dt>

5127 (0x1407)
</dt> <dd>

Tedesco - Liechtstein

</dd> <dt>

5129 (0x1409)
</dt> <dd>

Inglese - Nuova Zelanda

</dd> <dt>

5130 (0x140A)
</dt> <dd>

Spagnolo - Costa Rica

</dd> <dt>

5132 (0x140C)
</dt> <dd>

Francese ( Svizzera)

</dd> <dt>

6145 (0x1801)
</dt> <dd>

Arabo – Avaio

</dd> <dt>

6153 (0x1809)
</dt> <dd>

Inglese - Irlanda

</dd> <dt>

6154 (0x180A)
</dt> <dd>

Spagnolo – Spagna

</dd> <dt>

7169 (0x1C01)
</dt> <dd>

Arabo – Alfabeto arabo

</dd> <dt>

7177 (0x1C09)
</dt> <dd>

Inglese - Sudafrica

</dd> <dt>

7178 (0x1C0A)
</dt> <dd>

Spagnolo - Repubblica Popolare Cinese

</dd> <dt>

8193 (0x2001)
</dt> <dd>

Arabo - Oman

</dd> <dt>

8201 (0x2009)
</dt> <dd>

Inglese – Italia

</dd> <dt>

8202 (0x200A)
</dt> <dd>

Spagnolo – Spagna

</dd> <dt>

9217 (0x2401)
</dt> <dd>

Arabo – Alfabeto arabo

</dd> <dt>

9226 (0x240A)
</dt> <dd>

Spagnolo – Brasile

</dd> <dt>

10241 (0x2801)
</dt> <dd>

Arabo – Avana

</dd> <dt>

10249 (0x2809)
</dt> <dd>

Inglese - Sottotitolare

</dd> <dt>

10250 (0x280A)
</dt> <dd>

Spagnolo - Perù

</dd> <dt>

11265 (0x2C01)
</dt> <dd>

Arabo – Alfabeto arabo

</dd> <dt>

11273 (0x2C09)
</dt> <dd>

Inglese - Trinidad

</dd> <dt>

11274 (0x2C0A)
</dt> <dd>

Spagnolo ( Brasile)

</dd> <dt>

12289 (0x3001)
</dt> <dd>

Arabo - Leova

</dd> <dt>

12298 (0x300A)
</dt> <dd>

Spagnolo – Spagna

</dd> <dt>

13313 (0x3401)
</dt> <dd>

Arabo – Alfabeto arabo

</dd> <dt>

13322 (0x340A)
</dt> <dd>

Spagnolo ( Brasile)

</dd> <dt>

14337 (0x3801)
</dt> <dd>

Arabo - U.A.E.

</dd> <dt>

14346 (0x380A)
</dt> <dd>

Spagnolo – Svizzera

</dd> <dt>

15361 (0x3C01)
</dt> <dd>

Arabo – Brasile

</dd> <dt>

15370 (0x3C0A)
</dt> <dd>

Spagnolo - Paraguay

</dd> <dt>

16385 (0x4001)
</dt> <dd>

Arabo – Alfabeto arabo

</dd> <dt>

16394 (0x400A)
</dt> <dd>

Spagnolo – Spagna

</dd> <dt>

17418 (0x440A)
</dt> <dd>

Spagnolo - El El

</dd> <dt>

18442 (0x480A)
</dt> <dd>

Spagnolo – Islanda

</dd> <dt>

19466 (0x4C0A)
</dt> <dd>

Spagnolo – Spagna

</dd> <dt>

20490 (0x500A)
</dt> <dd>

Spagnolo - Portorico

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ \| ProductOptions ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")
</dt> </dl>

Aggiunte di prodotti di sistema installati e concessi in licenza al sistema operativo. Ad esempio, il valore 146 (0x92) per **OSProductSuite** indica Enterprise, Servizi terminal e Data Center (bit uno, quattro e sette set). Nell'elenco seguente sono elencati i valori possibili.

<dt>

1 (0x1)
</dt> <dd>

Microsoft Small Business Server è stato installato una volta, ma potrebbe essere stato aggiornato a un'altra versione di Windows.

</dd> <dt>

2 (0x2)
</dt> <dd>

Windows Server 2008 Enterprise installato.

</dd> <dt>

4 (0x4)
</dt> <dd>

Windows I componenti di BackOffice sono installati.

</dd> <dt>

8 (0x8)
</dt> <dd>

Il server di comunicazione è installato.

</dd> <dt>

16 (0x10)
</dt> <dd>

Servizi terminal è installato.

</dd> <dt>

32 (0x20)
</dt> <dd>

Microsoft Small Business Server viene installato con la licenza client restrittiva.

</dd> <dt>

64 (0x40)
</dt> <dd>

Windows Embedded è installato.

</dd> <dt>

128 (0x80)
</dt> <dd>

Viene installata un'edizione Datacenter.

</dd> <dt>

256 (0x100)
</dt> <dd>

Servizi terminal è installato, ma è supportata una sola sessione interattiva.

</dd> <dt>

512 (0x200)
</dt> <dd>

Windows È installata l'edizione Home.

</dd> <dt>

1024 (0x400)
</dt> <dd>

Installazione di Web Server Edition.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Archiviazione Server Edition è installato.

</dd> <dt>

16384 (0x4000)
</dt> <dd>

Compute Cluster Edition è installato.

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")
</dt> </dl>

Tipo di sistema operativo. L'elenco seguente identifica i valori possibili.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MACOS** (2)


</dt> <dd>

Macro

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span id="AIX"></span><span id="aix"></span>**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span id="MVS"></span><span id="mvs"></span>**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span id="OS400"></span><span id="os400"></span>**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**WIN95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**WIN98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**WINCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span id="OSF"></span><span id="osf"></span>**OSF** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenziante** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span id="IRIX"></span><span id="irix"></span>**IRIX** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)


</dt> <dd>

Solaris

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**LINUX** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**Sistema operativo 9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel MACH** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Insinale** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (61)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**TPF** (62)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Descrizione aggiuntiva per la versione corrente del sistema operativo.

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**PAEEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **True,** le estensioni degli indirizzi fisici (PAE) vengono abilitate dal sistema operativo in esecuzione nei processori Intel. PAE consente alle applicazioni di risolvere più di 4 GB di memoria fisica. Quando PAE è abilitato, il sistema operativo usa la conversione degli indirizzi lineare a tre livelli anziché a due livelli. Se si fornisce più memoria fisica a un'applicazione, si riduce la necessità di scambiare memoria con il file di pagina e si aumentano le prestazioni. Per abilitare PAE, usare l'opzione "/PAE" nel file Boot.ini file. Per altre informazioni sulla funzionalità Estensione indirizzi fisici, vedere <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .

</dd> <dt>

**PlusProductID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| Plus! ProductId")
</dt> </dl>

Non supportata.

</dd> <dt>

**PlusVersionNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| Plus! VersionNumber")
</dt> </dl>

Non supportata.

</dd> <dt>

**PortableOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il sistema operativo è stato avviato da un dispositivo USB esterno. Se true, il sistema operativo ha rilevato che si sta avviando in un dispositivo di archiviazione connesso localmente supportato.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 8 e Windows Server 2012.

</dd> <dt>

**Server/istanza primaria**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Specifica se si tratta del sistema operativo primario.

</dd> <dt>

**ProductType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Informazioni aggiuntive sul sistema.

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**Stazione di lavoro** (1)


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**Controller di** dominio (2)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Server** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")
</dt> </dl>

Non supportato

**Windows Server 2008 e Windows Vista: **

La **proprietà QuantumLength** definisce il numero di tick di clock per quantum. Un quantum è un'unità di tempo di esecuzione che l'utilità di pianificazione può concedere a un'applicazione prima di passare ad altre applicazioni. Quando un thread esegue un quantum, il kernel lo pre-esegue e lo sposta alla fine di una coda per le applicazioni con priorità uguali. La lunghezza effettiva del quantistico di un thread varia in diverse Windows diverse. Solo Windows NT/Windows 2000.

I valori possibili sono .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

**Un tick** (1)


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

**Due tick** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**QuantumType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Non supportato

**Windows Server 2008 e Windows Vista: **

La **proprietà QuantumType** specifica i quanti a lunghezza fissa o variabile. Windows'impostazione predefinita è quantum a lunghezza variabile in cui l'applicazione in primo piano ha un quantum più lungo rispetto alle applicazioni in background. Windows Il valore predefinito del server è quantum a lunghezza fissa. Un quantum è un'unità di tempo di esecuzione che l'utilità di pianificazione può concedere a un'applicazione prima di passare a un'altra applicazione. Quando un thread esegue un quantum, il kernel lo pre-esegue e lo sposta alla fine di una coda per le applicazioni con priorità uguali. La lunghezza effettiva del quantistico di un thread varia in diverse Windows diverse.

I valori possibili sono .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Risolto** (1)


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**Variabile** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**RegisteredUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| RegisteredOwner")
</dt> </dl>

Nome dell'utente registrato del sistema operativo.

Esempio: "Ben Smith"

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \| ProductId")
</dt> </dl>

Numero di identificazione seriale del prodotto del sistema operativo.

Esempio: "10497-OEM-0031416-71674"

</dd> <dt>

**ServicePackMajorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information strutture \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")
</dt> </dl>

Numero di versione principale del Service Pack installato nel sistema del computer. Se non è stato installato alcun Service Pack, il valore è 0 (zero).

</dd> <dt>

**ServicePackMinorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")
</dt> </dl>

Numero di versione secondaria del Service Pack installato nel sistema del computer. Se non è stato installato alcun Service Pack, il valore è 0 (zero).

</dd> <dt>

**SizeStoredInPagingFiles**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| System Memory Impostazioni \| 001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Numero totale di kilobyte che possono essere archiviati nei file di paging del sistema operativo: 0 (zero) indica che non sono presenti file di paging. Tenere presente che questo numero non rappresenta le dimensioni fisiche effettive del file di paging su disco.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un disco rigido abilitato per SMART, potrebbe funzionare correttamente, ma stima un errore nel prossimo futuro). Gli stati non di operazione includono: "Error", "Starting", "Stopping" e "Service". Lo stato del servizio si applica al lavoro amministrativo, ad esempio il ridimensionamento mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre operazioni amministrative. Non tutte queste operazioni sono online, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradato** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** ("Avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**SuiteMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, edizione Enterprise", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")
</dt> </dl>

Flag di bit che identificano le suite di prodotti disponibili nel sistema.

Ad esempio, per specificare sia Personal che BackOffice, **impostare SuiteMask** su `4 | 512` o `516` .

<dt>

1
</dt> <dd>

Piccole imprese

</dd> <dt>

2
</dt> <dd>

Enterprise

</dd> <dt>

4
</dt> <dd>

Backoffice

</dd> <dt>

8
</dt> <dd>

Comunicazioni

</dd> <dt>

16
</dt> <dd>

Servizi terminal

</dd> <dt>

32
</dt> <dd>

Small Business con restrizioni

</dd> <dt>

64
</dt> <dd>

Embedded Edition

</dd> <dt>

128
</dt> <dd>

Datacenter Edition

</dd> <dt>

256
</dt> <dd>

Utente singolo

</dd> <dt>

512
</dt> <dd>

Home Edition

</dd> <dt>

1024
</dt> <dd>

Web Server Edition

</dd> </dl>

</dd> <dt>

**SystemDevice**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funzioni del Registro di sistema Win32API \| \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| Paths \| TargetDevice")
</dt> </dl>

Partizione del disco fisico in cui è installato il sistema operativo.

</dd> <dt>

**SystemDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Funzioni [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))
</dt> </dl>

Directory di sistema del sistema operativo.

Esempio: "C: \\ WINDOWS \\ SYSTEM32"

</dd> <dt>

**SystemDrive**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Lettera dell'unità disco in cui si trova il sistema operativo. Esempio: "C:"

</dd> <dt>

**TotalSwapSpaceSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Spazio di swapping totale in kilobyte. Questo valore può essere **NULL** (non specificato) se lo spazio di swapping non è distinto dai file di pagina. Tuttavia, alcuni sistemi operativi distinguono questi concetti. Ad esempio, in UNIX interi processi possono essere scambiati quando l'elenco di pagine gratuite scende e rimane al di sotto di una quantità specificata.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem.**](cim-operatingsystem.md)

</dd> <dt>

**TotalVirtualMemorySize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Numero, in kilobyte, della memoria virtuale. Ad esempio, questo può essere calcolato aggiungendo la quantità totale di RAM alla quantità di spazio di paging, ad esempio aggiungendo la quantità di memoria in o aggregata dal sistema del computer alla proprietà **SizeStoredInPagingFiles.**

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem.**](cim-operatingsystem.md)

</dd> <dt>

**TotalVisibleMemorySize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")
</dt> </dl>

Quantità totale, in kilobyte, di memoria fisica disponibile per il sistema operativo. Questo valore non indica necessariamente la quantità reale di memoria fisica, ma ciò che viene segnalato al sistema operativo come disponibile.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

Questa proprietà viene ereditata da [**CIM \_ OperatingSystem.**](cim-operatingsystem.md)

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information \| [**Structures OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")
</dt> </dl>

Numero di versione del sistema operativo.

Esempio: "4.0"

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Funzioni \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")
</dt> </dl>

Windows directory del sistema operativo.

Esempio: "C: \\ WINDOWS"

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ OperatingSystem Win32** è derivata da [**CIM \_ OperatingSystem.**](cim-operatingsystem.md)

Qualsiasi sistema operativo che può essere installato in un computer che può eseguire un sistema operativo basato su Windows è un discendente o un membro di questa classe. **Win32 \_ OperatingSystem** è una classe singleton. Per ottenere la singola istanza, usare "@" per la chiave.

A differenza della maggior parte delle altre classi WMI generate da MgmtClassGen, il metodo **OperatingSystem.CreateInstance**() restituirà un **oggetto OperatingSystem** vuoto. Pertanto, se si usa C \# con MgmtClassGen, è possibile usare il codice seguente:


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>Esempio

È possibile trovare un esempio di VBScript che ottiene i dati del sistema operativo e del processore da [**\_ ComputerSystem Win32,**](win32-computersystem.md) [**Win32 \_ Processor**](win32-processor.md)e **Win32 \_ OperatingSystem** negli esempi di argomenti relativi al processore [**Win32. \_**](win32-processor.md)

L'esempio di generazione di Exchange con [PowerShell powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) in TechNet Gallery usa una classe **\_ OperatingSystem Win32** come parte di un'applicazione più grande per generare report sull'ambiente di scambio.

[L'esempio Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) nella raccolta TechNet usa la proprietà **LastBootupTime** per determinare per quanto tempo il server è stato attivo. Nell'esempio viene inoltre utilizzata l'opzione timeout per garantire che la chiamata WMI non si blocchi.

L'esempio di codice VBScript di [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) nella raccolta TechNet usa la classe **\_ OperatingSystem Win32** per recuperare informazioni sul sistema operativo da diversi computer remoti.

Lo script seguente ottiene le istanze di **Win32 \_ OperatingSystem** nello spazio dei nomi predefinito "Root CIMv2" e quindi visualizza informazioni \\ sul sistema operativo.


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



L'esempio di codice di PowerShell seguente visualizza tutte le informazioni operative sul sistema operativo corrente.


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



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

[**CIM \_ OperatingSystem**](cim-operatingsystem.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Attività WMI: sistemi operativi](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[Attività WMI: Hardware del computer](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[Attività WMI: Gestione desktop](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
