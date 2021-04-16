---
description: I programmatori che usano Windows Update Agent (WUA) iniziano con l'aggiunta di un riferimento a Wuapi.dll al progetto corrente (in Visual C++, Microsoft Visual Basic o C \# ) o facendo riferimento a wuapi. h e Wuguid. lib in un progetto C o C++.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Modello a oggetti di Windows Update Agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5060a76c850ea9ad97e9132f661d4b64f4f4fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550612"
---
# <a name="windows-update-agent-object-model"></a>Modello a oggetti di Windows Update Agent

I programmatori che usano Windows Update Agent (WUA) iniziano con l'aggiunta di un riferimento a Wuapi.dll al progetto corrente (in Visual C++, Microsoft Visual Basic o C \# ) o facendo riferimento a wuapi. h e Wuguid. lib in un progetto C o C++. Il primo passaggio nell'uso dell'API WUA consiste nel creare un'istanza di una delle interfacce creando un oggetto dalla coclasse appropriata.

Nella figura seguente viene descritto il modello a oggetti WUA. Per ulteriori informazioni, vedere la sezione "[oggetti WUA e attività associate](#wua-objects-and-associated-tasks)". Per un elenco completo di tutte le interfacce WUA, vedere [interfacce](interfaces.md).

![modello a oggetti dell'agente di Windows Update](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>Oggetti WUA e attività associate

Nella tabella seguente sono elencati gli oggetti WUA e le attività tipiche associate agli oggetti WUA.



| Oggetto                                                                | Descrizione                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Avviare, sospendere o riprendere Aggiornamenti automatici.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Recuperare o impostare il giorno e l'ora in cui installare gli aggiornamenti. Consente di specificare la modalità di notifica agli utenti di un evento Aggiornamenti automatici.                                                                                                                          |
| [**Category**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Recuperare le informazioni sulla categoria dell'aggiornamento, inclusi il nome, l'ID, la descrizione, il proprietario e il prodotto designato. Recuperare una raccolta di aggiornamenti appartenenti a questa categoria. Recuperare una raccolta delle categorie padre o figlio. |
| [**Metodo CategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Accedere a una raccolta di oggetti Category.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Recuperare informazioni sul risultato di un download.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Recuperare informazioni sul risultato di un'installazione o di una disinstallazione. Determinare se è necessario riavviare il sistema per completare l'installazione o la disinstallazione.                                                                  |
| [**SearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Recuperare informazioni sul risultato di una ricerca di categorie o aggiornamenti. Recuperare dalla ricerca una raccolta di categorie trovate nel computer di destinazione. Recupera una raccolta di aggiornamenti trovati dalla ricerca.                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Recuperare informazioni sui requisiti hardware e di riavvio del sistema OEM nel computer di destinazione.                                                                                                                                        |
| [**Aggiornamento**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Recuperare la maggior parte delle informazioni sull'aggiornamento, inclusi gli aggiornamenti in bundle, i requisiti di origine, l'identità, la descrizione, le opzioni di disinstallazione, priorità di download, dimensioni e scadenza.                                                                |
| [**Updatecollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Accedere a una raccolta di oggetti Update.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Avviare un download asincrono o sincrono dei file associati agli aggiornamenti.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Recuperare informazioni sul risultato del download per un aggiornamento.                                                                                                                                                                       |
| [**UpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Recuperare la descrizione e il contesto di un'eccezione generata quando si verifica un errore di aggiornamento.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Accedere a una raccolta di oggetti UpdateException.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Recuperare le informazioni su un aggiornamento che è stato installato o disinstallato, incluse l'applicazione, la data e la descrizione elaborate.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Accedere a una raccolta di oggetti UpdateHistoryEntry.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Recuperare informazioni sul risultato dell'installazione o sulla disinstallazione di un aggiornamento.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Avvia un'installazione asincrona o sincrona o la disinstallazione di un aggiornamento. Avviare una sequenza di dialogo interattiva per guidare l'utente nella procedura di installazione degli aggiornamenti.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Cerca gli aggiornamenti sul server in base a criteri quali il tipo di aggiornamento, l'ID o la categoria.                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Avviare una sessione per cercare, scaricare, installare o disinstallare gli aggiornamenti per un'applicazione.                                                                                                                                                  |
| [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Recuperare e impostare le impostazioni del proxy HTTP.                                                                                                                                                                                                       |



 

 

 



