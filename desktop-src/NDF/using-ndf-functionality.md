---
title: Uso della funzionalità NDF
description: Microsoft fornisce l'accesso alla funzionalità NDF tramite un'API pubblica. Quando si verifica un problema, l'applicazione può usare questa API per sfruttare questa funzionalità nel contesto di un'applicazione specifica.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85d1386971207330579f5395989e14c4b2315dc578f5bb3509695b99d6e215a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133228"
---
# <a name="using-ndf-functionality"></a>Uso della funzionalità NDF

Microsoft fornisce l'accesso alla funzionalità NDF tramite un'API pubblica. Quando si verifica un problema, l'applicazione può usare questa API per sfruttare questa funzionalità nel contesto di un'applicazione specifica.

Esistono tre fasi di esecuzione della diagnosi con la funzione definita dall'utente: creazione di un evento imprevisto, esecuzione di diagnosi e riparazione e chiusura dell'evento imprevisto. Questa panoramica indica quali funzioni NDF possono essere rilevanti per uno scenario specifico. Informazioni dettagliate su ogni funzione sono disponibili nella sezione [NDF Reference (Riferimento NDF).](ndf-reference.md)

## <a name="creating-an-incident"></a>Creazione di un evento imprevisto

Una sessione di diagnostica NDF richiede un evento imprevisto specifico per la diagnosi. Esistono diverse funzioni che possono essere usate per creare un evento imprevisto. Scegliere la funzione più simile a quella che l'applicazione stava tentando di eseguire quando si è verificato l'errore.

-   [**NdfCreateConnectivityIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)problemi generali di connettività Internet che non necessitano di informazioni aggiuntive.
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**NdfCreateWebIncidentEx:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)connessione a un URL HTTP o HTTPS.
-   [**NdfCreateSharingIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)accesso a un percorso UNC o a una condivisione file.
-   [**NdfCreateDNSIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)risoluzione di un nome host DNS.
-   [**NdfCreatePnrpIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)risoluzione di un nome peer PNRP.
-   [**NdfCreateGroupingIncident: aggiunta**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)a un gruppo peer-to-peer.
-   [**NdfCreateWinSockIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)connessione a una destinazione tramite un socket (quando nessuna delle altre funzioni è applicabile in modo specifico).
-   [**NdfCreateIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)usato quando nessun altro scenario è appropriato e la classe helper NDF specifica da richiamare è nota (insieme agli argomenti necessari). Usato principalmente a scopo di test dagli sviluppatori di applicazioni che hanno scritto la propria classe helper.

## <a name="running-diagnosis-and-repairs"></a>Esecuzione di diagnosi e riparazione

Esistono due modi per avviare la funzionalità di diagnosi e ripristino.

-   Uso del Windows Interfaccia utente (scelta consigliata)

    Quando si esegue nell'Windows utente standard, è possibile chiamare semplicemente la [**funzione NdfExecuteDiagnosis.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) La procedura guidata NDF avvierà e assisterà l'utente nell'identificazione (e, se possibile, nella risoluzione) del problema. La funzione restituirà al termine del processo. L'interfaccia utente è facoltativamente modale per l'applicazione.

-   Uso di un Interfaccia utente personalizzato (Windows solo 7 e versioni successive)

    Sono disponibili funzioni diverse da usare negli scenari in cui non viene visualizzata alcuna interfaccia utente o in cui non viene usata l'esperienza Windows standard (ad esempio, Media Center, applicazioni incorporate e il prompt dei comandi). Questa opzione ignora la funzionalità dell'esperienza utente fornita nella procedura guidata NDF, che include la limitazione dei risultati alle cause radice completamente supportate, nonché l'euristica per presentare le riparazione all'utente nell'ordine consigliato. Quando si usano queste funzioni, è necessario fornire manualmente tali funzionalità. È anche necessario assicurarsi di liberare la memoria usata dai risultati della diagnosi.

    Per iniziare la diagnosi, chiamare [**la funzione NdfDiagnoseIncident.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) Eventuali problemi rilevati verranno restituiti all'applicazione come raccolta di strutture [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) che descrivono le cause radice identificate e le possibili soluzioni.

    Dopo aver selezionato un ripristino (o aver chiesto all'utente di selezionare una riparazione), è necessario chiamare [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) per tentare il ripristino e determinare se il problema è stato risolto.

    In alcuni casi, un ripristino potrebbe essere eseguito correttamente, ma non risolverà il problema. In questi casi, è consigliabile chiudere l'evento imprevisto esistente e quindi aprirne uno nuovo. Ciò garantisce l'identificazione di eventuali nuovi problemi non mascherati dal ripristino iniziale. Si supponga, ad esempio, che nessuna rete wireless sia stata visibile. Dopo la reimpostazione della scheda, le reti wireless sono visibili, ma nessuna di esse è nell'elenco preferito. Si tratta di un nuovo problema che richiederebbe una nuova diagnosi per l'identificazione. Se un secondo tentativo di diagnosi di questo tipo non identifica problemi aggiuntivi, è possibile tentare un ripristino diverso per risolvere il problema originale oppure l'utente può essere informato che il problema non può essere risolto.

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) e [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) sono API sincrone. Se si vuole annullare l'attività avviata da queste funzioni, chiamare [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) da un altro thread. La funzione restituirà al successivo punto di arresto disponibile nel processo di diagnosi o ripristino.

    In qualsiasi momento, è possibile chiamare [**facoltativamente NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) per recuperare una copia del log NDF per la sessione di diagnosi corrente e includerla nei log dell'applicazione. Il log viene scaricato una volta recuperato e le chiamate successive recupereranno solo gli eventi che si sono verificati dopo l'ultima chiamata a questa funzione.

## <a name="closing-an-incident"></a>Chiusura di un evento imprevisto

Al termine della diagnosi di un evento imprevisto, chiamare [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) per liberare le risorse di sistema associate all'esecuzione della diagnostica sull'evento imprevisto. Si noti che in questo modo non vengono liberati gli oggetti creati da [**NdfDiagnoseIncident.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)
