---
description: I moduli unione forniscono un metodo standard per distribuire componenti Windows installer condivisi e logica di installazione alle applicazioni.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Uso dell'automazione per unire un modulo unione in un database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513a765670df44396c34537721eb6f75ed98796dd31ddefd5d26387e2a6b5d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141330"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Uso dell'automazione per unire un modulo unione in un database

[I moduli unione](merge-modules.md) forniscono un metodo standard per distribuire i componenti Windows [*installer*](c-gly.md)condivisi e la logica di installazione alle applicazioni.

I moduli unione devono essere uniti in un pacchetto di installazione usando uno strumento di unione. La procedura consigliata consiste nell'ottenere uno strumento di unione distribuito liberamente o nell'acquistare uno degli strumenti di merge disponibili da fornitori di software [ indipendenti, ](merge-module-automation.md)ad esempio è possibile usareMergemod.dll.

La procedura seguente illustra come unire un modulo unione in un database Windows Installer usando [Automazione moduli unione](merge-module-automation.md).

**Per unire un modulo in un database**

1.  Aprire un file di log usando il [**metodo OpenLog.**](merge-openlog.md)

    Questo passaggio è necessario solo se è necessario creare un file di log o aggiungere un file di log esistente per il processo di unione.

2.  Aprire il [.msi](windows-installer-file-extensions.md) di installazione usando il [**metodo OpenDatabase**](merge-opendatabase.md) dell'oggetto [**merge**](merge-object.md).

    Questo passaggio è obbligatorio.

    Il database aperto è quello che si desidera ricevere il modulo unione.

3.  Aprire il modulo unione con estensione [msm](windows-installer-file-extensions.md) usando il [**metodo OpenModule.**](merge-openmodule.md)

    Questo passaggio è obbligatorio.

    Si tratta del modulo unione che viene unito nel database. Un modulo deve essere aperto prima di poter essere unito a un database di installazione.

4.  Unire il modulo nel database di installazione chiamando il [**metodo Merge**](merge-object.md) o [**mergeEx.**](merge-mergeex.md)

    Questo passaggio è obbligatorio.

    Il [**metodo Merge**](merge-object.md) o [**mergeEx**](merge-mergeex.md) può essere chiamato una sola volta per unire una combinazione specifica [ di](windows-installer-file-extensions.md).msifile con estensione msm.

    > [!Note]  
    > Il [**metodo MergeEx**](merge-mergeex.md) è disponibile solo in [Mergemod.dll versione 2.0](merge-module-automation.md) o successiva e solo quando si usa l'interfaccia [**IMsmMerge2.**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2)

     

5.  Recuperare la [**proprietà Errors**](merge-errors.md) ed esaminare la raccolta di oggetti [**Error**](error-object.md) restituita per i conflitti di merge o altri errori.

    È necessario risolvere eventuali errori.

    Il recupero non è distruttivo e più istanze della raccolta di errori possono essere recuperate leggendo ripetutamente la [**proprietà Errors.**](merge-errors.md)

6.  Associare i componenti del modulo unione alle funzionalità usando il [**metodo**](merge-connect.md) Connessione merge.

    Questo passaggio è necessario solo se sono disponibili funzionalità esistenti e si desidera aggiungere funzionalità da unire nel database di installazione.

    Prima di chiamare questo metodo, deve esistere una funzionalità. Per altre informazioni, vedere [Connessione di un modulo unione a più funzionalità](connecting-a-merge-module-to-multiple-features.md).

7.  Se necessario, estrarre i file di origine dal modulo eseguendo una o più delle operazioni seguenti:
    -   Usare [**ExtractFiles o**](merge-extractfiles.md) [**ExtractFilesEx**](merge-extractfilesex.md) per estrarre i file da un file .cab incorporato e quindi copiarlo in una directory specificata.
        > [!Note]  
        > [**ExtractFilesEx**](merge-extractfilesex.md) richiede [Mergemod.dll versione 2.0](merge-module-automation.md) o successiva.

         

    -   Usare [**ExtractCAB**](merge-extractcab.md) per estrarre i file da un file .cab incorporato e quindi salvarli in un file specificato.
    -   Usare [**CreateSourceImage**](merge-createsourceimage.md) per estrarre i file da un modulo e quindi, dopo l'unione, copiare in un'immagine di origine su disco.
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) è disponibile solo in [Mergemod.dll versione 2.0](merge-module-automation.md) o successiva.

         
8.  Chiudere il modulo unione aperto corrente usando il [**metodo CloseModule.**](merge-closemodule.md)

    Questo passaggio è obbligatorio.

9.  Chiudere il database di installazione aperto usando il [**metodo CloseDatabase.**](merge-closedatabase.md)

    Questo passaggio è obbligatorio.

    La chiusura di un database cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non vengono recuperati.

10. Chiudere il file di log corrente usando il [**metodo CloseLog.**](merge-closelog.md)

    Questo passaggio è obbligatorio se si dispone di un file di log aperto.

Dopo che il modulo è stato unito al database [ usando ](merge-module-automation.md)Mergemod.dll, è necessario aggiornare [media table](media-table.md) per descrivere il layout dell'immagine di origine desiderato. Il processo di unione fornito da Mergemod.dll non aggiorna la tabella dei supporti perché il consumer del modulo di merge può selezionare vari modi per eseguire il layout dell'immagine di origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



