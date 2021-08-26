---
description: I moduli unione offrono agli sviluppatori un metodo standard per distribuire i componenti Windows Installer condivisi e la logica di installazione alle applicazioni.
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: Uso dell'API per unire un modulo di merge in un database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdbeb68b193cceff10fbd1cd3f56f4c8804a4e1fb4f7c169fd2d893dc0b4bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039031"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>Uso dell'API per unire un modulo di merge in un database

[I moduli unione](merge-modules.md) offrono agli sviluppatori un metodo standard per distribuire i componenti Windows [*Installer*](c-gly.md) condivisi e la logica di installazione alle applicazioni. I moduli unione devono essere uniti in un pacchetto di installazione tramite uno strumento di unione. L'alternativa migliore consiste nell'ottenere uno strumento di merge distribuito gratuitamente o acquistare uno degli strumenti di unione disponibili da fornitori di software indipendenti. Ad esempio, è possibile usare la funzionalità fornita [ daMergemod.dll](merge-module-automation.md).

Usare i passaggi seguenti in sequenza per unire un modulo unione in un database di installazione Windows Installer dall'API [diMergemod.dll](merge-module-automation.md).

**Per unire un modulo unione in un database di installazione Windows Installer**

1.  Aprire un file di log [**usando OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog). Questo passaggio è necessario solo se è necessario creare un file di log o aggiungerne uno esistente per il processo di unione.
2.  Aprire il database di installazione, [.msi file](windows-installer-file-extensions.md), che riceverà il modulo di unione usando [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase). Questo passaggio è obbligatorio.
3.  Aprire il modulo unione, [un file con estensione msm,](windows-installer-file-extensions.md)che viene unito nel database usando [**OpenModule.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) Un modulo deve essere aperto prima di poter essere unito a un database di installazione. Questo passaggio è obbligatorio.
4.  Unire il modulo nel database di installazione usando [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) o [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex). Si noti **che Merge** o **MergeEx** può essere chiamato una sola volta per unire una particolare combinazione di .msi file con estensione msm. **MergeEx** è disponibile solo quando si [usaMergemod.dll versione 2.0](merge-module-automation.md) o successiva e solo quando si usa l'interfaccia [IMsmMerge2.](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Questo passaggio è obbligatorio.
5.  Chiamare [**get \_ Errors ed**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) esaminare la raccolta recuperata di errori per i conflitti di merge o altri errori. Il recupero non è distruttivo. È possibile recuperare più istanze della raccolta di errori leggendo ripetutamente la chiamata **a get \_ Errors**. Sarà necessario risolvere eventuali errori in base alle esigenze.
6.  Associare i componenti del modulo unione a tutte le funzionalità aggiuntive che sono state o verranno unite nel database di installazione [**usando Connessione**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect). La funzionalità deve esistere già prima di chiamare questo metodo. Questo passaggio è necessario solo se si dispone di funzionalità aggiuntive. Per altre informazioni, vedere Connessione di un [modulo di merge a più funzionalità](connecting-a-merge-module-to-multiple-features.md)
7.  Se necessario, estrarre i file di origine dal modulo eseguendo una o più delle operazioni seguenti.

    Per estrarre file da un file .cab e quindi copiarlo in una directory specificata, usare [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) o [**ExtractFilesEx.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) Si noti **che ExtractFilesEx** [ richiedeMergemod.dll versione 2.0](merge-module-automation.md) o successiva.

    Per estrarre file da un file .cab e quindi salvarli in un file specificato, usare [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab).

    Per estrarre file da un modulo e quindi copiare in un'immagine di origine su disco dopo l'unione, usare [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage). Si noti **che CreateSourceImage** è disponibile solo con [Mergemod.dll versione 2.0](merge-module-automation.md) o successiva.

8.  Chiudere il modulo unione aperto corrente usando [**CloseModule.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) Questo passaggio è obbligatorio.
9.  Chiudere il database di installazione aperto corrente usando [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase). Questo passaggio è obbligatorio. La chiusura di un database cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non sono stati recuperati.
10. Chiudere il file di log corrente [**usando CloseLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog). Questo passaggio è obbligatorio se è stato aperto un file di log.

Dopo che il modulo è stato unito al database [ usandoMergemod.dll](merge-module-automation.md), è necessario aggiornare [media table](media-table.md) per descrivere il layout dell'immagine di origine desiderato. Il processo di unione fornito da Mergemod.dll non aggiorna la tabella dei supporti perché il consumer del modulo di unione può selezionare vari modi per eseguire il layout dell'immagine di origine.

 

 
