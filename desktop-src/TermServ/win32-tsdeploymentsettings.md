---
title: Win32_TSDeploymentSettings classe
description: Definisce le impostazioni predefinite che vengono Gestione RemoteApp durante la creazione di Remote Desktop Protocol (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings classe Servizi Desktop remoto
- Win32_TSDeploymentSettings classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f5b5cde779cbd9b8120fa648138611236935080f3517a28a6f19dcee8864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349309"
---
# <a name="win32_tsdeploymentsettings-class"></a>Classe \_ TSDeploymentSettings Win32

Definisce le impostazioni predefinite che vengono Gestione RemoteApp durante la creazione di Remote Desktop Protocol (RDP). Queste impostazioni non influiscono su applicazioni o desktop pubblicati.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSDeploymentSettings** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSDeploymentSettings** ha queste proprietà.

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se consentire lo smussamento del carattere.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa di una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Data di scadenza del certificato. Questo valore viene archiviato come formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) a 64 bit.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Identificazione personale del certificato usato per firmare i file RDP.

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica l'utente da cui viene emesso il certificato.

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica a chi viene rilasciato il certificato.

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Profondità in bit del colore dello schermo. I valori possibili sono 4, 8, 15, 16, 24 e 32.

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Contenuto del file RDP che corrisponde al Impostazioni RDP personalizzato Gestione RemoteApp.

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Contenuto del file RDP che corrisponde alle impostazioni di distribuzione in Gestione RemoteApp. Se questo valore è impostato, le impostazioni di distribuzione RDP sorrendono le impostazioni predefinite in questa classe. Ad esempio, se si imposta la proprietà **GatewayAuthMode** in questa classe e si imposta la proprietà **DeploymentRDPSettings,** la proprietà **GatewayAuthMode** di questa classe verrà ignorata e verrà usato il valore **GatewayAuthMode** di **DeploymentRDPSettings.**

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome del server Host sessione Desktop remoto o nome di dominio completo (FQDN) dell'host sessione Desktop server farm.

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Metodo di autenticazione di Gateway Desktop remoto. Sono possibili i valori seguenti.

<dt>

0
</dt> <dd>

Password

</dd> <dt>

1
</dt> <dd>

Smart card

</dd> <dt>

4
</dt> <dd>

Consente all'utente di selezionare durante la connessione.

</dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome del server Gateway Desktop remoto da usare.

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se usare un server Gateway Desktop remoto per connettersi al server Host sessione Desktop remoto di destinazione attraverso un firewall. Sono possibili i valori seguenti.

<dt>

0
</dt> <dd>

Non usare un server Gateway Desktop remoto.

</dd> <dt>

1
</dt> <dd>

Usare un server Gateway Desktop remoto. Ignorare il server Gateway Desktop remoto per gli indirizzi locali.

</dd> <dt>

2
</dt> <dd>

Usare un server Gateway Desktop remoto.

</dd> <dt>

3
</dt> <dd>

Rilevare automaticamente le impostazioni del server Gateway Desktop remoto.

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Quando possibile, usare le stesse credenziali utente per il server Gateway Desktop remoto e il server Host sessione Desktop remoto.

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se usare un certificato per firmare i file RDP.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Porta**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Porta RDP da usare.

</dd> <dt>

**Opzioni di reindirizzamento**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica le opzioni di reindirizzamento del dispositivo e delle risorse per le connessioni RemoteApp. I flag **per RedirectionOptions** possono essere combinati. Sono possibili i valori seguenti.

<dt>

0
</dt> <dd>

Nessun reindirizzamento di dispositivi o risorse.

</dd> <dt>

1
</dt> <dd>

Reindirizzare le unità disco.

</dd> <dt>

2
</dt> <dd>

Reindirizzare le stampanti.

</dd> <dt>

4
</dt> <dd>

Reindirizzare gli Appunti.

</dd> <dt>

8
</dt> <dd>

Reindirizzare i Plug and Play supportati.

</dd> <dt>

16
</dt> <dd>

Reindirizzare le smart card.

</dd> <dt>

32
</dt> <dd>

Reindirizzare l'audio.

</dd> <dt>

64
</dt> <dd>

Reindirizzare le porte seriali.

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se richiedere l'autenticazione del server.

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

**UseMultimon**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se sono abilitati più monitor per il desktop.

</dd> </dl>

## <a name="remarks"></a>Commenti

È necessario essere un membro del gruppo Administrators per impostare le proprietà usando questa classe.

Se **RequireServerAuth è** impostato su **TRUE,** tenere presente quanto segue:

-   Se il programma RemoteApp è per uso Intranet e tutti i computer client eseguono Windows Server 2008 o Windows Vista, non è necessario configurare il server Host sessione Desktop remoto per usare un certificato SSL. In questo caso, Autenticazione a livello di rete viene usato .
-   È necessario specificare il nome di dominio completo del server o della farm per il valore della **proprietà FarmName.**

Per connettersi allo spazio dei nomi "CIMV2 TerminalServices", il livello di autenticazione \\ deve includere la privacy dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY,** che può essere impostato tramite la funzione COM [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Per Visual Basic chiamate di script e script, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). Vengono installati nel computer quando si aggiunge il ruolo associato. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

