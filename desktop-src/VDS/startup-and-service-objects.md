---
description: VDS fornisce oggetti per l'esecuzione di attività correlate al servizio. In questo argomento viene descritto ogni oggetto .
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Oggetti di avvio e di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a87c7e52a263d03e80f44911f72db5f49259baf33a7b2f90680f30bb3b2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125931"
---
# <a name="startup-and-service-objects"></a>Oggetti di avvio e di servizio

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

VDS fornisce oggetti per l'esecuzione di attività correlate al servizio. In questo argomento viene descritto ogni oggetto .

## <a name="service-loader-object"></a>Oggetto Service Loader

L'oggetto caricatore del servizio fornisce i metodi utilizzati dalle applicazioni per caricare e inizializzare VDS. Per preparare VDS per l'uso, un'applicazione deve eseguire le operazioni seguenti:

-   Creare un'istanza dell'oggetto caricatore del servizio, che restituisce [**l'interfaccia IVdsServiceLoader.**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader)
-   Chiamare il [**metodo IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) per caricare il servizio.

Per un esempio di codice, vedere [Caricamento di VDS.](loading-vds.md)

Consentire sempre l'inizializzazione completa del servizio prima di chiamare i metodi esposti dall'oggetto servizio. Usare il [**metodo IVdsService::IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) per determinare lo stato del processo di caricamento. Usare il [**metodo IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) per bloccare le chiamate agli oggetti VDS fino al completamento dell'inizializzazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.

| Tipo                                              | Elemento                                         |
|---------------------------------------------------|-------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Enumerazioni associate                           | Nessuno.                                           |
| Strutture associate                             | Nessuno.                                           |



 

## <a name="service-object"></a>Oggetto service

L'oggetto servizio è un oggetto multifunzione centrale per tutte le applicazioni VDS. Con questo oggetto, un chiamante può eseguire le operazioni seguenti:

-   Determinare lo stato dell'inizializzazione del servizio.
-   Recuperare tutti i provider hardware o software registrati con VDS.
-   Report sui dischi non allocati.
-   Restituisce il tipo file system e la lettera di unità associati ai volumi in un disco.
-   Rimuovere i percorsi in modalità utente inutilizzati e le cartelle montate dal Registro di sistema e aggiornare i dischi.
-   Ricevere notifiche VDS.
-   Riavviare l'host.
-   Recuperare Fibre Channel porte HBA o schede iniziatore iSCSI nel computer locale.
-   Preparare in modo sicuro i LUN esposti come dischi nel computer locale per la rimozione.

Le strutture di notifica VDS passano i GUID degli oggetti a tutte le applicazioni registrate con VDS per ricevere le notifiche. Usare il [**metodo IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) per convertire un GUID di oggetto in un puntatore a oggetto. Per una descrizione più completa del modello di notifica, vedere [Notifiche VDS.](vds-notification-model.md)

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                                                   | Elemento                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* , [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* , [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Interfacce sempre implementate ma non esposte alle applicazioni | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Enumerazioni associate                                                | [**VDS \_ FLAG \_ DEL PROVIDER DI \_ QUERY,**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)TIPO DI OGGETTO [**VDS, \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_object_type)FLAG DEL SERVIZIO [**VDS, \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_service_flag)FLAG DELLA LETTERA DI UNITÀ [**VDS, FLAG DEL FILE SYSTEM VDS, \_ \_ \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag)DELLA PROPRIETÀ DEL [**FILE \_ \_ SYSTEM \_ \_ VDS.**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag) [**\_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag)                                                      |
| Strutture associate                                                  | [**VDS \_ SERVICE \_ PROP,**](/windows/desktop/api/Vds/ns-vds-vds_service_prop) [**VDS \_ FILE SYSTEM \_ \_ PROP,**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop) [**VDS FILE SYSTEM TYPE PROP, VDS DRIVE LETTER \_ \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop) [**\_ \_ \_ NOTIFICATION, VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification)FILE SYSTEM [**\_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**VDS MOUNT POINT \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003: queste** interfacce non sono supportate fino a Windows Server 2003 R2.

## <a name="initiator-adapter-object"></a>Oggetto adapter dell'iniziatore

Un oggetto adattatore iniziatore modella un adattatore iniziatore iSCSI nel computer host del servizio VDS. Il servizio VDS può visualizzare solo le schede dell'iniziatore nel computer locale. Il ruolo di un oggetto adattatore iniziatore è quello di gestire le sessioni di accesso dal computer locale alle destinazioni iSCSI.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Enumerazioni associate                           | [**VDS \_ TIPO DI \_ \_ ACCESSO ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ \_ \_ FLAG DI ACCESSO ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), [**TIPO DI AUTENTICAZIONE \_ ISCSI \_ \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Strutture associate                             | [**VDS \_ ISCSI \_ INITIATOR \_ ADAPTER \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).                                                                                        |



 

**\* Windows Server 2003: questa** interfaccia non è supportata fino a Windows Server 2003 R2.

## <a name="initiator-portal-object"></a>Oggetto del portale dell'iniziatore

Un oggetto del portale iniziatore modella un portale iniziatore iSCSI in un iniziatore iSCSI. Un portale iniziatore è la combinazione di un indirizzo IP e di una porta tramite cui un computer host si connette a un portale in un sottosistema iSCSI. Il ruolo di un oggetto del portale dell'iniziatore è quello di fungere da endpoint di un percorso MPIO e di configurare le impostazioni di sicurezza IPSEC.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Enumerazioni associate                           | [**VDS \_ \_ \_ FLAG IPSEC ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Strutture associate                             | [**VDS \_ ISCSI \_ INITIATOR \_ PORTAL \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**VDS \_ ISCSI \_ IPSEC \_ KEY**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**VDS \_ IPADDRESS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003: questa** interfaccia non è supportata fino a Windows Server 2003 R2.

## <a name="hba-port-object"></a>Oggetto porta HBA

L'oggetto porta HBA modella una Fibre Channel della scheda bus host (HBA).

Usare il [**metodo IVdsServiceHba::QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) per determinare le porte HBA note a VDS nel computer locale.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.

| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Enumerazioni associate                           | [**VDS \_ HBAPORT \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**VDS \_ HBAPORT \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**VDS \_ HBAPORT \_ SPEED \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Strutture associate                             | [**VDS \_ HBAPORT \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003: questa** interfaccia non è supportata fino a Windows Server 2003 R2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Caricamento di VDS](loading-vds.md)
</dt> <dt>

[**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[Notifiche VDS](vds-notification-model.md)
</dt> </dl>

 

 
