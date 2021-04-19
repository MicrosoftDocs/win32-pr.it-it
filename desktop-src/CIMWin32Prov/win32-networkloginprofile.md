---
description: Win32 \_ NetworkLoginProfile&\# 8194; La classe WMI rappresenta le informazioni di accesso di rete di un utente specifico in un sistema di computer che esegue Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Classe Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305164"
---
# <a name="win32_networkloginprofile-class"></a>Win32 \_ NetworkLoginProfile (classe)

La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile Win32** rappresenta le informazioni di accesso di rete di un utente specifico in un computer che esegue Windows. Sono inclusi, ad esempio, lo stato delle password, i privilegi di accesso, le quote disco e i percorsi della directory di accesso.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ NetworkLoginProfile** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ NetworkLoginProfile** dispone di queste proprietà.

<dl> <dt>

**AccountExpires**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Acct \_ scade")
</dt> </dl>

L'account scadrà. Questo valore viene calcolato dal numero di secondi trascorsi dal 00:00:00 al 1 gennaio 1970 e viene impostato nel formato seguente: ad aaaammgghhmmss. mmmmmm SUTC.

Esempio: 20521201000230,000000 000

</dd> <dt>

**AuthorizationFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ Flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")
</dt> </dl>

Set di flag che specificano le risorse che un utente è autorizzato a utilizzare o modificare.

<dt>

1 (0x1)
</dt> <dd>

Stampante

</dd> <dt>

2 (0x2)
</dt> <dd>

Comunicazione

</dd> <dt>

4 (0x4)
</dt> <dd>

Server

</dd> <dt>

8 (0x8)
</dt> <dd>

Account

</dd> </dl>

</dd> <dt>

**BadPasswordCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| NetUserEnum")
</dt> </dl>

Numero di volte in cui l'utente immette una password errata durante l'accesso a un computer in cui è in esecuzione Windows.

Esempio: 0

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

**CodePage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ tabella codici \_ ")
</dt> </dl>

Tabella codici per la lingua scelta dall'utente. Una tabella codici è il set di caratteri utilizzato.

</dd> <dt>

**Commento**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ commento")
</dt> </dl>

Commento o descrizione per questo profilo di accesso.

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code")
</dt> </dl>

Codice paese/area geografica per la lingua scelta dall'utente.

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

**Flag**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags"), [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("script", "Account disabled", "Home dir required", "lockout", "password non obbligatoria", "Paswword Can Change", "Encrypted test password allowed", "Temp duplicate account", "Normal account", "account trust tra domini", "account di attendibilità della workstation", "account di attendibilità del server", "senza scadenza password", "account di accesso MNS", "smartcard obbligatoria", "trusted per la delega", "non delegata", "USA solo chiave des", "non richiedere la preautorizzazione", "password scaduta")
</dt> </dl>

Proprietà disponibili per questo profilo di rete.

Le proprietà che è possibile impostare includono:

<dt>

1 (0x1)
</dt> <dd>

Script

Uno script di accesso eseguito. Questo valore deve essere impostato per LAN Manager 2,0.

</dd> <dt>

2 (0x2)
</dt> <dd>

Account disabilitato

L'account dell'utente è disabilitato.

</dd> <dt>

8 (0x8)
</dt> <dd>

Home directory obbligatoria

È necessaria una home directory.

</dd> <dt>

16 (0x10)
</dt> <dd>

Blocco

L'account è attualmente bloccato. Per [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), questo valore può essere cancellato per sbloccare un account bloccato in precedenza. Questo valore non può essere usato per bloccare un account precedentemente sbloccato.

</dd> <dt>

32 (0x20)
</dt> <dd>

Password non richiesta

Non è necessaria alcuna password.

</dd> <dt>

64 (0x40)
</dt> <dd>

Impossibile modificare la password

L'utente non può modificare la password.

</dd> <dt>

128 (0x80)
</dt> <dd>

Password di test crittografata consentita

</dd> <dt>

256 (0x100)
</dt> <dd>

Account duplicato temporaneo

Un account per gli utenti il cui account primario si trova in un altro dominio. Questo account fornisce l'accesso utente al dominio, ma non a un dominio che considera attendibile il dominio. Il gestore utenti fa riferimento a questo tipo di account come account utente locale.

</dd> <dt>

512 (0x200)
</dt> <dd>

Account normale

Tipo di account predefinito che rappresenta un utente tipico.

</dd> <dt>

2048 (0x800)
</dt> <dd>

Account trust tra domini

Consentire a un account attendibile per un dominio che considera attendibile altri domini.

</dd> <dt>

4096 (0x1000)
</dt> <dd>

Account attendibilità workstation

Un account computer per una workstation o un server Windows appartenente a questo dominio.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

Account Trust Server

Un account computer di un controller di dominio di backup che è membro di questo dominio.

</dd> <dt>

65536 (0x10000)
</dt> <dd>

Nessuna scadenza password

</dd> <dt>

131072 (0x20000)
</dt> <dd>

Account di accesso MNS

Tipo di account di accesso MNS (Major node set) che rappresenta un utente MNS.

</dd> <dt>

262144 (0x40000)
</dt> <dd>

Smart Card obbligatoria

</dd> <dt>

524288 (0x80000)
</dt> <dd>

Attendibile per la delega

</dd> <dt>

1048576 (0x100000)
</dt> <dd>

Non delegato

</dd> <dt>

2097152 (0x200000)
</dt> <dd>

USA solo chiave DES

</dd> <dt>

4194304 (0x400000)
</dt> <dd>

Non richiedere la preautorizzazione

</dd> <dt>

8388608 (0x800000)
</dt> <dd>

Password scaduta

Indica che la password è scaduta.

</dd> </dl>

Le proprietà seguenti descrivono il tipo di account. È possibile impostare un solo valore:

-   \_account UF Normal \_
-   \_account con \_ duplicazione temporanea UF \_
-   \_ \_ account attendibilità UF workstation \_
-   \_ \_ account trust server \_ UF
-   \_ \_ account trust tra domini \_ UF

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ nome completo")
</dt> </dl>

Nome completo dell'utente che appartiene al profilo di accesso alla rete. Questa stringa può essere vuota se l'utente sceglie di non associare un nome completo a un nome utente.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir")
</dt> </dl>

Percorso della Home directory dell'utente. Questa stringa può essere vuota se l'utente sceglie di non specificare una home directory.

Esempio: " \\ homedir"

</dd> <dt>

**HomeDirectoryDrive**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")
</dt> </dl>

Lettera di unità assegnata alla Home directory dell'utente per l'accesso.

Esempio: "C:"

</dd> <dt>

**LastLogoff**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Ultima \_ disconnessione")
</dt> </dl>

Ultimo accesso dell'utente al sistema. Questo valore viene calcolato dal numero di secondi trascorsi da 00:00:00, 1 gennaio 1970. Il valore " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " indica che l'ora dell'ultimo disconnessione è sconosciuta. Il formato di questo valore è ad aaaammgghhmmss. mmmmmm SUTC. Per informazioni sulla conversione di questa proprietà nell'ora locale, vedere [attività WMI: date e ore](../wmisdk/wmi-tasks--dates-and-times.md).

Esempio: 19521201000230,000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ ultimo \_ accesso")
</dt> </dl>

Ultimo accesso dell'utente al sistema. Questo valore viene calcolato dal numero di secondi trascorsi da 00:00:00, 1 gennaio 1970. Il formato di questo valore è ad aaaammgghhmmss. mmmmmm SUTC. Per informazioni sulla conversione di questa proprietà nell'ora locale, vedere [attività WMI: date e ore](../wmisdk/wmi-tasks--dates-and-times.md).

Esempio: 19521201000230,000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 ore di \_ accesso \_ ")
</dt> </dl>

Orari durante i quali l'utente può effettuare l'accesso. Ogni bit rappresenta un'unità di tempo specificata dalla proprietà **UnitsPerWeek** . Ad esempio, se l'unità di tempo è ogni ora, il primo bit (bit 0, Word 0) è domenica, 0:00 a 0:59, il secondo bit (bit 1, Word 0) è domenica, 1:00 a 1:59 e così via. Se questo membro è impostato su **null**, non esiste alcuna restrizione temporale. L'ora è impostata su GMT e deve essere regolata per altri fusi orari (ad esempio, GMT meno 8 ore per PST).

</dd> <dt>

**LogonServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server")
</dt> </dl>

Nome del server a cui vengono inviate le richieste di accesso. I nomi dei server devono essere preceduti da due barre rovesciate ( \\ \\ ). Il nome di un server con un asterisco ( \\ \\ \* ) indica che la richiesta di accesso può essere gestita da qualsiasi server di accesso. Una stringa null indica che le richieste vengono inviate al controller di dominio.

Esempio: " \\ \\ MyServer"

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantità massima di spazio su disco disponibile per l'utente. Se MaximumStorage è impostato su USER \_ MAXSTORAGE \_ Unlimited, l'utente può usare tutto lo spazio su disco disponibile.

Esempio: 10 milioni

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ nome")
</dt> </dl>

Account utente in un dominio o in un computer specifico. Il numero di caratteri nel nome non può superare il valore di UNLEN.

Esempio: "somedomain \\ JohnDoe"

</dd> <dt>

**NumberOfLogons**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ accessi")
</dt> </dl>

Numero di volte che l'utente ha tentato di accedere a questo account. Il valore 0xFFFFFFFF indica che il valore è sconosciuto. Questa proprietà viene gestita separatamente in ogni controller di dominio di backup (BDC) nel dominio. Per ottenere un valore accurato, è necessario usare solo il valore più grande di tutti i I BDC.

Example: 4

</dd> <dt>

**Parametri**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parametri")
</dt> </dl>

Spazio accantonato per l'uso da parte delle applicazioni. Questa stringa può essere null oppure può contenere un numero qualsiasi di caratteri prima del carattere null di terminazione. I prodotti Microsoft utilizzano questo membro per archiviare le informazioni di configurazione dell'utente. Non modificare queste informazioni, poiché questo valore è specifico di un'applicazione.

</dd> <dt>

**Password**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age")
</dt> </dl>

Periodo di tempo in cui una password è stata applicata. Questo valore viene misurato dal numero di secondi trascorsi dall'Ultima modifica della password.

Esempio: 00001201000230,000000 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ modale \_ info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ Age")
</dt> </dl>

Data e ora di scadenza della password. Il valore viene impostato nel formato seguente: ad aaaammgghhmmss. mmmmmm SUTC

Esempio: 19521201000230,000000 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ gruppo primario \_ ID")
</dt> </dl>

Identificatore relativo (RID) del gruppo globale primario per questo utente. L'identificatore verifica il gruppo primario a cui appartiene il profilo dell'utente.

</dd> <dt>

**Privilegi**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")
</dt> </dl>

Livello di privilegio assegnato alla proprietà **del \_ nome usri3** .

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

**Guest** (0)


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

**Utente** (1)


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

**Amministratore** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Profilo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ profilo usri3")
</dt> </dl>

Percorso del profilo dell'utente. Questo valore può essere una stringa null, un percorso assoluto locale o un percorso UNC. Un profilo utente contiene impostazioni personalizzabili per ogni utente, ad esempio i colori del desktop.

Esempio: "C: \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ percorso script")
</dt> </dl>

Percorso della directory dello script di accesso dell'utente. Uno script di accesso esegue automaticamente un set di comandi ogni volta che un utente accede a un sistema.

Esempio: "C: \\ Win \\ profiles \\ ThomasSteven"

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

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ unità usri3 \_ alla \_ settimana")
</dt> </dl>

Numero di unità di tempo in cui la settimana è divisa. Viene utilizzato con la proprietà **LogonHours** per limitare l'accesso degli utenti al computer.

Esempio: 168 (ore alla settimana)

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ Comment")
</dt> </dl>

Commento o descrizione definito dall'utente per questo profilo.

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ ID utente")
</dt> </dl>

RID dell'utente. L'identificatore verifica che l'utente esista ed è univoco per questo dominio.

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags")
</dt> </dl>

Tipo di account per cui l'utente dispone dei privilegi.

I valori possibili sono:

-   "Account normale"
-   "Account duplicato"
-   "Account attendibilità workstation"
-   "Account Trust Server"
-   "Account trust tra domini"
-   Sconosciuto

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**Normale account** ("normale account")


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**Account duplicato** ("account duplicato")


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**Account attendibilità workstation** ("account trust workstation")


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**Account trust server** ("account Trust Server")


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

**Account trust tra domini** ("account trust tra domini")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> </dl>

</dd> <dt>

**Workstation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ workstation usri3")
</dt> </dl>

Nomi delle workstation da cui l'utente può effettuare l'accesso. È possibile specificare fino a otto workstation. i nomi devono essere separati da virgole (,). Una stringa null indica nessuna restrizione. Per disabilitare gli accessi da tutte le workstation a questo account, impostare UF \_ ACCOUNTDISABLE nella proprietà **Flags** di questa classe.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ NetworkLoginProfile** deriva dall' [**\_ impostazione CIM**](cim-setting.md).

Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema. Per altre informazioni, vedere [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).

## <a name="examples"></a>Esempio

L'esempio [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell restituisce le informazioni di accesso alla rete per tutti gli utenti di un computer.

Nell'esempio VBScript seguente vengono restituite informazioni di accesso alla rete.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
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

 

 
