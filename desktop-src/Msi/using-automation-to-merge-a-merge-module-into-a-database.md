---
description: I moduli unione forniscono un metodo standard per la distribuzione di componenti di Windows Installer condivisi e l'impostazione della logica per le applicazioni.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Utilizzo dell'automazione per unire un modulo merge in un database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308668"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Utilizzo dell'automazione per unire un modulo merge in un database

I [moduli unione](merge-modules.md) forniscono un metodo standard per la distribuzione di [*componenti*](c-gly.md)di Windows Installer condivisi e l'impostazione della logica per le applicazioni.

I moduli merge devono essere Uniti in un pacchetto di installazione usando uno strumento di merge. La procedura consigliata consiste nell'ottenere uno strumento di merge distribuito liberamente oppure acquistare uno degli strumenti di merge disponibili da fornitori di software indipendenti. ad esempio, è possibile utilizzare [Mergemod.dll](merge-module-automation.md).

Nella procedura riportata di seguito viene illustrato come unire un modulo merge in un database Windows Installer utilizzando l' [automazione del modulo merge](merge-module-automation.md).

**Per unire un modulo in un database**

1.  Aprire un file di log usando il metodo [**OpenLog**](merge-openlog.md) .

    Questo passaggio è necessario solo se è necessario creare un file di log o accodare un file di log esistente per il processo di merge.

2.  Aprire il database di installazione con [estensione msi](windows-installer-file-extensions.md) utilizzando il metodo [**OpenDatabase**](merge-opendatabase.md) dell' [**oggetto merge**](merge-object.md).

    Questo passaggio è obbligatorio.

    Il database aperto è quello che si desidera ricevere per il modulo unione.

3.  Aprire il modulo merge con [estensione MSM](windows-installer-file-extensions.md) usando il metodo [**ApriModulo**](merge-openmodule.md) .

    Questo passaggio è obbligatorio.

    Si tratta del modulo merge che viene unito nel database. Prima di poter eseguire il merge di un modulo con un database di installazione, è necessario aprirlo.

4.  Unire il modulo nel database di installazione chiamando il metodo [**merge**](merge-object.md) o il metodo [**MergeEx**](merge-mergeex.md) .

    Questo passaggio è obbligatorio.

    Il metodo [**merge**](merge-object.md) o il metodo [**MergeEx**](merge-mergeex.md) può essere chiamato una sola volta per unire una combinazione specifica di file con [estensione msi](windows-installer-file-extensions.md) e MSM.

    > [!Note]  
    > Il metodo [**MergeEx**](merge-mergeex.md) è disponibile solo in [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva e solo quando si usa l'interfaccia [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .

     

5.  Recuperare la proprietà Errors ed esaminare la raccolta di oggetti [**Error**](error-object.md) restituiti [**per i conflitti**](merge-errors.md) di merge o altri errori.

    È necessario risolvere gli eventuali errori.

    Il recupero non è distruttivo e più istanze della raccolta errori possono essere recuperate leggendo ripetutamente la proprietà [**Errors**](merge-errors.md) .

6.  Associare i componenti del modulo merge alle funzionalità usando il metodo [**Connect**](merge-connect.md) .

    Questo passaggio è necessario solo se si dispone di funzionalità esistenti e si desidera aggiungere funzionalità da unire nel database di installazione.

    È necessario che esista una funzionalità prima di chiamare questo metodo. Per ulteriori informazioni, vedere [connessione di un modulo merge a più funzionalità](connecting-a-merge-module-to-multiple-features.md).

7.  Se necessario, estrarre i file di origine dal modulo eseguendo una o più delle operazioni seguenti:
    -   Usare [**ExtractFiles**](merge-extractfiles.md) o [**ExtractFilesEx**](merge-extractfilesex.md) per estrarre i file da un file CAB incorporato e quindi copiarli in una directory specificata.
        > [!Note]  
        > [**ExtractFilesEx**](merge-extractfilesex.md) richiede [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva.

         

    -   Utilizzare [**ExtractCAB**](merge-extractcab.md) per estrarre i file da un file con estensione cab incorporato e quindi salvarli in un file specificato.
    -   Usare [**CreateSourceImage**](merge-createsourceimage.md) per estrarre i file da un modulo e quindi, dopo il merge, copiarli in un'immagine di origine su disco.
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) è disponibile solo in [Mergemod.dll versione 2,0](merge-module-automation.md) o successiva.

         
8.  Chiudere il modulo Open merge corrente usando il metodo [**CloseModule**](merge-closemodule.md) .

    Questo passaggio è obbligatorio.

9.  Chiudere il database di installazione aperto utilizzando il metodo [**ChiudiDatabase**](merge-closedatabase.md) .

    Questo passaggio è obbligatorio.

    La chiusura di un database Cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non vengono recuperati.

10. Chiudere il file di log corrente usando il metodo [**CloseLog**](merge-closelog.md) .

    Questo passaggio è obbligatorio se si dispone di un file di log aperto.

Dopo che il modulo è stato unito al database usando [Mergemod.dll](merge-module-automation.md), è necessario aggiornare la [tabella dei supporti](media-table.md) per descrivere il layout dell'immagine di origine desiderato. Il processo di merge fornito da Mergemod.dll non aggiorna la tabella dei supporti perché il consumer del modulo merge può selezionare diversi modi per creare il layout dell'immagine di origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



