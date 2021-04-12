---
title: Interfacce di virtualizzazione Desktop remoto
description: L'API di virtualizzazione Desktop remoto supporta le interfacce seguenti.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338279"
---
# <a name="remote-desktop-virtualization-interfaces"></a>Interfacce di virtualizzazione Desktop remoto

L'API di virtualizzazione Desktop remoto supporta le interfacce seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**ITsSbBaseNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

Espone metodi che segnalano messaggi di stato e di errore a Connessione Desktop remoto broker (gestore connessione Desktop remoto).

</dd> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

Espone i metodi e le proprietà che archiviano le informazioni sullo stato relative a una richiesta di connessione in ingresso da un client Connessione Desktop remoto (RDC).

</dd> <dt>

[**ITsSbClientConnectionPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

Può essere usato per definire le proprietà personalizzate di una connessione client nel modo appropriato.

</dd> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

Espone metodi e proprietà che contengono informazioni sull'ambiente che ospita il computer di destinazione. Questa interfaccia può essere utilizzata per archiviare le informazioni su un server fisico che ospita macchine virtuali.

</dd> <dt>

[**ITsSbEnvironmentPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

Può essere usato per definire le proprietà personalizzate di un ambiente che ospita i computer di destinazione in base alle esigenze.

</dd> <dt>

[**ITsSbFilterPluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

Filtra archivio plug-in

</dd> <dt>

[**ITsSbGenericNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

Espone metodi che segnalano il completamento di e ottiene il tempo di attesa dal gestore connessione Desktop remoto.

</dd> <dt>

[**ITsSbGlobalStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

Espone metodi che eseguono query per computer di destinazione, sessioni, ambienti e farm che sono stati aggiunti all'archivio gestore connessione Desktop remoto.

</dd> <dt>

[**ITsSbLoadBalanceResult**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

Espone metodi e proprietà che archiviano il nome di destinazione restituito da un algoritmo di bilanciamento del carico.

</dd> <dt>

[**ITsSbLoadBalancing**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

Espone metodi che è possibile usare per fornire un algoritmo di bilanciamento del carico personalizzato.

</dd> <dt>

[**ITsSbLoadBalancingNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

Espone metodi che restituiscono il risultato di un algoritmo di bilanciamento del carico a gestore connessione Desktop remoto.

</dd> <dt>

[**ITsSbOrchestration**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

Espone i metodi utilizzati da gestore connessione Desktop remoto per assicurarsi che la destinazione sia pronta prima di reindirizzare un client.

</dd> <dt>

[**ITsSbOrchestrationNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

Espone metodi che restituiscono un oggetto [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) al gestore connessione Desktop remoto dopo che la destinazione è stata preparata correttamente per una connessione.

</dd> <dt>

[**ITsSbPlacement**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

Espone metodi che preparano l'ambiente (il computer che ospita la macchina virtuale).

</dd> <dt>

[**ITsSbPlacementNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

Espone metodi che restituiscono informazioni sugli ambienti al gestore connessione Desktop remoto.

</dd> <dt>

[**ITsSbPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

Espone metodi che inizializzano e terminano plug-in.

</dd> <dt>

[**ITsSbPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

Espone metodi che notificano a gestore connessione Desktop remoto l'inizializzazione o la terminazione di un plug-in.

</dd> <dt>

[**ITsSbPluginPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

Può essere usato per definire le proprietà del plug-in personalizzato in base alle esigenze.

</dd> <dt>

[**ITsSbPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

Può essere usato per definire le proprietà personalizzate nel modo appropriato.

</dd> <dt>

[**ITsSbProvider**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

Espone metodi che creano implementazioni predefinite di oggetti utilizzati nella virtualizzazione Desktop remoto.

</dd> <dt>

[**ITsSbProvisioning**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

Espone metodi che creano e gestiscono macchine virtuali.

</dd> <dt>

[**ITsSbProvisioningPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

Espone metodi che notificano a gestore connessione Desktop remoto il provisioning delle macchine virtuali.

</dd> <dt>

[**ITsSbResourceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

Espone i metodi utilizzati da gestore connessione Desktop remoto per notificare i plug-in delle modifiche di stato che si verificano negli oggetti sessione, destinazione e connessione client.

</dd> <dt>

[**ITsSbResourceNotificationEx**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

Espone i metodi utilizzati da gestore connessione Desktop remoto per notificare i plug-in delle modifiche di stato che si verificano negli oggetti sessione, destinazione e connessione client.

</dd> <dt>

[**ITsSbResourcePlugin**](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

Espone metodi che estendono le funzionalità di gestore connessione Desktop remoto.

</dd> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni.

</dd> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> <dd>

Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni.

</dd> <dt>

[**ITsSbServiceNotification**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

Espone i metodi utilizzati da gestore connessione Desktop remoto per notificare i plug-in delle modifiche di stato che si verificano nel gestore connessione Desktop remoto stesso.

</dd> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

Espone le proprietà che archiviano le informazioni relative a una sessione utente.

</dd> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.

</dd> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dd>

Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.

</dd> <dt>

[**ITsSbTargetPropertySet**](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

Derivare da questa interfaccia per definire un set di proprietà di destinazione personalizzato.

</dd> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

Espone le proprietà utilizzate da Connessione Desktop remoto broker per impostare la coda di un plug-in.

</dd> <dt>

[**ITsSbTaskPlugin**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

Espone metodi che aggiornano la coda delle attività per i plug-in di Connessione Desktop remoto broker.

</dd> <dt>

[**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

Espone metodi che segnalano lo stato e i messaggi di errore relativi alle attività al gestore connessione Desktop remoto.

</dd> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

Utilizzato per estendere le funzionalità di gestore sessioni Servizi terminal. Implementare questa interfaccia quando si desidera fornire un plug-in che esegue l'override della logica di reindirizzamento di broker di sessione di Servizi terminal.

</dd> </dl>

 

 