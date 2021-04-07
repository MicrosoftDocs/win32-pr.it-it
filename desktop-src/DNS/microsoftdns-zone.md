---
title: Classe MicrosoftDNS_Zone
description: La \_ classe della zona MicrosoftDNS descrive una zona DNS. Ogni istanza della classe della \_ zona MicrosoftDNS deve essere assegnata esattamente a un server DNS. Le zone possono essere associate a più istanze di MicrosoftDNS \_ Domain o MicrosoftDNS \_ ResourceRecord.
ms.assetid: 9c59fa61-cca5-4718-ad40-8d2c6ed5fc2d
keywords:
- DNS della classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone della classe DNS, descritta
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
ms.openlocfilehash: b15119c7a5cdc1dba2998e17b5c69a4d0e15c6ca
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048862"
---
# <a name="microsoftdns_zone-class"></a>\_Classe della zona MicrosoftDNS

> [!NOTE]
> Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più. Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.

> [!NOTE]
> Questo articolo contiene riferimenti al termine server master, un termine che Microsoft non usa più. Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.

La classe della **\_ zona MicrosoftDNS** descrive una zona DNS. Ogni istanza della classe **della \_ zona MicrosoftDNS** deve essere assegnata esattamente a un server DNS. Le zone possono essere associate a più istanze di [**MicrosoftDNS \_ Domain**](microsoftdns-domain.md) o [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

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

La classe della **\_ zona MicrosoftDNS** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe della **\_ zona MicrosoftDNS** dispone di questi metodi.



| Metodo                   | Descrizione                                                                                                                                                                                                |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AgeAllRecords**        | Abilita la durata per alcuni o tutti i record non NS e non SOA.<br/>                                                                                                                                       |
| **ChangeZoneType**       | Modifica i tipi di zona. <br/> Qualificatori: implementato<br/>                                                                                                                                         |
| **CreateZone**           | Crea una nuova zona. <br/> Qualificatori: nessuno.<br/>                                                                                                                                               |
| **ForceRefresh**         | Impone un aggiornamento del database secondario dal server DNS master. <br/> Qualificatori: implementato<br/>                                                                                               |
| **Getdistinguishname** | Ottiene il nome distinto DS per la zona. <br/> Qualificatori: implementato<br/>                                                                                                                 |
| **PauseZone**            | Sospende la zona. <br/> Qualificatori: implementato<br/>                                                                                                                                            |
| **ReloadZone**           | Ricarica la zona. <br/> Qualificatori: implementato<br/>                                                                                                                                           |
| **ResetSecondaries**     | Reimposta la matrice di indirizzi IP secondaria. <br/> Qualificatori: implementato<br/>                                                                                                                      |
| **ResumeZone**           | Riprende la zona. <br/> Qualificatori: implementato<br/>                                                                                                                                           |
| **UpdateFromDS**         | Impone un aggiornamento della zona dal servizio directory (DS). Affinché questo metodo sia valido, il valore di ZoneType deve essere 0 perché la zona deve essere effettivamente archiviata nel servizio DS. <br/> Qualificatori: implementato<br/> |
| **WriteBackZone**        | Salva i dati della zona nel relativo file di zona. <br/> Qualificatori: implementata, statica<br/>                                                                                                                   |



 

### <a name="properties"></a>Proprietà

La classe della **\_ zona MicrosoftDNS** dispone di queste proprietà.

<dl> <dt>

**Invecchiamento**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il comportamento di invecchiamento e scavenging della zona. Zero indica che lo scavenging è disabilitato. Quando lo scavenging è disabilitato, i timestamp dei record della zona non vengono aggiornati e i record non sono soggetti a scavenging. Se impostata su uno, i record vengono sottoposti a scavenging e i relativi timestamp vengono aggiornati quando il server riceve la richiesta di aggiornamento dinamico per i record. Per le zone integrate Active Directory, questo valore viene impostato sulla proprietà *DefaultAgingState* del server DNS in cui viene creata la zona. Per le zone primarie standard, il valore predefinito è zero.

</dd> <dt>

**AllowUpdate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona accetta richieste di aggiornamento dinamico.

</dd> <dt>

**Creato automaticamente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona è stata creata in autocreazione.

</dd> <dt>

**AvailForScavengeTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'ora in cui il server può tentare di eseguire lo scavenging della zona. Anche se la zona è configurata per consentire lo scavenging, il server DNS non tenterà di eseguire lo scavenging di questa zona fino a dopo questo momento. Questo valore viene impostato sull'ora corrente più l'intervallo di aggiornamento della zona ogni volta che viene caricata la zona. Questo parametro viene archiviato localmente e non viene replicato in altre copie della zona.

</dd> <dt>

**DataFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il nome del file di zona.

</dd> <dt>

**DisableWINSRecordReplication**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il record WINS è replicato. Se impostato su TRUE, la replica del record WINS è disabilitata.

</dd> <dt>

**DsIntegrated**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se la zona è integrata in DS.

</dd> <dt>

**ForwarderSlave**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il DNS utilizza la ricorsione durante la risoluzione dei nomi per la zona di avanzamento specificata. Applicabile solo alle zone di inoltri condizionali.

</dd> <dt>

**ForwarderTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il tempo, in secondi, in cui un server DNS che esegue l'invio di una query per il nome sotto la zona di avanzamento attende la risoluzione dal server d'avvio prima di tentare di risolvere la query stessa. Questo parametro è applicabile solo alle zone di avanzamento.

</dd> <dt>

**LastSuccessfulSoaCheck**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di secondi a partire dall'inizio del 1 gennaio 1970 GMT, perché il numero di serie SOA per la zona è stato selezionato per l'ultima volta.

</dd> <dt>

**LastSuccessfulXfr**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di secondi a partire dall'inizio del 1 gennaio 1970 GMT, dall'ultimo trasferimento della zona da un server master.

</dd> <dt>

**LocalMasterServers**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzi IP locali dei server DNS master per questa zona. Se impostate, questi master superano il MasterServers trovato in Active Directory.

</dd> <dt>

**MasterServers**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzi IP dei server DNS master per questa zona.

</dd> <dt>

**NoRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'intervallo di tempo tra l'ultimo aggiornamento del timestamp di un record e il primo momento in cui è possibile aggiornare il timestamp.

</dd> <dt>

**Notificare**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona master notifica i database secondari di eventuali modifiche nel database RRs. Impostare su 1 per notificare i database secondari.

</dd> <dt>

**NotifyServers**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che enumerano gli indirizzi IP dei server DNS per ricevere una notifica delle modifiche in quest'area.

</dd> <dt>

**Sospeso**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona è sospesa.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'intervallo di aggiornamento, durante il quale si prevede che i record con un timestamp diverso da zero vengano aggiornati in modo che rimangano nella zona. I record che non sono stati aggiornati entro la scadenza dell'intervallo di aggiornamento potrebbero essere rimossi dal successivo scavenging eseguito da un server. Questo valore non deve mai essere inferiore al periodo di aggiornamento più lungo dei record registrati nella zona. I valori troppo piccoli possono causare la rimozione di record DNS validi. i valori troppo grandi prolungano la durata dei record non aggiornati. Questo valore viene impostato sulla proprietà *DefaultRefreshInterval-* del server DNS in cui viene creata la zona.

</dd> <dt>

**Inverso**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona è inversa (TRUE) o in poi (FALSE).

</dd> <dt>

**ScavengeServers**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che enumera l'elenco di indirizzi IP dei server DNS a cui è consentito eseguire lo scavenging dei record non aggiornati di questa zona. Se l'elenco non è specificato, il server DNS primario autorevole per la zona può eseguire lo scavenging della zona quando vengono soddisfatti altri prerequisiti.

</dd> <dt>

**SecondaryServers**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che enumerano gli indirizzi IP dei server DNS che possono ricevere questa zona tramite la replica della zona.

</dd> <dt>

**SecureSecondaries**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il trasferimento di zona può essere solo designato come secondari. I database secondari designati sono server DNS i cui indirizzi IP sono elencati in SecondariesIPAddressesArray.

</dd> <dt>

**Arresto**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la copia della zona è scaduta. Se TRUE, la zona è scaduta o è stata arrestata.

</dd> <dt>

**UseNBStat**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questo valore booleano indica se la zona usa la ricerca inversa NBStat.

</dd> <dt>

**UseWins**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la zona usa la ricerca di WINS.

</dd> <dt>

**ZoneType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il tipo della zona. I valori validi sono:

-   DS integrato
-   Primaria
-   Secondari

* * Windows Server 2003: * *

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
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dominio MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Metodo CreateZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Metodo PauseZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





