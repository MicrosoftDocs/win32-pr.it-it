---
title: Classe Win32_TSGeneralSetting
description: Rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGeneralSetting Servizi Desktop remoto
- Classe Win32_TSGeneralSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741775"
---
# <a name="win32_tsgeneralsetting-class"></a>Win32 \_ TSGeneralSetting (classe)

La classe WMI **\_ TSGeneralSetting Win32** rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico. Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSGeneralSetting** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSGeneralSetting** presenta questi metodi.



| Metodo                                                                                        | Descrizione                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Imposta il livello di crittografia.<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Imposta il livello di sicurezza su uno dei "livelli di sicurezza RDP" (0), "Negotiate" (1) o "SSL" (2).<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Abilita o Disabilita il requisito per cui gli utenti devono essere autenticati al momento della connessione impostando il valore della proprietà **UserAuthenticationRequired** .<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSGeneralSetting** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa a una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CertificateName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per il nome soggetto del certificato personale del computer locale.

</dd> <dt>

**Certificati**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene un archivio certificati serializzato contenente tutti i certificati dell'archivio **account utente** del computer che sono certificati server validi per l'utilizzo con SSL (Secure Sockets Layer).

</dd> <dt>

**Commento**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome descrittivo della combinazione del protocollo di trasporto e del livello della sessione.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **low** ("solo i dati inviati dal client al server sono protetti dalla crittografia in base al livello di attendibilità della chiave del server. I dati inviati da server a client non sono protetti. "), **medium** (" tutti i dati inviati tra server e client sono protetti dalla crittografia in base al livello di attendibilità della chiave standard del server "), **alto** (" tutti i dati inviati tra server e client sono protetti con la massima attendibilità della chiave del server in base alla crittografia ").
</dt> </dl>

Livello di crittografia minimo.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bassa** (1)


</dt> <dd>

Basso livello di crittografia. Solo i dati inviati dal client al server vengono crittografati con la crittografia a 56 bit. Tenere presente che i dati inviati dal server al client non sono crittografati.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Compatibilità media/client** (2)


</dt> <dd>

Livello di crittografia compatibile con il client. Tutti i dati inviati da client a server e da server a client vengono crittografati al livello di attendibilità massima supportato dal client.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (3)


</dt> <dd>

Livello elevato di crittografia. Tutti i dati inviati da client a server e da server a client vengono crittografati con la crittografia a 128 bit avanzata. I client che non supportano questo livello di crittografia non possono connettersi.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Conforme allo standard FIPS** (4)


</dt> <dd>

Crittografia conforme a FIPS. Tutti i dati inviati da client a server e da server a client vengono crittografati e decrittografati con gli algoritmi di crittografia Federal Information Processing Standard (FIPS) usando i moduli di crittografia Microsoft. FIPS è uno standard denominato "requisiti di sicurezza per i moduli di crittografia". FIPS 140-1 (1994) e FIPS 140-2 (2001) descrivono i requisiti governativi per i moduli di crittografia hardware e software utilizzati all'interno del governo degli Stati Uniti.

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **MinEncryptionLevel** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceSecurityLayer**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **SecurityLayer** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**PolicySourceUserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la proprietà **UserAuthenticationRequired** è configurata dal server, da criteri di gruppo o per impostazione predefinita.

<dt>

0 (0x0)
</dt> <dd>

Server

</dd> <dt>

1 (0x1)
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2 (0x2)
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**SecurityLayer**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **RDPSecurityLayer** ("livello di sicurezza RDP: comunicazione tra serverand il client utilizzerà la crittografia RDP nativa"), **Negotiate** ("il livello più sicuro supportato dal client verrà usato. Se supportato, verrà usato TLS 1,0. "), **SSL** (" SSL (TLS 1,0) verrà usato per l'autenticazione server, oltre a forencrypting tutti i dati trasferiti tra il server e il client. Per questa impostazione è necessario che il server disponga di un certificato compatibile con SSL. "), **NEWTBD** (" nuovo livello di sicurezza in Longhorn ").
</dt> </dl>

Specifica il livello di sicurezza usato tra il client e il server.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Livello di protezione RDP** (1)


</dt> <dd>

La comunicazione tra il server e il client utilizza la crittografia RDP nativa.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negoziazione** (2)


</dt> <dd>

Viene utilizzato il livello più sicuro supportato dal client. Se supportato, viene usato SSL (TLS 1,0).

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

SSL (TLS 1,0) viene utilizzato per l'autenticazione server e per la crittografia di tutti i dati trasferiti tra il server e il client. Questa impostazione richiede che il server disponga di un certificato compatibile con SSL. Questa impostazione non è compatibile con un valore **MinEncryptionLevel** pari a 1.

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)


</dt> <dd>

Un nuovo livello di sicurezza.

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica l'hash SHA1 in formato esadecimale del certificato SSL per il server di destinazione da utilizzare.

È possibile trovare l'identificazione personale di un certificato tramite lo snap-in MMC certificati della scheda Dettagli della pagina Proprietà certificato.

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato della proprietà **SSLCertificateSHA1Hash** .

<dt>

0 (0x0)
</dt> <dd>

Non valido

</dd> <dt>

1 (0x1)
</dt> <dd>

Autofirmato predefinito

</dd> <dt>

2 (0x2)
</dt> <dd>

Criteri di gruppo predefiniti applicati

</dd> <dt>

3 (0x3)
</dt> <dd>

Personalizzato

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Errore")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Errore di predazione")


</dt> <dd></dd> <dt>



 ("Avvio")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**Terminale**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del terminale.

Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del protocollo di livello sessione. ad esempio, Microsoft RDP 5,0.

</dd> <dt>

**Trasporto**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di trasporto utilizzato nella connessione. ad esempio TCP, NetBIOS o IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di autenticazione utente utilizzato per le connessioni remote. Se impostato su 1, ovvero abilitato, **UserAuthenticationRequired** richiede l'autenticazione dell'utente in fase di connessione per aumentare la protezione del server contro gli attacchi alla rete. Solo i client [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) che supportano la versione 6,0 o successiva di RDP sono in grado di connettersi. Per evitare le rotture per gli utenti remoti, è consigliabile distribuire i client RDP che supportano la versione del protocollo appropriata prima di abilitare la proprietà.

Usare il metodo [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) per abilitare o disabilitare questa proprietà.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

L'autenticazione utente alla connessione è disabilitata.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

L'autenticazione utente alla connessione è abilitata.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica se per la connessione viene utilizzato per impostazione predefinita il processo di autenticazione standard di Windows o un altro pacchetto di autenticazione installato nel sistema.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Per impostazione predefinita, non è il processo di autenticazione standard di Windows.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Il valore predefinito è il processo di autenticazione standard di Windows.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

Tenere presente che le stazioni della finestra non associate alla sessione della console non possono accedere ai metodi e alle proprietà di questa classe. Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiranno **WBEM \_ E \_ non \_ supportati**. Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto allo scopo di aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.

Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6. Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> </dl>

 

