---
description: Il provider a oggetti modella il programma responsabile della gestione dell'archiviazione.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Oggetto provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb64d879b8213970edd5887c2d7a217c434ec38a113d2c9f36cd9e1d73e564d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999467"
---
# <a name="provider-object"></a>Oggetto provider

\[A partire da Windows 8 e Windows Server 2012, [l'interfaccia](virtual-disk-service-portal.md) COM del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Il provider a oggetti modella il programma responsabile della gestione dell'archiviazione. Questo oggetto fornisce l'accesso alle funzionalità del provider software e del provider di hardware. I programmi provider eseguono operazioni su dispositivi software (volumi e dischi) e dispositivi hardware (sottosistemi di archiviazione e array di unità dietro i controller RAID).

VDS registra un oggetto provider come oggetto COM nel Registro di sistema di Windows e usa interfacce contenute (non aggregazione) per implementare gli oggetti rimanenti, il wrapping di tutte le interfacce e i metodi e l'aggiunta condizionale di funzionalità. Gli oggetti e le interfacce di cui viene eseguito il wrapping dall'oggetto provider variano a seconda del tipo di provider.

Non è possibile creare un'istanza di un oggetto provider direttamente dall'applicazione. È invece necessario avviare VDS, ottenere un puntatore a un oggetto servizio e usare l'oggetto servizio per eseguire query per i provider noti all'host. Per istruzioni sul caricamento di VDS, vedere [Oggetti di avvio e di servizio](startup-and-service-objects.md).

Usare il [**metodo IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) per enumerare i programmi provider registrati in un host. Il primo parametro del metodo consente di specificare solo i provider software, solo i provider di hardware o entrambi. Con un oggetto provider è possibile eseguire operazioni sugli oggetti gestiti da tale provider. Come illustrato nella figura seguente, è possibile usare i metodi esposti [**dall'interfaccia IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) per creare ed eseguire query sugli oggetti del pacchetto associati ai provider software. Analogamente, è possibile usare i metodi [**nell'interfaccia IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) per interagire con gli oggetti del sottosistema associati ai provider di hardware.

![Diagramma che mostra un'applicazione che si dirama in 'Providers', quindi 'Pack' o 'Subsystem' e quindi 'Spindles'.](images/vdsproviderobject.png)

Le proprietà dell'oggetto includono un identificatore di oggetto GUID permanente che rappresenta un provider specifico e un secondo GUID che rappresenta la versione del provider. Si noti che gli altri identificatori di oggetto nel modello a oggetti VDS non sono persistenti. Le proprietà rimanenti per questo oggetto includono un nome del provider, informazioni aggiuntive sulla versione, il software o l'hardware del tipo di provider, vari flag e un'impostazione di priorità di ricompilazione che si applica solo ai provider software.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate 

| Tipo                                                                                         | Elemento                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Interfacce sempre esposte solo dai provider di software                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Interfacce sempre esposte solo dai provider di hardware                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Interfacce che possono essere esposte da questo oggetto                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Interfacce che possono essere esposte solo dai provider di hardware                                    | [**IVdsHwProviderType,**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype) [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows Server 2008, Windows Vista e Windows Server 2003:** l'interfaccia [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) non è supportata.<br/> |
| Interfacce sempre implementate ma non esposte alle applicazioni                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Interfacce sempre implementate dai provider di hardware ma non esposte alle applicazioni | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Interfacce che possono essere implementate dai provider di hardware ma non esposte alle applicazioni     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Enumerazioni associate                                                                      | [**VDS \_ PROVIDER \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag), [**FLAG DEL \_ \_ \_ PROVIDER DI QUERY VDS**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)E TIPO DI [**PROVIDER VDS \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Strutture associate                                                                        | Nessuno.                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[Oggetti di avvio e di servizio](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

