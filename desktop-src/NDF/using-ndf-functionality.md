---
title: Uso della funzionalità NDF
description: Microsoft fornisce accesso alla funzionalità NDF tramite un'API pubblica. Quando si verifica un problema, l'applicazione può usare questa API per sfruttare questa funzionalità nel contesto di un'applicazione specifica.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca74a8a80f7babca75182625ec71dc1ec47cbc7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/10/2020
ms.locfileid: "104398828"
---
# <a name="using-ndf-functionality"></a>Uso della funzionalità NDF

Microsoft fornisce accesso alla funzionalità NDF tramite un'API pubblica. Quando si verifica un problema, l'applicazione può usare questa API per sfruttare questa funzionalità nel contesto di un'applicazione specifica.

Sono disponibili tre fasi di esecuzione della diagnosi con NDF, ovvero la creazione di un evento imprevisto, l'esecuzione di diagnosi e riparazioni e la chiusura dell'evento imprevisto. In questa panoramica vengono indicate le funzioni NDF che possono essere rilevanti per uno scenario specifico. Per informazioni dettagliate su ogni funzione, vedere la sezione di [riferimento a NDF](ndf-reference.md) .

## <a name="creating-an-incident"></a>Creazione di un evento imprevisto

Una sessione di diagnostica NDF richiede un evento imprevisto specifico da diagnosticare. Sono disponibili diverse funzioni che è possibile usare per creare un evento imprevisto. Scegliere la funzione che corrisponde maggiormente a quella che l'applicazione stava tentando di eseguire quando si è verificato l'errore.

-   [**NdfCreateConnectivityIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident): problemi generali di connettività Internet che non necessitano di informazioni aggiuntive.
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**NdfCreateWebIncidentEx**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex): connessione a un URL http o HTTPS.
-   [**NdfCreateSharingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident): accesso a un percorso UNC o a una condivisione file.
-   [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident): risoluzione di un nome host DNS.
-   [**NdfCreatePnrpIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident): risoluzione di un nome peer PNRP.
-   [**NdfCreateGroupingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident): aggiunta di un gruppo peer-to-peer.
-   [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident): connessione a una destinazione tramite un socket (quando nessuna delle altre funzioni viene applicata in modo specifico).
-   [**NdfCreateIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident): usata quando non è appropriato alcun altro scenario e la classe helper NDF specifica da richiamare è nota (insieme agli argomenti necessari). Usato principalmente a scopo di test da parte degli sviluppatori di applicazioni che hanno scritto una propria classe helper.

## <a name="running-diagnosis-and-repairs"></a>Esecuzione di diagnosi e riparazioni

Esistono due modi per avviare la diagnostica e la funzionalità di ripristino.

-   Uso dell'interfaccia utente di Windows (scelta consigliata)

    Quando è in esecuzione nell'interfaccia utente standard di Windows, è possibile chiamare semplicemente la funzione [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) . Viene avviata la procedura guidata NDF che consente all'utente di identificare e, se possibile, di risolvere il problema. La funzione restituirà una volta terminato il processo. L'interfaccia utente è facoltativamente modale per l'applicazione.

-   Uso di un'interfaccia utente personalizzata (solo Windows 7 e versioni successive)

    Sono disponibili diverse funzioni da usare in scenari in cui non viene visualizzata alcuna interfaccia utente o in cui l'esperienza Windows standard non è in uso (ad esempio, Media Center, applicazioni incorporate e il prompt dei comandi). Questa opzione consente di ignorare le funzionalità dell'esperienza utente fornite nella procedura guidata NDF, che include la limitazione dei risultati alle cause radice completamente supportate, nonché l'euristica per presentare le riparazioni all'utente nell'ordine consigliato. Quando si usano queste funzioni, è necessario fornire le stesse funzionalità. È inoltre necessario assicurarsi di liberare la memoria utilizzata dai risultati della diagnosi.

    Per iniziare la diagnosi, chiamare la funzione [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) . Eventuali problemi rilevati verranno restituiti all'applicazione come raccolta di strutture [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) che descrivono le cause principali identificate e le possibili correzioni.

    Dopo aver selezionato un ripristino (o chiesto all'utente di selezionare un ripristino), è necessario chiamare [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) per tentare la riparazione e determinare se il problema è stato risolto.

    In alcuni casi, una riparazione può essere eseguita correttamente, ma non risolverà il problema. In questi casi, è consigliabile chiudere l'evento imprevisto esistente e quindi aprirne uno nuovo. In questo modo verranno identificati tutti i nuovi problemi non mascherati dalla correzione iniziale. Si supponga, ad esempio, che non sia stata visualizzata alcuna rete wireless. Dopo aver reimpostato l'adapter, le reti wireless sono visibili, ma nessuna di esse si trova nell'elenco Preferiti. Si tratta di un nuovo problema che richiederebbe una nuova diagnosi da identificare. Se un secondo tentativo di diagnosi non identifica ulteriori problemi, è possibile tentare di risolvere il problema originale oppure è possibile che l'utente sia informato che non è stato possibile risolvere il problema.

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) e [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) sono API sincrone. Se si desidera annullare l'attività avviata da queste funzioni, chiamare [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) da un altro thread. La funzione restituirà al successivo punto di arresto disponibile nel processo di diagnosi o di ripristino.

    In qualsiasi momento, è possibile chiamare [**NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) per recuperare una copia del log NDF per la sessione di diagnosi corrente e includerla nei log dell'applicazione. Il log viene svuotato una volta recuperato e le chiamate successive recupereranno solo gli eventi che si sono verificati dopo l'ultima chiamata a questa funzione.

## <a name="closing-an-incident"></a>Chiusura di un evento imprevisto

Al termine della diagnosi di un evento imprevisto, chiamare [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) per liberare le risorse di sistema associate all'esecuzione della diagnostica in tale evento imprevisto. Si noti che questa operazione non libera gli oggetti creati da [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident).
