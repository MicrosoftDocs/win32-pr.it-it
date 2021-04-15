---
title: Classe Win32_TSDeploymentSettings
description: Definisce le impostazioni predefinite utilizzate dal Gestione RemoteApp durante la creazione di file di Remote Desktop Protocol (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSDeploymentSettings Servizi Desktop remoto
- Classe Win32_TSDeploymentSettings Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476391"
---
# <a name="win32_tsdeploymentsettings-class"></a>Win32 \_ TSDeploymentSettings (classe)

Definisce le impostazioni predefinite utilizzate dal Gestione RemoteApp durante la creazione di file di Remote Desktop Protocol (RDP). Queste impostazioni non influiscono su applicazioni o desktop pubblicati.

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

La classe **Win32 \_ TSDeploymentSettings** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSDeploymentSettings** dispone di queste proprietà.

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se consentire la smussatura dei caratteri.

</dd> <dt>

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

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Data di scadenza del certificato. Questo valore viene archiviato come formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) a 64 bit.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Identificazione personale del certificato utilizzato per firmare i file RDP.

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica il certificato emesso da.

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica la persona a cui viene rilasciato il certificato.

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Profondità in bit del colore dello schermo. I valori possibili sono 4, 8, 15, 16, 24 e 32.

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Contenuto del file RDP che corrisponde alle impostazioni RDP personalizzate in Gestione RemoteApp.

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Contenuto del file RDP che corrisponde alle impostazioni di distribuzione in Gestione RemoteApp. Se questo valore è impostato, le impostazioni di distribuzione RDP sostituiscono le impostazioni predefinite in questa classe. Se, ad esempio, si imposta la proprietà **GatewayAuthMode** in questa classe e si imposta la proprietà **DeploymentRDPSettings** , la proprietà **GatewayAuthMode** di questa classe verrà ignorata e verrà utilizzato il valore **GatewayAuthMode** del **DeploymentRDPSettings** .

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

**Farmname**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Il nome del server Host sessione Desktop remoto o il nome di dominio completo (FQDN) dell'host sessione Desktop remoto server farm.

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Metodo di autenticazione Gateway Desktop remoto. Sono possibili i valori seguenti.

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

Consenti all'utente di selezionare durante la connessione.

</dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome del server Gateway Desktop remoto da utilizzare.

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se utilizzare un server Gateway Desktop remoto per connettersi al server Host sessione Desktop remoto di destinazione in un firewall. Sono possibili i valori seguenti.

<dt>

0
</dt> <dd>

Non usare un server Gateway Desktop remoto.

</dd> <dt>

1
</dt> <dd>

Utilizzare un server Gateway Desktop remoto. Ignorare il server Gateway Desktop remoto per gli indirizzi locali.

</dd> <dt>

2
</dt> <dd>

Utilizzare un server Gateway Desktop remoto.

</dd> <dt>

3
</dt> <dd>

Rileva automaticamente le impostazioni del server Gateway Desktop remoto.

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Quando possibile, utilizzare le stesse credenziali utente per il server Gateway Desktop remoto e il server Host sessione Desktop remoto.

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se utilizzare un certificato per firmare i file RDP.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Porta**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Porta RDP da utilizzare.

</dd> <dt>

**RedirectionOptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Specifica le opzioni di reindirizzamento delle risorse e del dispositivo per le connessioni RemoteApp. I flag per **RedirectionOptions** possono essere combinati. Sono possibili i valori seguenti.

<dt>

0
</dt> <dd>

Nessun reindirizzamento di dispositivi o risorse.

</dd> <dt>

1
</dt> <dd>

Reindirizza unità disco.

</dd> <dt>

2
</dt> <dd>

Reindirizza le stampanti.

</dd> <dt>

4
</dt> <dd>

Reindirizzare gli Appunti.

</dd> <dt>

8
</dt> <dd>

Reindirizza i dispositivi Plug and Play supportati.

</dd> <dt>

16
</dt> <dd>

Reindirizza le smart card.

</dd> <dt>

32
</dt> <dd>

Reindirizza audio.

</dd> <dt>

64
</dt> <dd>

Reindirizza le porte seriali.

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se richiedere l'autenticazione server.

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

**UseMultimon**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se sono abilitati più monitoraggi per il desktop.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostare le proprietà tramite questa classe, è necessario essere membri del gruppo Administrators.

Se **RequireServerAuth** è impostato su **true**, tenere presente quanto segue:

-   Se il programma RemoteApp è per l'utilizzo nella Intranet e tutti i computer client eseguono Windows Server 2008 o Windows Vista, non è necessario configurare il server Host sessione Desktop remoto per l'utilizzo di un certificato SSL. In questo caso, viene utilizzato Autenticazione a livello di rete.
-   Per il valore della proprietà **farmname** , è necessario specificare il nome di dominio completo del server o della farm.

Per connettersi allo \\ spazio dei nomi "CIMV2 TerminalServices", è necessario che il livello di autenticazione includa la riservatezza dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6. Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). Vengono installati nel computer quando si aggiunge il ruolo associato. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

