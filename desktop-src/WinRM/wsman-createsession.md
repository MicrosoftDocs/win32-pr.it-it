---
title: Metodo WSMan. CreateSession (WSManDisp. h)
description: Crea un oggetto sessione che può quindi essere utilizzato per le operazioni di rete successive.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo CreateSession
- Metodo CreateSession Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518142"
---
# <a name="wsmancreatesession-method"></a>WSMan. CreateSession, metodo

Crea un oggetto [**sessione**](session.md) che può quindi essere utilizzato per le operazioni di rete successive.

## <a name="syntax"></a>Sintassi


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessione* \[ a in, facoltativo\]
</dt> <dd>

Protocollo e servizio a cui connettersi, incluso IPv4 o IPv6. Il formato delle informazioni di connessione è il seguente: < ><  ><>*suffisso* di indirizzo di trasporto. Per esempi, vedere la sezione Osservazioni. Se non viene fornita alcuna informazione di connessione, viene usato il computer locale.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Flag di sessione che specificano il metodo di autenticazione, ad esempio [*Negotiate*](windows-remote-management-glossary.md) Authentication o [*Digest Authentication*](windows-remote-management-glossary.md), per la connessione a un computer remoto. Questi flag specificano anche altre informazioni sulla connessione della sessione, ad esempio la codifica o la crittografia. Questo parametro deve contenere uno o più flag in **\_ \_ WSManSessionFlags** per una connessione remota. Per altre informazioni, vedere [costanti di sessione](session-constants.md). Non sono necessarie impostazioni di flag per una connessione a WinRM nel computer locale. Il valore predefinito è **WSManFlagUseNegotiate**.

Per ulteriori informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md) e il parametro *ConnectionOptions* .

</dd> <dt>

*ConnectionOptions* \[ in, facoltativo\]
</dt> <dd>

Puntatore a un oggetto [**ConnectionOptions**](connectionoptions.md) che contiene un nome utente e una password. Il valore predefinito è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**sessione**](session.md) che può quindi essere utilizzato per eseguire operazioni WinRM locali o remote.

## <a name="remarks"></a>Commenti

Il metodo **CreateSession** Inizializza l'oggetto [**Session**](session.md) raccogliendo parametri, ad esempio flag, credenziali e una stringa di connessione per il parametro *Connection* . **CreateSession** non si connette effettivamente al computer locale o remoto. Se non è possibile stabilire la connessione, si verifica un errore durante la prima operazione di **sessione** , ad esempio [**Get**](session-get.md) o [**enumerate**](session-enumerate.md), dopo la chiamata a **CreateSession**. Questo comportamento è diverso da una connessione [*WMI*](windows-remote-management-glossary.md) a uno [*spazio dei nomi*](windows-remote-management-glossary.md) in un computer remoto. Per ulteriori informazioni, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).

L'esempio di codice VBScript seguente viene usato per chiamare questo metodo.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



Negli esempi seguenti vengono illustrati i diversi formati utilizzati per specificare le informazioni di connessione nel parametro *Connection* . quando si crea una sessione HTTPS, il campo <*Address*> deve corrispondere al nome del certificato del computer server, in caso contrario si verifica un errore:

-   "https://service"

    Usa HTTPS per connettersi al percorso predefinito del servizio Web.

-   "https://service.corp.com/websvcs/wsman"

    Usa HTTPS per connettersi alla posizione specifica del servizio Web.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] "

    Usa HTTPS e IPv6 con la porta predefinita.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] : 9999/WSMan"

    Usa HTTPS e IPv6 con la porta specificata.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene creata una sessione nel computer locale.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



Nell'esempio di codice VBScript seguente viene creata una sessione in un computer remoto identificato da un indirizzo IP. Lo script fornisce un nome utente e una password per un account. I flag **WSManFlagCredUserNamePassword** e **WSManFlagUseBasic** vengono combinati per indicare che l'account è un account locale nel computer remoto. Se la creazione della sessione ha esito negativo, lo script viene terminato. Lo script usa i metodi che restituiscono la costante, ad esempio [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).

Per eseguire questo script, tenere presente che è necessario configurare le impostazioni di configurazione predefinite per client e server per consentire il traffico non crittografato e l'autenticazione di base (**AllowUnencrypted** impostato su **true** e Basic impostato su **true**). Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



Nell'esempio di codice VBScript seguente, l'account è un account di dominio e viene utilizzata l'autenticazione Negotiate. Con l'autenticazione Negotiate, è necessario specificare il nome utente come `computername\username` o `ipaddress\username` .


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> <dt>

[Autenticazione per le connessioni remote](authentication-for-remote-connections.md)
</dt> <dt>

[Installazione e configurazione per Gestione remota Windows](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





