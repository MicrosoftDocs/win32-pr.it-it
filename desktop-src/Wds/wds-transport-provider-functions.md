---
title: Funzioni del provider di trasporto WDS
description: I provider di contenuti definiti dall'utente possono esporre le funzioni di callback seguenti al server multicast.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1044c923226dcc618e816219dcec9d7edf78855e03acf13b76ba4d7ed9ad15a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053259"
---
# <a name="wds-transport-provider-functions"></a>Funzioni del provider di trasporto WDS

I provider di contenuti definiti dall'utente possono esporre le funzioni di callback seguenti al server multicast.



| Funzione                                                                               | Descrizione                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*WdsTransportProviderCloseContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | Chiude un flusso di contenuto specificato da un handle.                                                                          |
| [*WdsTransportProviderCloseInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | Chiude un'istanza di un provider di contenuti specificato da un handle.                                                         |
| [*WdsTransportProviderCompareContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | Confronta un nome di contenuto e un'istanza specificati con un flusso di contenuto aperto per determinare se sono uguali.             |
| [*WdsTransportProviderCreateInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | Apre una nuova istanza di un provider di contenuti.                                                                             |
| [*WdsTransportProviderDumpState*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | Indica al provider di trasporto di stampare un riepilogo del relativo stato e qualsiasi altra informazione pertinente nel log di traccia. |
| [*WdsTransportProviderGetContentMetadata*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | Recupera i metadati per un flusso di contenuto aperto.                                                                          |
| [*WdsTransportProviderGetContentSize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | Recupera le dimensioni di un flusso di contenuto aperto.                                                                           |
| [*WdsTransportProviderInitialize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | Inizializza un provider di contenuti.                                                                                         |
| [*WdsTransportProviderOpenContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | Apre una nuova visualizzazione statica di un flusso di contenuto.                                                                            |
| [*WdsTransportProviderReadContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | Legge il contenuto da un flusso di contenuto aperto.                                                                              |
| [*WdsTransportProviderRefreshSettings*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | Indica al provider di trasporto di leggere nuovamente le impostazioni pertinenti.                                                       |
| [*WdsTransportProviderShutdown*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Arresta il provider di contenuti.                                                                                         |
| [*WdsTransportProviderUserAccessCheck*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | Specifica l'accesso a un flusso di contenuto in base al token di un utente.                                                           |



 

 

 




