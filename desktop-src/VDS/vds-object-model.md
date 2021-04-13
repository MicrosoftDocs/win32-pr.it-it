---
description: Modello a oggetti VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modello a oggetti VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234406"
---
# <a name="vds-object-model"></a>Modello a oggetti VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS consente l'accesso indiretto ai dispositivi di archiviazione basati su host, ad esempio i dischi e i dispositivi CD-ROM, e agli array di dischi gestiti da controller RAID hardware. Mentre alcune entità di archiviazione modellano i dispositivi fisici, altri costrutti virtuali del modello: volumi, partizioni e così via. Gli oggetti descritti in questo argomento rappresentano le entità fisiche e virtuali di VDS.

Le applicazioni chiamano i metodi esposti da tali oggetti e VDS chiama il provider appropriato per eseguire le operazioni di archiviazione richieste. Un'applicazione non chiama mai direttamente un programma provider.

### <a name="classification-of-objects"></a>Classificazione degli oggetti

Come illustrato nella figura seguente, i programmi del provider software implementano gli oggetti che modellano le entità basate su host. i programmi del provider hardware implementano oggetti che modellano dispositivi RAID hardware interni ed esterni; gli oggetti comuni rimanenti sono indipendenti dal provider o sono implementati da VDS. Un mandrino, che non è un oggetto VDS, è un termine per supporti di archiviazione generici che comprende gli extent del disco o dell'unità.

![Diagramma che mostra una classificazione di oggetti, definiti come "oggetti comuni", "oggetti provider software" e "oggetti provider hardware".](images/vdsobjectmodel.png)

Per ulteriori informazioni sul comportamento di ogni oggetto, selezionare uno degli argomenti seguenti:

-   Service Loader e oggetti servizio, vedere [Startup and Service Objects](startup-and-service-objects.md).
-   Enumerazione e oggetti asincroni, vedere [oggetti helper](helper-objects.md).
-   Oggetto provider, vedere [oggetto provider](provider-object.md).
-   Oggetti Pack, disco, volume e volume Plex, vedere [oggetti provider di software](software-provider-objects.md).
-   Oggetti Plex del sottosistema, controller, unità, LUN e LUN, vedere [oggetti provider hardware](hardware-provider-objects.md).

### <a name="object-creation"></a>Creazione di oggetti

Il completamento delle operazioni di configurazione e query associate alla creazione di oggetti può richiedere molto tempo. di conseguenza, VDS richiama tutti i metodi in modo asincrono. Il provider di individuazione restituisce tutti gli eventi di completamento, di errore o di modifica dello stato. I provider di software registrano inoltre tutti gli errori e le modifiche significative di stato.

### <a name="object-deletion"></a>Eliminazione oggetti

Diversi metodi VDS eliminano o trasformano oggetti VDS. Un chiamante può mantenere un riferimento, tramite un puntatore a interfaccia, a un oggetto eliminato dopo la restituzione del metodo. Quando il chiamante rilascia l'interfaccia, VDS Elimina l'oggetto.

Per quanto riguarda l'eliminazione di oggetti, i chiamanti devono evitare di richiamare qualsiasi elemento tranne il metodo [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su queste interfacce. Il provider deve essere sufficientemente solido per gestire i chiamanti errati; Se un chiamante richiama un metodo su un oggetto eliminato, il provider deve restituire l' **\_ oggetto VDS \_ E \_ eliminato**.

### <a name="service-initialization"></a>Inizializzazione del servizio

VDS fornisce un identificatore di classe (CLSID) per il caricatore del servizio e gli oggetti servizio, ma solo il CLSID del caricatore di servizi è pubblico. L'inizializzazione del servizio si verifica quando i provider, un'applicazione chiamante e il servizio eseguono le attività seguenti:

-   Ogni nuovo provider richiama il metodo [**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) durante l'installazione per la registrazione con VDS. La chiamata crea una chiave del registro di sistema nell'hive di sistema, identificata dal GUID oggetto del provider. Contenuto in questa chiave è il CLSID dell'oggetto provider, il nome, la versione e il GUID della versione del provider.
    > [!Note]  
    > I GUID oggetto provider sono permanenti; i GUID degli oggetti software e hardware non lo sono.

     

-   Un'applicazione chiama la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , passando il CLSID del caricatore del servizio come argomento. Con un puntatore all'oggetto del caricatore del servizio, l'applicazione può avviare VDS localmente o in remoto passando il nome del computer desiderato come parametro al metodo [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .
-   Quando l'applicazione iniziale si connette al servizio, VDS chiama prima [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) su ogni CLSID trovato sotto la chiave del registro di sistema e quindi chiama il metodo [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) su ogni provider per inizializzare i programmi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su VDS](about-vds.md)
</dt> <dt>

[**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
