---
title: Classe Win32_TSGeneralSetting
description: Rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting classe Servizi Desktop remoto
- Win32_TSGeneralSetting classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: de2cc2e7ede46b503e0d33f65c5735d5e0cc653a75184384be2d706bfc8ac9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999811"
---
# <a name="win32_tsgeneralsetting-class"></a>Classe \_ TSGeneralSetting Win32

La **classe WMI Win32 \_ TSGeneralSetting** rappresenta le impostazioni generali del terminale, ad esempio il livello di crittografia e il protocollo di trasporto.

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

La **classe Win32 \_ TSGeneralSetting** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ TSGeneralSetting** include questi metodi.



| Metodo                                                                                        | Descrizione                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Imposta il livello di crittografia.<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Imposta il livello di sicurezza su uno dei livelli di sicurezza RDP (0), "Negotiate" (1) o "SSL" (2).<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Abilita o disabilita il requisito che gli utenti devono essere autenticati in fase di connessione impostando il valore **della proprietà UserAuthenticationRequired.**<br/> |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSGeneralSetting** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa di una riga) dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CertificateName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per il nome soggetto del certificato personale del computer locale.

</dd> <dt>

**Certificati**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene un archivio certificati serializzato che contiene tutti i certificati dell'archivio **account** utente personali del computer che sono certificati server validi per l'uso con SSL (Secure Sockets Layer).

</dd> <dt>

**Commento**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Nome descrittivo della combinazione di livello sessione e protocollo di trasporto.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Basso** ("Solo i dati inviati dal client al server sono protetti dalla crittografia in base al livello di protezione della chiave standard del server. I dati inviati dal server al  client non sono protetti."), Media ("Tutti i dati inviati tra server e client sono protetti dalla crittografia in base al livello di attendibilità della chiave standard del server."),  Alto ("Tutti i dati inviati tra server e client sono protetti dalla crittografia in base alla potenza massima della chiave del server").
</dt> </dl>

Livello di crittografia minimo.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Basso** (1)


</dt> <dd>

Basso livello di crittografia. Solo i dati inviati dal client al server vengono crittografati usando la crittografia a 56 bit. Tenere presente che i dati inviati dal server al client non sono crittografati.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Media/Compatibile con il client** (2)


</dt> <dd>

Livello di crittografia compatibile con il client. Tutti i dati inviati dal client al server e dal server al client vengono crittografati alla massima potenza della chiave supportata dal client.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (3)


</dt> <dd>

Livello elevato di crittografia. Tutti i dati inviati dal client al server e dal server al client vengono crittografati usando la crittografia avanzata a 128 bit. I client che non supportano questo livello di crittografia non possono connettersi.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Conforme a FIPS** (4)


</dt> <dd>

Crittografia conforme a FIPS. Tutti i dati inviati dal client al server e dal server al client vengono crittografati e decrittografati con gli algoritmi di crittografia Federal Information Processing Standard (FIPS) usando i moduli di crittografia Microsoft. FIPS è uno standard intitolato "Requisiti di sicurezza per i moduli crittografici". FIPS 140-1 (1994) e FIPS 140-2 (2001) descrivono i requisiti governativi per i moduli di crittografia hardware e software usati all'interno del governo degli Stati Uniti.

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà MinEncryptionLevel** è configurata dal server, da Criteri di gruppo o per impostazione predefinita.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà SecurityLayer** è configurata dal server, da Criteri di gruppo o per impostazione predefinita.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà UserAuthenticationRequired** è configurata dal server, da Criteri di gruppo o per impostazione predefinita.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **RDPSecurityLayer** ("Livello di sicurezza RDP: la comunicazione tra il server e il client userà la crittografia RDP nativa."), **Negotiate** ("Verrà usato il livello più sicuro supportato dal client. Se supportato, verrà usato TLS 1.0"), **SSL** ("SSL (TLS 1.0) verrà usato per l'autenticazione del server e per la crittografia di tutti i dati trasferiti tra il server e il client. Questa impostazione richiede che il server abbia un certificato compatibile con SSL."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")
</dt> </dl>

Specifica il livello di sicurezza utilizzato tra il client e il server.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Livello di sicurezza RDP** (1)


</dt> <dd>

La comunicazione tra il server e il client usa la crittografia RDP nativa.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)


</dt> <dd>

Viene usato il livello più sicuro supportato dal client. Se supportato, viene usato SSL (TLS 1.0).

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

SSL (TLS 1.0) viene usato per l'autenticazione server e per crittografare tutti i dati trasferiti tra il server e il client. Questa impostazione richiede che il server abbia un certificato compatibile con SSL. Questa impostazione non è compatibile con un **valore MinEncryptionLevel** pari a 1.

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)


</dt> <dd>

Nuovo livello di sicurezza.

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica l'hash SHA1 in formato esadecimale del certificato SSL da usare per il server di destinazione.

L'identificazione personale di un certificato può essere trovata usando lo snap-in MMC Certificati nella scheda Dettagli della pagina delle proprietà del certificato.

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato della **proprietà SSLCertificateSHA1Hash.**

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

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un disco rigido abilitato per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati non di operazione includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono in linea, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degraded")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Avvio")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del terminale.

Questa proprietà viene ereditata da [**\_ TerminalSetting Win32.**](win32-terminalsetting.md)

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del protocollo del livello sessione. ad esempio, Microsoft RDP 5.0.

</dd> <dt>

**Trasporto**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di trasporto utilizzato nella connessione. ad esempio TCP, NetBIOS o IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di autenticazione utente utilizzata per le connessioni remote. Se impostato su 1, ovvero abilitato, **UserAuthenticationRequired** richiede l'autenticazione utente in fase di connessione per aumentare la protezione del server dagli attacchi di rete. Solo [Remote Desktop Protocol](remote-desktop-protocol.md) client RDP che supportano RDP versione 6.0 o successiva sono in grado di connettersi. Per evitare interruzioni per gli utenti remoti, è consigliabile distribuire client RDP che supportano la versione appropriata del protocollo prima di abilitare la proprietà .

Usare il [**metodo SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) per abilitare o disabilitare questa proprietà.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

L'autenticazione utente alla connessione è disabilitata.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

L'autenticazione utente alla connessione è abilitata.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se per impostazione predefinita la connessione viene Windows processo di autenticazione standard o a un altro pacchetto di autenticazione installato nel sistema.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

Non viene utilizzato per impostazione predefinita il processo di autenticazione Windows standard.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

Il valore predefinito è il processo di autenticazione Windows standard.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

Tenere presente che le stazioni finestra non associate alla sessione della console non possono accedere ai metodi e alle proprietà di questa classe. Se si tenta di eseguire questa operazione specificando "Console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiranno **WBEM \_ E \_ NOT \_ SUPPORTED**. Questo codice di errore verrà restituito anche se una stazione finestra tenta di chiamare i metodi di questo oggetto allo scopo di aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.

Per connettersi allo spazio \\ dei \\ nomi TerminalServices CIMV2 radice, il livello di autenticazione \\ deve includere la privacy dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione **di RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Per Visual Basic chiamate di script e script, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 

