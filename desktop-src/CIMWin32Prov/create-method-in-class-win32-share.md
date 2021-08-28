---
description: Avvia la condivisione per una risorsa server.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 582e255223b6eb971fd447c7884ff730662a1b344c107791b1a57a074c2c1354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504771"
---
# <a name="create-method-of-the-win32_share-class"></a>Metodo Create della classe Win32 \_ Share

Il **metodo Crea**   [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) avvia la condivisione per una risorsa server.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* \[ Pollici\]
</dt> <dd>

Percorso locale della condivisione Windows locale.

Ad esempio, "C: \\ Programmi".

</dd> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Passa l'alias a un percorso configurato come condivisione in un computer che esegue Windows.

Ad esempio, "public".

</dd> <dt>

*Tipo* \[ Pollici\]
</dt> <dd>

Passa il tipo di risorsa condivisa. I tipi includono unità disco, code di stampa, comunicazioni interprocesso (IPC) e dispositivi generali. Può essere uno dei valori seguenti.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unità disco** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Coda di** stampa (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Amministratore unità disco** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Amministratore coda di** stampa (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Amministratore del** dispositivo (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Amministratore IPC** (2147483651)


</dt> <dd></dd> </dl> </dd> <dt>

*MaximumAllowed* \[ in, facoltativo\]
</dt> <dd>

Limite al numero massimo di utenti autorizzati a usare contemporaneamente questa risorsa.

Esempio: 10. Questo parametro è facoltativo.

</dd> <dt>

*Descrizione* \[ in, facoltativo\]
</dt> <dd>

Commento facoltativo per descrivere la risorsa condivisa. Questo parametro è facoltativo.

</dd> <dt>

*Password* \[ in, facoltativo\]
</dt> <dd>

Password (quando il server è in esecuzione con sicurezza a livello di condivisione) per la risorsa condivisa. Se il server viene eseguito con sicurezza a livello di utente, questo parametro viene ignorato. Questo parametro è facoltativo.

</dd> <dt>

*Accesso* \[ in, facoltativo\]
</dt> <dd>

Descrittore di sicurezza per le autorizzazioni a livello di utente. Un descrittore di sicurezza contiene informazioni sulle autorizzazioni, sul proprietario e sulle funzionalità di accesso della risorsa. Se questo parametro non viene fornito o è **NULL,** tutti gli utenti hanno accesso in lettura alla condivisione. Per altre informazioni, vedere [**Descrittore di sicurezza Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) e Modifica della sicurezza [degli accessi in oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione** riuscita (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Nome non valido** (9)
</dt> <dt>

**Livello non valido** (10)
</dt> <dt>

**Parametro non** valido (21)
</dt> <dt>

**Condivisione duplicata** (22)
</dt> <dt>

**Percorso reindirizzato** (23)
</dt> <dt>

**Dispositivo o directory sconosciuto** (24)
</dt> <dt>

**Nome di rete non trovato** (25)
</dt> <dt>

**Altro** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

**Create** è un metodo statico.

Solo i membri del gruppo locale Administrators o Account Operators o quelli con appartenenza al gruppo operatore Communication, Print o Server possono eseguire **correttamente Create**. L'operatore Print può aggiungere solo code di stampa. L'operatore Communication può aggiungere solo code di dispositivi di comunicazione.

## <a name="examples"></a>Esempio

[L'esempio di PowerShell](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) Esporta e importa file consente di esportare e importare condivisioni file e di impostare le autorizzazioni di condivisione. Analogamente, [l'esempio Crea una condivisione e Imposta autorizzazioni](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) crea anche una nuova condivisione e imposta le autorizzazioni di condivisione.

Il codice di PowerShell seguente crea una condivisione.


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



L'esempio di codice precedente restituisce quanto segue:

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

Nell'esempio di codice C \# seguente viene descritto come chiamare il metodo create.


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Condivisione \_ Win32**](win32-share.md)
</dt> </dl>

 

