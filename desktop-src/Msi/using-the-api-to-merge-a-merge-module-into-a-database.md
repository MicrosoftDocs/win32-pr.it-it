---
description: I moduli unione forniscono un metodo standard che consente agli sviluppatori di distribuire componenti di Windows Installer condivisi e di configurare la logica per le applicazioni.
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: Utilizzo dell'API per unire un modulo merge in un database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68298671045825dda41ad120896fa22c89f068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314765"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>Utilizzo dell'API per unire un modulo merge in un database

I [moduli unione](merge-modules.md) forniscono un metodo standard che consente agli sviluppatori di distribuire [*componenti*](c-gly.md) di Windows Installer condivisi e di configurare la logica per le applicazioni. I moduli merge devono essere Uniti in un pacchetto di installazione usando uno strumento di merge. L'alternativa migliore è ottenere uno strumento di merge distribuito liberamente oppure acquistare uno degli strumenti di Unione disponibili presso i fornitori di software indipendenti. Ad esempio, è possibile usare la funzionalità fornita da [Mergemod.dll](merge-module-automation.md).

Usare i passaggi seguenti in sequenza per unire un modulo merge in un database di installazione Windows Installer dall'API di [Mergemod.dll](merge-module-automation.md).

**Per unire un modulo merge in un database di installazione Windows Installer**

1.  Aprire un file di log usando [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog). Questo passaggio è necessario solo se è necessario creare un file di log o accodare un file di log esistente per il processo di merge.
2.  Aprire il database di installazione, un [file con estensione msi](windows-installer-file-extensions.md), che riceverà il modulo merge usando [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase). Questo passaggio è obbligatorio.
3.  Aprire il modulo merge, ovvero un [file con estensione MSM](windows-installer-file-extensions.md), da unire nel database tramite [**ApriModulo**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule). Prima di poter eseguire il merge di un modulo con un database di installazione, è necessario aprirlo. Questo passaggio è obbligatorio.
4.  Unire il modulo nel database di installazione usando [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) o [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex). Si noti che **merge** o **MergeEx** può essere chiamato una sola volta per unire una particolare combinazione di file con estensione msi e MSM. **MergeEx** è disponibile solo quando si usa [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva e solo quando si usa l'interfaccia [IMsmMerge2](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) . Questo passaggio è obbligatorio.
5.  Chiamare [**get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) ed esaminare la raccolta di errori recuperata per i conflitti di merge o altri errori. Il recupero non è distruttivo. È possibile recuperare più istanze della raccolta di errori leggendo ripetutamente la chiamata di **get \_ Errors**. Sarà necessario risolvere gli eventuali errori nel modo appropriato per il caso.
6.  Associare i componenti del modulo merge a eventuali funzionalità aggiuntive che sono state o verranno unite nel database di installazione tramite [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect). La funzionalità deve esistere già prima di chiamare questo metodo. Questo passaggio è necessario solo se si dispone di funzionalità aggiuntive. per ulteriori informazioni, vedere [connessione di un modulo merge a più funzionalità](connecting-a-merge-module-to-multiple-features.md)
7.  Se necessario, estrarre i file di origine dal modulo eseguendo una o più delle operazioni seguenti.

    Per estrarre i file da un file con estensione cab incorporato e quindi copiarli in una directory specificata, utilizzare [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) o [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex). Si noti che **ExtractFilesEx** richiede [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva.

    Per estrarre i file da un file con estensione cab incorporato e quindi salvarli in un file specificato, usare [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab).

    Per estrarre i file da un modulo e quindi copiarli in un'immagine di origine su disco dopo il merge, usare [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage). Si noti che **CreateSourceImage** è disponibile solo con [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva.

8.  Chiudere il modulo Open merge corrente usando [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule). Questo passaggio è obbligatorio.
9.  Chiudere il database di installazione aperto corrente usando [**ChiudiDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase). Questo passaggio è obbligatorio. La chiusura di un database Cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non sono stati recuperati.
10. Chiudere il file di log corrente usando [**CloseLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog). Questo passaggio è obbligatorio se è stato aperto un file di log.

Dopo che il modulo è stato unito al database usando [Mergemod.dll](merge-module-automation.md), è necessario aggiornare la [tabella dei supporti](media-table.md) per descrivere il layout dell'immagine di origine desiderato. Il processo di merge fornito da Mergemod.dll non aggiorna la tabella dei supporti perché il consumer del modulo merge può selezionare diversi modi per creare il layout dell'immagine di origine.

 

 
