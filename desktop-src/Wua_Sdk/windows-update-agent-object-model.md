---
description: I programmatori che usano Windows Update Agent (WUA) iniziano aggiungendo un riferimento a Wuapi.dll al progetto corrente (in Visual C++, Microsoft Visual Basic o C) o facendo riferimento a \# Wuapi.h e Wuguid.lib in un progetto C o C++.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Windows Aggiornare il modello a oggetti dell'agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b60f9306dfae5910418ddc07353a421e0325c0953fb1f47994ad007ded5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855447"
---
# <a name="windows-update-agent-object-model"></a>Windows Aggiornare il modello a oggetti dell'agente

I programmatori che usano Windows Update Agent (WUA) iniziano aggiungendo un riferimento a Wuapi.dll al progetto corrente (in Visual C++, Microsoft Visual Basic o C) o facendo riferimento a \# Wuapi.h e Wuguid.lib in un progetto C o C++. Il primo passaggio nell'uso dell'API WUA consiste nel creare un'istanza di una delle interfacce creando un oggetto dalla coclasse appropriata.

Nella figura seguente viene descritto il modello a oggetti WUA. Per altre informazioni, vedere la sezione["Oggetti WUA e attività associate".](#wua-objects-and-associated-tasks) Per un elenco completo di tutte le interfacce WUA, vedere [Interfacce](interfaces.md).

![modello a oggetti dell'agente di Windows Update](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>Oggetti WUA e attività associate

Nella tabella seguente sono elencati gli oggetti WUA e le attività tipiche associate agli oggetti WUA.



| Oggetto                                                                | Descrizione                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Avviare, sospendere o riprendere Aggiornamenti automatici.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Recuperare o impostare il giorno e l'ora di installazione degli aggiornamenti. Specificare la modalità di notifica di un evento Aggiornamenti automatici utenti.                                                                                                                          |
| [**Category**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Recuperare informazioni sulla categoria dell'aggiornamento, inclusi il nome, l'ID, la descrizione, il proprietario e il prodotto previsto. Recupera una raccolta di aggiornamenti appartenenti a questa categoria. Recupera una raccolta delle categorie padre o figlio. |
| [**CategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Accedere a una raccolta di oggetti Category.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Recuperare informazioni sul risultato di un download.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Recuperare informazioni sul risultato di un'installazione o di una disinstallazione. Determinare se è necessario un riavvio del sistema per completare l'installazione o la disinstallazione.                                                                  |
| [**Searchresult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Recuperare informazioni sul risultato di una ricerca di categorie o aggiornamenti. Recuperare una raccolta di categorie trovate nel computer di destinazione dalla ricerca. Recuperare una raccolta di aggiornamenti trovati dalla ricerca.                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Recuperare informazioni sui requisiti di riavvio del sistema e hardware OEM nel computer di destinazione.                                                                                                                                        |
| [**Aggiornamento**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Recuperare la maggior parte delle informazioni sull'aggiornamento, inclusi gli aggiornamenti in bundle, i requisiti di origine, l'identità, la descrizione, le opzioni di disinstallazione, la priorità di download, le dimensioni e la scadenza.                                                                |
| [**UpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Accedere a una raccolta di oggetti Update.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Avviare un download asincrono o sincrono dei file associati agli aggiornamenti.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Recuperare informazioni sul risultato del download per un aggiornamento.                                                                                                                                                                       |
| [**Updateexception**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Recuperare la descrizione e il contesto di un'eccezione generata quando si verifica un errore di aggiornamento.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Accedere a una raccolta di oggetti UpdateException.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Recuperare informazioni su un aggiornamento che è stato installato o disinstallato, inclusi l'applicazione elaborata, la data e la descrizione.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Accedere a una raccolta di oggetti UpdateHistoryEntry.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Recuperare informazioni sul risultato dell'installazione o della disinstallazione di un aggiornamento.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Avviare un'installazione o una disinstallazione asincrona o sincrona di un aggiornamento. Avviare una sequenza di finestre di dialogo interattive per guidare l'utente nella procedura di installazione degli aggiornamenti.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Cerca gli aggiornamenti nel server in base a criteri quali il tipo di aggiornamento, l'ID o la categoria.                                                                                                                                            |
| [**Sessione di aggiornamento**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Avviare una sessione per cercare, scaricare, installare o disinstallare gli aggiornamenti per un'applicazione.                                                                                                                                                  |
| [**Webproxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Recuperare e impostare le impostazioni del proxy HTTP.                                                                                                                                                                                                       |



 

 

 



