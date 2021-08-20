---
title: MicrosoftDNS_Zone classe
description: La classe Zona MicrosoftDNS \_ descrive una zona DNS. Ogni istanza della classe Zona MicrosoftDNS \_ deve essere assegnata esattamente a un server DNS. Le zone possono essere associate a più istanze delle classi MicrosoftDNS \_ Domain o \_ MicrosoftDNS ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- MicrosoftDNS_Zone DNS della classe
- MicrosoftDNS_Zone classe DNS , descritto
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone
- MicrosoftDNS_Zone.PauseZone
- MicrosoftDNS_Zone.ResumeZone
- MicrosoftDNS_Zone.ReloadZone
- MicrosoftDNS_Zone.ForceRefresh
- MicrosoftDNS_Zone.UpdateFromDS
- MicrosoftDNS_Zone.WriteBackZone
- MicrosoftDNS_Zone.AgeAllRecords
- MicrosoftDNS_Zone.CreateZone
- MicrosoftDNS_Zone.ChangeZoneType
- MicrosoftDNS_Zone.ResetSecondaries
- MicrosoftDNS_Zone.GetDistinguishedName
- MicrosoftDNS_Zone.ZoneType
- MicrosoftDNS_Zone.DsIntegrated
- MicrosoftDNS_Zone.AllowUpdate
- MicrosoftDNS_Zone.DataFile
- MicrosoftDNS_Zone.DisableWINSRecordReplication
- MicrosoftDNS_Zone.Notify
- MicrosoftDNS_Zone.SecureSecondaries
- MicrosoftDNS_Zone.Paused
- MicrosoftDNS_Zone.Shutdown
- MicrosoftDNS_Zone.Reverse
- MicrosoftDNS_Zone.AutoCreated
- MicrosoftDNS_Zone.UseWins
- MicrosoftDNS_Zone.UseNBStat
- MicrosoftDNS_Zone.Aging
- MicrosoftDNS_Zone.RefreshInterval
- MicrosoftDNS_Zone.NoRefreshInterval
- MicrosoftDNS_Zone.AvailForScavengeTime
- MicrosoftDNS_Zone.MasterServers
- MicrosoftDNS_Zone.LocalMasterServers
- MicrosoftDNS_Zone.ScavengeServers
- MicrosoftDNS_Zone.SecondaryServers
- MicrosoftDNS_Zone.NotifyServers
- MicrosoftDNS_Zone.ForwarderTimeout
- MicrosoftDNS_Zone.ForwarderSlave
- MicrosoftDNS_Zone.LastSuccessfulSoaCheck
- MicrosoftDNS_Zone.LastSuccessfulXfr
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37b8c99fcd0fb70206758dd67dab8cfffe145ea2ef1aa75186b1268a7ff3b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957180"
---
# <a name="microsoftdns_zone-class"></a>Classe Zona \_ MicrosoftDNS

> [!NOTE]
> Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più. Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.

> [!NOTE]
> Questo articolo contiene riferimenti al termine server master, un termine che Microsoft non usa più. Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.

La **classe \_ Zona MicrosoftDNS** descrive una zona DNS. Ogni istanza della **classe \_ Zona MicrosoftDNS** deve essere assegnata esattamente a un server DNS. Le zone possono essere associate a più istanze [**delle classi MicrosoftDNS \_ Domain o**](microsoftdns-domain.md) [**MicrosoftDNS \_ ResourceRecord.**](microsoftdns-resourcerecord.md)

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MicrosoftDNS_Zone : MicrosoftDNS_Domain
{
  uint32  ZoneType;
  boolean DsIntegrated;
  uint32  AllowUpdate;
  string  DataFile;
  boolean DisableWINSRecordReplication;
  uint32  Notify;
  uint32  SecureSecondaries;
  boolean Paused;
  boolean Shutdown;
  boolean Reverse;
  boolean AutoCreated;
  boolean UseWins;
  boolean UseNBStat;
  boolean Aging;
  uint32  RefreshInterval;
  uint32  NoRefreshInterval;
  uint32  AvailForScavengeTime;
  string  MasterServers[];
  string  LocalMasterServers[];
  string  ScavengeServers[];
  string  SecondaryServers[];
  string  NotifyServers[];
  uint32  ForwarderTimeout;
  boolean ForwarderSlave;
  uint32  LastSuccessfulSoaCheck;
  uint32  LastSuccessfulXfr;
};
```

## <a name="members"></a>Members

La **classe \_ Zona MicrosoftDNS** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Zona MicrosoftDNS** include questi metodi.



| Metodo                   | Descrizione                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Abilita l'aging per alcuni o tutti i record non NS e non SOA.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Modifica i tipi di zona. <br/> Qualificatori: implementati<br/>                                                                                                                                         |
| **CreateZone**           | Crea una nuova zona. <br/> Qualificatori: nessuno.<br/>                                                                                                                                               |
| **ForceRefresh**         | Forza un aggiornamento del database secondario dal server DNS master. <br/> Qualificatori: implementati<br/>                                                                                               |
| **GetDistinguishedName** | Ottiene il nome distinto DS per la zona. <br/> Qualificatori: implementati<br/>                                                                                                                 |
| **PauseZone**            | Sospende la zona. <br/> Qualificatori: implementati<br/>                                                                                                                                            |
| **ReloadZone**           | Ricarica la zona. <br/> Qualificatori: implementati<br/>                                                                                                                                           |
| **ResetSecondaries**     | Reimposta la matrice di indirizzi IP secondari. <br/> Qualificatori: implementati<br/>                                                                                                                      |
| **ResumeZone**           | Riprende la zona. <br/> Qualificatori: implementati<br/>                                                                                                                                           |
| **UpdateFromDS**         | Forza un aggiornamento della zona dal servizio directory( DS). Per la validità di questo metodo, ZoneType deve essere 0. La zona deve essere effettivamente archiviata nel DS. <br/> Qualificatori: implementati<br/> |
| **WriteBackZone**        | Salva i dati della zona nel file di zona. <br/> Qualificatori: implementati, statici<br/>                                                                                                                   |



 

### <a name="properties"></a>Proprietà

La **classe \_ Zona MicrosoftDNS** ha queste proprietà.

<dl> <dt>

**Invecchiamento**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il comportamento di aging e scavenging della zona. Zero indica che lo scavenging è disabilitato. Quando lo scavenging è disabilitato, i timestamp dei record nella zona non vengono aggiornati e i record non sono soggetti a scavenging. Se impostato su uno, i record vengono sottoposti a scavenging e i relativi timestamp vengono aggiornati quando il server riceve la richiesta di aggiornamento dinamico per i record. Per le zone integrate in Active Directory, questo valore è impostato sulla *proprietà DefaultAgingState* del server DNS in cui viene creata la zona. Per le zone primarie standard, il valore predefinito è zero.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona accetta richieste di aggiornamento dinamico.

</dd> <dt>

**Creazione automatica**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona viene create automaticamente.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'ora in cui il server può tentare di eseguire lo scavenging della zona. Anche se la zona è configurata per abilitare lo scavenging del server DNS, non tenterà di eseguire lo scavenging di questa zona fino a dopo questo momento. Questo valore è impostato sull'ora corrente più l'intervallo di aggiornamento della zona ogni volta che la zona viene caricata. Questo parametro viene archiviato in locale e non viene replicato in altre copie della zona.

</dd> <dt>

**Datafile**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il nome del file di zona.

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il record WINS viene replicato. Se impostato su TRUE, la replica dei record WINS è disabilitata.

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se la zona è integrata con DS.

</dd> <dt>

**ForwarderSlave**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il DNS usa la ricorsione durante la risoluzione dei nomi per la zona di inoltro specificata. Applicabile solo alle zone di inoltro condizionale.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il tempo, in secondi, in cui un server DNS che inoltra una query per il nome nella zona di inoltro attende la risoluzione dal server d'inoltro prima di tentare di risolvere la query stessa. Questo parametro è applicabile solo alle zone di inoltro.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di secondi dall'inizio del 1° gennaio 1970 GMT, dall'ultima verifica del numero di serie SOA per la zona.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di secondi dall'inizio del 1° gennaio 1970 GMT, dall'ultimo trasferimento della zona da un server master.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzi IP locali dei server DNS master per questa zona. Se impostato, questi master estraeno i MasterServer trovati in Active Directory.

</dd> <dt>

**Masterservers**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzi IP dei server DNS master per questa zona.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'intervallo di tempo tra l'ultimo aggiornamento del timestamp di un record e il momento meno recente in cui il timestamp può essere aggiornato.

</dd> <dt>

**Notificare**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona master invia una notifica ai database secondari di eventuali modifiche nel relativo database di richieste di ripristino. Impostare su 1 per inviare notifiche ai database secondari.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che enumerano gli indirizzi IP dei server DNS a cui notificare le modifiche in questa zona.

</dd> <dt>

**Sospeso**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona è sospesa.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'intervallo di aggiornamento durante il quale si prevede che i record con timestamp diverso da zero siano aggiornati per rimanere nella zona. I record che non sono stati aggiornati alla scadenza dell'intervallo di aggiornamento potrebbero essere rimossi al successivo scavenging eseguito da un server. Questo valore non deve mai essere inferiore al periodo di aggiornamento più lungo dei record registrati nella zona. I valori troppo piccoli possono causare la rimozione di record DNS validi. I valori troppo grandi prolungano la durata dei record non aggiornati. Questo valore è impostato sulla *proprietà DefaultRefreshInterval* del server DNS in cui viene creata la zona.

</dd> <dt>

**Reverse**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona è inversa (TRUE) o in avanti (FALSE).

</dd> <dt>

**ScavengeServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che enumera l'elenco di indirizzi IP dei server DNS autorizzati a eseguire lo scavenging dei record non aggiornati di questa zona. Se l'elenco non è specificato, qualsiasi server DNS primario autorevole per la zona può eseguire lo scavenge della zona quando vengono soddisfatti altri prerequisiti.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che enumerano gli indirizzi IP dei server DNS autorizzati a ricevere questa zona tramite la replica di zona.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il trasferimento di zona è consentito solo ai database secondari designati. I database secondari designati sono server DNS i cui indirizzi IP sono elencati in SecondariesIPAddressesArray.

</dd> <dt>

**Arresto**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la copia della zona è scaduta. Se TRUE, la zona è scaduta o è stata arrestata.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questo valore booleano indica se la zona usa la ricerca inversa NBStat.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona utilizza la ricerca WINS.

</dd> <dt>

**Tipo di zona**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il tipo della zona. I valori validi sono:

-   Integrazione di DS
-   Primaria
-   Secondari

**Windows Server 2003: **

Valori aggiuntivi:

-   Cache
-   Stub
-   Server d'inoltro

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dominio \_ MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Metodo AgeAllRecords della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Metodo ChangeZoneType della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Metodo CreateZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Metodo ForceRefresh della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Metodo PauseZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Metodo ReloadZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Metodo ResetSecondaries della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Metodo ResumeZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Metodo UpdateFromDS della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Metodo WriteBackZone della classe Zone \_ MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





