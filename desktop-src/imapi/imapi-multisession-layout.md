---
title: Layout multisessione IMAPI
description: IMAPI offre agli sviluppatori di applicazioni la possibilità di creare immagini file system ISO 9660 e UDF e masterizzarle su CD, DVD e Blu-Ray \ 8482; supporti ottici.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d816d293a3474f46dc3a48577a46615672103099dc2aa561d393953f29ccf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249414"
---
# <a name="imapi-multisession-layout"></a>Layout multisessione IMAPI

IMAPI offre agli sviluppatori di applicazioni la possibilità di creare immagini file system ISO 9660 e UDF e masterizzarle su CD, DVD e Blu-Ray™ ottico. Con Windows 7, IMAPI offre supporto aggiuntivo per la masterizzazione multisessione su DVD e blu-ray™ supporti risibilibili.

Nella documentazione seguente viene illustrato in dettaglio il layout del disco utilizzato da IMAPI per implementare più sessioni. Queste informazioni devono essere usate per garantire l'interoperabilità tra IMAPI e altri software di masterizzazione, nonché per consentire agli sviluppatori di questo software di creare immagini disco multisessione compatibili con IMAPI.

> [!Note]  
> Per un esempio che illustra in dettaglio la creazione di un disco multisessione, vedere [Creazione di un disco multisessione](creating-a-multisession-disc.md).

 

## <a name="multisession-on-sequential-media"></a>Multisessione su supporti sequenziali

L'implementazione IMAPI di multisessione su supporti sequenziali è supportata per l'uso con supporti CD-R, CD-RW, DVD-R, DVD+R e Blu-Ray™. IMAPI usa la modalità di registrazione Session-At-Once per CD-RW e di conseguenza, in questo scenario, il formato viene considerato un tipo di supporto sequenziale.

In uno scenario che prevede la multisessione su supporti sequenziali tramite la funzione definita dall'utente, IMAPI scrive le strutture di ancoraggio (UDF Anchor Volume Descriptor Pointer - AVDP), le strutture del volume (UDF Volume Descriptor Sequence - VDS) e le strutture dei metadati file system (UDF File Set Descriptor - FSD) all'inizio di ogni nuova sessione, come descritto nel diagramma seguente:

![Diagramma che mostra la struttura file system metadati con il punto di montaggio 'Import/F S' indicato con una freccia rossa in corrispondenza dell'ancoraggio della sessione fisica 2.](images/multises1.png)

> [!Note]  
> Questa figura illustra il layout del disco IMAPI quando si usa UDF 2.50 con metadati ridondanti.

 

I dati archiviati in supporti registrati in sequenza sono costituiti da una serie di sessioni fisiche. Ogni sessione contiene un'file system che rappresenta i dati utente come set di file organizzati in directory. I file system metadati sono costituiti da una serie di strutture di dati organizzate gerarchicamente. Nella parte superiore della gerarchia risiedono strutture di ancoraggio (AVDP) che si trovano in indirizzi di blocchi logici predefiniti. Le strutture di ancoraggio specificano le posizioni delle strutture di livello successivo che non hanno indirizzi predefiniti. Il livello successivo di gerarchia dopo le strutture di ancoraggio contiene le strutture del volume (VDS) che descrivono le proprietà del volume e fanno riferimento alle strutture di metadati file system (FSD), che a loro volta descrivono singoli file e directory.

## <a name="multisession-on-rewritable-media"></a>Multisessione su supporti risibili

L'approccio per i supporti sequenziali descritto nella sezione precedente è incompatibile con i supporti riabilitabili (non sequenziali). Questi formati multimediali includono DVD-RW, DVD+RW, DVD-RAM, Blu-Ray™ risibile e altri supporti scrivibili casuali, ad esempio dischi REV Iomega. I supporti riscibili non supportano il concetto di sessioni fisiche corrispondenti alle sessioni logiche, ovvero singoli incrementi di cui viene eseguito il commit da parte di un'applicazione master. Viene esposta una sola sessione fisica, ovvero un'area che inizia all'inizio del disco che rappresenta l'intera area indirizzabile che può contenere più sessioni logiche.

> [!Note]  
> Anche se DVD-RW è un'eccezione perché supporta il concetto di sessione fisica in modalità sequenziale, questa funzionalità non è attualmente supportata da IMAPI.

 

Per risolvere la mancanza di mapping uno-a-uno tra sessioni fisiche e logiche nei formati risibile, IMAPI aggiorna in modo selettivo le strutture di ancoraggio (AVDP) nella prima sessione  logica in modo che puntino alle nuove strutture di volume (VDS) e alle strutture di metadati file system (FSD) all'inizio dell'ultima sessione logica, come descritto nel diagramma seguente: 

![Diagramma che mostra la struttura file system metadati con il punto di montaggio 'Import/F S' indicato con una freccia rossa in corrispondenza dell'ancoraggio della sessione logica 1.](images/multises2.png)

> [!Note]  
> Questa figura illustra il layout del disco IMAPI quando si usa UDF 2.50 con metadati ridondanti.

 

Quando si aggiunge una nuova sessione logica a un disco risibile, IMAPI determina innanzitutto la fine dell'ultima sessione logica analizzando i metadati del volume (VDS). IMAPI aggiunge quindi la nuova sessione logica, completa di nuove strutture di metadati di ancoraggio (AVDP), volume (VDS) e file system metadata structures (FSD), fisicamente contigue con la sessione logica registrata in precedenza. Il passaggio finale richiede che le strutture di ancoraggio (AVDP) all'inizio della prima sessione logica siano aggiornate in modo che puntino alle strutture del volume (VDS) nella nuova *sessione* logica. Il risultato operativo è identico a quello dei supporti sequenziali.

## <a name="additional-recommendations"></a>Ulteriori indicazioni

-   **Layout partizione**

    Per ottenere la compatibilità IMAPI, è consigliabile che gli sviluppatori di software di terze parti usino i layout dei dischi descritti in questa documentazione. Gli sviluppatori devono evitare layout con partizioni file system che occupano l'intero disco, perché ciò richiede la registrazione di applicazioni per individuare lo spazio disponibile all'interno delle partizioni esistenti ogni volta che è necessario aggiungere dati al disco. Spesso, le applicazioni di registrazione a tale scopo utilizzano marcatori proprietari sul disco per indicare la quantità di spazio effettivamente occupata dai dati utente. Questi layout di disco non sono compatibili con IMAPI perché i marcatori proprietari non vengono riconosciuti all'esterno dell'applicazione per cui sono stati creati.

-   **Tipo di partizione definita dall'utente**

    IMAPI usa il **tipo di partizione** UDF di sola lettura nell'implementazione di multisessione su supporti riscibili. Gli sviluppatori di software di  masterizzazione di terze parti devono usare il tipo di partizione UDF di sola lettura per ottenere la Windows masterizzazione tramite IMAPI. Se si usa un altro tipo di partizione definita dall'utente, ad esempio **Riwritable,** IMAPI non può fornire supporto per la mastering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un disco multisessione](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




