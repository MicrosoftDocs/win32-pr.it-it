---
description: L'oggetto provider modella il programma responsabile della gestione dell'archiviazione.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Oggetto provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb36517f0091776b9429911212610134f31077a2
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566338"
---
# <a name="provider-object"></a>Oggetto provider

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

L'oggetto provider modella il programma responsabile della gestione dell'archiviazione. Questo oggetto consente di accedere alle funzionalità del provider software e del provider hardware. I programmi provider eseguono operazioni su dispositivi software (volumi e dischi) e dispositivi hardware (sottosistemi di archiviazione e matrici di unità dietro i controller RAID).

VDS registra un oggetto provider come oggetto COM nel registro di sistema di Windows e utilizza le interfacce contenute (non aggregate) per implementare gli oggetti rimanenti, eseguendo il wrapping di tutte le interfacce e dei metodi e aggiungendo le funzionalità in modo condizionale. Gli oggetti e le interfacce di cui è stato eseguito il wrapper dall'oggetto provider variano a seconda del tipo di provider.

Non è possibile creare un'istanza di un oggetto provider direttamente dall'applicazione. Al contrario, è necessario avviare VDS, ottenere un puntatore a un oggetto servizio e utilizzare l'oggetto servizio per eseguire una query per i provider noti all'host. Per istruzioni sul caricamento di VDS, vedere [Startup and Service Objects](startup-and-service-objects.md).

Usare il metodo [**IVdsService:: QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) per enumerare i programmi del provider registrati in un host. Il primo parametro del metodo consente di specificare solo provider di software, solo provider hardware o entrambi. Con un oggetto provider è possibile eseguire operazioni sugli oggetti gestiti dal provider. Come illustrato nella figura seguente, è possibile utilizzare i metodi esposti dall'interfaccia [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) per creare ed eseguire query su oggetti Pack associati a provider di software. Analogamente, è possibile utilizzare i metodi sull'interfaccia [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) per interagire con gli oggetti del sottosistema associati ai provider hardware.

![Diagramma che mostra la diramazione di un'applicazione in ' provider ',' Pack ' o ' Subsystem ' e quindi ' mandrini '.](images/vdsproviderobject.png)

Le proprietà dell'oggetto includono un identificatore di oggetto GUID persistente che rappresenta un provider specifico e un secondo GUID che rappresenta la versione del provider. Si noti che altri identificatori di oggetto nel modello a oggetti VDS sono non permanenti. Le proprietà rimanenti per questo oggetto includono un nome di provider, informazioni aggiuntive sulla versione, il software o l'hardware del tipo di provider, diversi flag e un'impostazione della priorità di ricompilazione che si applica solo ai provider di software.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate 

| Tipo                                                                                         | Elemento                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Interfacce sempre esposte solo da provider software                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Interfacce sempre esposte solo da provider hardware                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Interfacce che possono essere esposte da questo oggetto                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Interfacce che possono essere esposte solo da provider hardware                                    | [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype), [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows Server 2008, windows vista e Windows Server 2003:** l'interfaccia [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) non è supportata.<br/> |
| Interfacce sempre implementate ma non esposte alle applicazioni                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Interfacce sempre implementate da provider hardware ma non esposte ad applicazioni | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Interfacce che possono essere implementate da provider hardware ma non esposte ad applicazioni     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Enumerazioni associate                                                                      | [**VDS \_ \_Flag del provider**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag), [**\_ \_ \_ flag del provider di query VDS**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)e [**\_ \_ tipo di provider VDS**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Strutture associate                                                                        | Nessuna.                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[Oggetti Startup e Service](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

