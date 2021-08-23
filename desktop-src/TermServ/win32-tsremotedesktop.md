---
title: Win32_TSRemoteDesktop classe
description: Descrive una connessione Desktop remoto disponibile tramite Desktop remoto Accesso Web (rd Accesso Web).
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteDesktop classe Servizi Desktop remoto
- Win32_TSRemoteDesktop classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd6bae5e03bd9cb1a73917cfb0e6b121d3b2d57dd30cc2d37bb7e51abf086061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769411"
---
# <a name="win32_tsremotedesktop-class"></a>Classe \_ TSRemoteDesktop Win32

Descrive una connessione Desktop remoto disponibile tramite Desktop remoto Accesso Web (rd Accesso Web).

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ TSRemoteDesktop** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSRemoteDesktop** ha queste proprietà.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Alias della connessione Desktop remoto.

</dd> <dt>

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

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contenuto in byte dell'icona corrispondente alla connessione desktop remoto.

</dd> <dt>

**IconIndex**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indice o ID dell'icona per la connessione desktop remoto.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Percorso dell'icona per la connessione desktop remoto.

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

**IsVmFarm**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se questa connessione Desktop remoto fa parte di una farm di macchine virtuali.

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

**RDPFileContents**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Contenuto del file RDP che corrisponde alla connessione desktop remoto.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Descrittore di sicurezza che controlla l'accesso alla connessione desktop remoto, in formato SDDL. Una stringa vuota implica consentire tutti gli accessi. Questo descrittore di sicurezza non supporta le ACE DENY o le voci ACE che fanno riferimento a utenti o gruppi non di dominio.

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se la connessione Desktop remoto deve essere visualizzata in Connessione Desktop remoto Accesso Web.

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

**VmFarmSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Impostazioni della farm di macchine virtuali per la connessione desktop remoto.

</dd> </dl>

## <a name="remarks"></a>Commenti

È necessario essere un membro del gruppo Administrators per impostare le proprietà usando questa classe.

Per connettersi allo spazio \\ dei \\ nomi TerminalServices CIMV2 radice, il livello di autenticazione \\ deve includere la privacy dei pacchetti. Per le chiamate C/C++, si tratta di un livello di autenticazione **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY,** che può essere impostato tramite la funzione COM [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Per Visual Basic chiamate di script e script, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

