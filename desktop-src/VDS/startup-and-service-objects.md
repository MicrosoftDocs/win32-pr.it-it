---
description: VDS fornisce oggetti per l'esecuzione di attività relative ai servizi. In questo argomento vengono descritti i singoli oggetti.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Oggetti Startup e Service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92beb0a4f825f767299a7ced74d43ef2487fa252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318595"
---
# <a name="startup-and-service-objects"></a>Oggetti Startup e Service

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS fornisce oggetti per l'esecuzione di attività relative ai servizi. In questo argomento vengono descritti i singoli oggetti.

## <a name="service-loader-object"></a>Oggetto caricatore servizio

L'oggetto caricatore del servizio fornisce i metodi usati dalle applicazioni per caricare e inizializzare VDS. Per preparare VDS per l'utilizzo, un'applicazione deve eseguire le operazioni seguenti:

-   Creare un'istanza dell'oggetto del caricatore di servizi, che restituisce l'interfaccia [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) .
-   Chiamare il metodo [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) per caricare il servizio.

Per un esempio di codice, vedere [caricamento di VDS](loading-vds.md).

Consentire sempre il completamento dell'inizializzazione del servizio prima di chiamare i metodi esposti dall'oggetto servizio. Usare il metodo [**IVdsService:: IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) per determinare lo stato del processo di caricamento. Usare il metodo [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) per bloccare le chiamate agli oggetti VDS fino al completamento dell'inizializzazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.

| Tipo                                              | Elemento                                         |
|---------------------------------------------------|-------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Enumerazioni associate                           | Nessuna.                                           |
| Strutture associate                             | Nessuna.                                           |



 

## <a name="service-object"></a>Oggetto servizio

L'oggetto servizio è un oggetto multifunzione che è fondamentale per tutte le applicazioni VDS. Con questo oggetto, un chiamante può eseguire le operazioni seguenti:

-   Determinare lo stato dell'inizializzazione del servizio.
-   Recuperare tutti i provider hardware o software registrati con VDS.
-   Report sui dischi non allocati.
-   Restituisce il tipo file system e la lettera di unità associata ai volumi su un disco.
-   Rimuovere i percorsi in modalità utente non usati e le cartelle montate dal registro di sistema e aggiornare i dischi.
-   Ricevere le notifiche VDS.
-   Riavviare l'host.
-   Recuperare Fibre Channel porte HBA o schede iniziatore iSCSI nel computer locale.
-   Preparare in modo sicuro i LUN esposti come dischi nel computer locale per la rimozione.

Le strutture di notifica VDS passano i GUID oggetto a tutte le applicazioni registrate con VDS per ricevere le notifiche. Usare il metodo [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) per convertire il GUID di un oggetto in un puntatore a un oggetto. Per una descrizione più completa del modello di notifica, vedere [notifiche VDS](vds-notification-model.md).

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                                                   | Elemento                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* , [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* , [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Interfacce sempre implementate ma non esposte alle applicazioni | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Enumerazioni associate                                                | [**VDS \_ \_ \_ flag del provider di query**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag), [**\_ \_ tipo di oggetto VDS**](/windows/desktop/api/Vds/ne-vds-vds_object_type), [**\_ \_ flag del servizio VDS**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), [**\_ \_ \_ flag della lettera di unità VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), [**\_ \_ \_ flag del file System VDS**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag), flag [**\_ prop del file \_ System \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).                                                      |
| Strutture associate                                                  | [**VDS \_ \_prop del servizio**](/windows/desktop/api/Vds/ns-vds-vds_service_prop), [**\_ prop del file \_ \_ System VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), [**\_ tipo di file \_ System \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), notifica della [**\_ \_ lettera \_ di unità VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), [**\_ notifica del file \_ System \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**\_ \_ \_ notifica del punto di montaggio VDS**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003:** queste interfacce non sono supportate fino a Windows Server 2003 R2.

## <a name="initiator-adapter-object"></a>Oggetto adapter initiator

Un oggetto adapter initiator modella un adapter iniziatore iSCSI nel computer host del servizio VDS. Il servizio VDS può visualizzare solo gli adapter Initiator nel computer locale. Il ruolo di un oggetto adapter Initiator è la gestione delle sessioni di accesso dal computer locale alle destinazioni iSCSI.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Enumerazioni associate                           | [**VDS \_ \_ \_ tipo di accesso iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ \_ \_ flag di accesso iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), [**\_ \_ \_ tipo di autenticazione iSCSI VDS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Strutture associate                             | [**VDS \_ \_prop dell' \_ adapter \_ dell'iniziatore iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).                                                                                        |



 

**\* Windows Server 2003:** questa interfaccia non è supportata fino a Windows Server 2003 R2.

## <a name="initiator-portal-object"></a>Oggetto portale initiator

Un oggetto portale initiator modella un portale dell'iniziatore iSCSI in un iniziatore iSCSI. Un portale iniziatore è la combinazione di un indirizzo IP e di una porta attraverso cui un computer host si connette a un portale in un sottosistema iSCSI. Il ruolo di un oggetto portale initiator consiste nel fungere da endpoint di un percorso MPIO e configurare le impostazioni di sicurezza IPSEC.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Enumerazioni associate                           | [**VDS \_ \_ \_ flag IPSec iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Strutture associate                             | [**VDS \_ \_prop del \_ portale \_ dell'iniziatore iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**\_ \_ \_ chiave IPsec iSCSI VDS**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**\_ IP VDS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003:** questa interfaccia non è supportata fino a Windows Server 2003 R2.

## <a name="hba-port-object"></a>Oggetto porta HBA

L'oggetto porta HBA modella una porta Fibre Channel scheda bus host (HBA).

Usare il metodo [**IVdsServiceHba:: QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) per determinare le porte HBA note a VDS nel computer locale.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.

| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Enumerazioni associate                           | [**VDS \_ HBAPORT \_ Type**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**VDS \_ HBAPORT \_ status**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**VDS \_ HBAPORT \_ Speed \_ flag**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Strutture associate                             | [**VDS \_ HBAPORT \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003:** questa interfaccia non è supportata fino a Windows Server 2003 R2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Caricamento di VDS](loading-vds.md)
</dt> <dt>

[**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[Notifiche VDS](vds-notification-model.md)
</dt> </dl>

 

 
