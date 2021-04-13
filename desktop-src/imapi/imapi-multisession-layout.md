---
title: Layout multisessione IMAPi
description: IMAPi fornisce agli sviluppatori di applicazioni la possibilità di creare immagini ISO 9660 e UDF file system e di masterizzarle su CD, DVD e Blu-Ray \ 8482; supporti ottici.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104568364"
---
# <a name="imapi-multisession-layout"></a>Layout multisessione IMAPi

IMAPi fornisce agli sviluppatori di applicazioni la possibilità di creare immagini ISO 9660 e UDF file system e di masterizzarle su CD, DVD e Blu-Ray™ supporti ottici. Con Windows 7, IMAPi fornisce supporto aggiuntivo per la masterizzazione multisessione su DVD e Blu-Ray™ supporti riscrivibili.

La documentazione seguente illustra in dettaglio il layout dei dischi usato da IMAPi per implementare la multisessione. Queste informazioni devono essere utilizzate per garantire l'interoperabilità tra IMAPi e altri software di masterizzazione, nonché consentire agli sviluppatori del software di creare immagini di dischi multisessione compatibili con IMAP.

> [!Note]  
> Per un esempio dettagliato della creazione di un disco a più sessioni, vedere [creazione di un disco a più sessioni](creating-a-multisession-disc.md).

 

## <a name="multisession-on-sequential-media"></a>Multisessione su supporti sequenziali

L'implementazione di IMAPi di Multisession su supporti sequenziali è supportata per l'uso con CD-R, CD-RW, DVD-R, DVD + R e Blu-Ray™ supporti. IMAPi usa la modalità di registrazione Session-at-once per CD-RW e, di conseguenza, in questo scenario il formato è considerato un tipo di supporto sequenziale.

In uno scenario che prevede la multisessione su supporti sequenziali mediante UDF, IMAPi scrive le strutture di ancoraggio (UDF Anchor volume descrittor Pointer-avoirdupois), le strutture dei volumi (UDF Volume Descriptor Sequence-VDS) e le strutture di metadati file system (UDF file set Descriptor-FSD) all'inizio di ogni nuova sessione, come illustrato nel diagramma seguente:

![Diagramma che mostra la struttura dei metadati di file system con il punto di montaggio "Import/F S" indicato con una freccia rossa in corrispondenza dell'ancoraggio della sessione fisica 2.](images/multises1.png)

> [!Note]  
> Questa figura illustra il layout del disco IMAPi quando si usa UDF 2,50 con metadati ridondanti.

 

I dati archiviati in un supporto registrato in sequenza sono costituiti da una serie di sessioni fisiche. Ogni sessione contiene un file system completo che rappresenta i dati utente come un set di file organizzati in directory. Il file system metadati è costituito da una serie di strutture di dati organizzate gerarchicamente. Nella parte superiore della gerarchia risiedono le strutture di ancoraggio (avoirdupois) situate in indirizzi di blocco logico predefiniti (LBAs). Le strutture di ancoraggio specificano i percorsi delle strutture di livello successivo che non hanno indirizzi predefiniti. Il livello successivo della gerarchia dopo le strutture di ancoraggio contiene le strutture del volume (VDS) che descrivono le proprietà del volume e fanno riferimento alle strutture di metadati file system (FSD), che a loro volta descrivono i singoli file e directory.

## <a name="multisession-on-rewritable-media"></a>Multisessione su supporti riscrivibili

L'approccio per i supporti sequenziali descritti nella sezione precedente è incompatibile con i supporti riscrivibili (non sequenziali). Questi formati multimediali includono DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ riscrivibili e altri supporti scrivibili casuali, ad esempio i dischi Iomega REV. Il supporto riscrivibile non supporta il concetto di sessioni fisiche corrispondenti a sessioni logiche, ovvero incrementi individuali sottoposte a commit da un'applicazione Master. Viene esposta una sola sessione fisica, ovvero un'area a partire dall'inizio del disco che rappresenta l'intera area indirizzabile che può contenere più sessioni logiche.

> [!Note]  
> Mentre DVD-RW è un'eccezione in quanto supporta il concetto di sessione fisica in modalità sequenziale, questa funzionalità non è attualmente supportata da IMAPi.

 

Per risolvere la mancanza di mapping uno-a-uno tra sessioni fisiche e logiche in formati riscrivibili, IMAPi Aggiorna selettivamente le strutture di ancoraggio (avoirdupois) nella *prima* sessione logica in modo che punti alle nuove strutture di volumi (VDS) e alle strutture di metadati file System (FSD) all'inizio dell' *Ultima* sessione logica, come illustrato nel diagramma seguente:

![Diagramma che mostra la struttura dei metadati di file system con il punto di montaggio "Import/F S" indicato con una freccia rossa in corrispondenza dell'ancoraggio della sessione logica 1.](images/multises2.png)

> [!Note]  
> Questa figura illustra il layout del disco IMAPi quando si usa UDF 2,50 con metadati ridondanti.

 

Quando si aggiunge una nuova sessione logica a un disco riscrivibile, IMAPi determina innanzitutto la fine dell'ultima sessione logica analizzando i metadati del volume (VDS). IMAPi aggiunge quindi la nuova sessione logica, completa di nuovo ancoraggio (avoirdupois), volume (VDS) e file system Metadata Structures (FSD), fisicamente contiguo con la sessione logica registrata in precedenza. Il passaggio finale richiede l'aggiornamento delle strutture di ancoraggio (avoirdupois) all'inizio della prima sessione logica in modo che puntino alle strutture del volume (VDS) nella *nuova* sessione logica. Il risultato operativo è identico a quello dei supporti sequenziali.

## <a name="additional-recommendations"></a>Ulteriori indicazioni

-   **Layout partizione**

    Per ottenere IMAPi compatibilità, è consigliabile che gli sviluppatori di software di terze parti usino i layout dei dischi descritti in questa documentazione. Gli sviluppatori devono evitare i layout con file system partizioni che occupano l'intero disco, perché ciò richiede la registrazione delle applicazioni per individuare lo spazio disponibile all'interno delle partizioni esistenti ogni volta che i dati devono essere aggiunti al disco. Spesso, le applicazioni di registrazione a questo scopo utilizzano marcatori proprietari sul disco per indicare la quantità di spazio effettivamente occupata dai dati utente. Questi layout di disco non sono compatibili con IMAPi perché i marcatori proprietari non sono riconosciuti all'esterno dell'applicazione per cui sono stati creati.

-   **Tipo di partizione UDF**

    IMAPi usa il tipo di partizione UDF di **sola lettura** nell'implementazione di Multisession su supporti riscrivibili. Gli sviluppatori di software di masterizzazione di terze parti devono usare il tipo di partizione UDF di **sola lettura** per ottenere compatibilità con la masterizzazione basata su Windows tramite IMAPI. Se viene usato un altro tipo di partizione UDF, ad esempio **riscrivibile** , IMAPI non è in grado di fornire supporto per la master.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un disco multisessione](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




