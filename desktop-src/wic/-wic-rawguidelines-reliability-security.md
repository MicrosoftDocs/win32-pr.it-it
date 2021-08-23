---
description: Affidabilità e sicurezza
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Affidabilità e sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4704b84d09698fd6fabcf2d190050063ec3b3190904aa669fa78799c5d0158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441731"
---
# <a name="reliability-and-security"></a>Affidabilità e sicurezza

Poiché i codec Windows Imaging Component (WIC) verranno richiamati dalla shell di Windows e dal Raccolta foto, gli autori di codec devono fare tutto il possibile per garantire un livello elevato di affidabilità e sicurezza nei codec WIC.

La scrittura di codice affidabile dipende in gran parte da procedure di codifica ottimali, revisioni del codice efficaci e test approfonditi degli unit test e degli scenari. Inoltre, le linee guida seguenti consentono di garantire che il codec sia conforme ai criteri Windows Vista relativi all'affidabilità.

-   Abilitare l'annullamento di I/O.

    Gli autori di codec devono consentire all'utente finale di annullare qualsiasi operazione a esecuzione lunga. I codec WIC supportano questa operazione implementando IWICBitmapProgressNotification. In questo modo un'applicazione chiamante può specificare una funzione di callback che il codec deve chiamare a intervalli specificati per notificare al chiamante lo stato di avanzamento dell'operazione corrente. Quando un'applicazione restituisce ERROR CANCELLED dalla funzione di callback, il codec deve annullare qualsiasi operazione in corso e propagare il \_ valore HRESULT al chiamante. Ciò è particolarmente importante per i codec RAW, perché potrebbero essere necessari alcuni secondi per decodificare un'immagine RAW di dimensioni complete e le applicazioni necessitano di un modo per interrompere questa elaborazione.

-   Assicurarsi che il codice venga eseguito nell'ambito più piccolo necessario per eseguire la funzione.

    Gli autori di codec devono assicurarsi che il codec non consuma più risorse del necessario o abbia un ambito maggiore di quello richiesto. L'ambito di un codec in WIC è un singolo file di immagine. Il codec viene creato quando viene caricato un file di immagine e il codec viene rilasciato alla chiusura dell'immagine. Poiché WIC è una piattaforma estensibile basata su componenti, i codec WIC avranno carichi e scaricamenti sovrapposti e verranno avviati e arrestati all'interno dello stesso processo. Se l'infrastruttura sottostante di un codec richiede operazioni di avvio e arresto in un ambito più grande di una singola immagine, l'affidabilità sarà interrotta. I codec abilitati per WIC verranno usati da Windows Explorer, nonché da altre applicazioni. Pertanto, se un codec rimane caricato per la durata del processo, la memoria non verrà rilasciata in modo efficiente e un errore del codec potrebbe bloccarsi Windows Explorer e potenzialmente richiedere il riavvio del computer. Tenere presente che il codec verrà richiamato ogni volta che un'immagine viene visualizzata in anteprima per la prima volta in Windows Explorer: è essenziale che si tratta di un'operazione leggera.

-   Usare strumenti di analisi statica e dinamica del codice.

    -   Strumenti di analisi statica:

        PREfix: per rilevare gli errori in fase di compilazione.

        PREfast: per l'analisi del codice per la ricerca di bug.

    -   Strumenti di analisi dinamica:

        AppVerifier, che consente di rendere le applicazioni più resilienti simulando i problemi comuni del software reale.

-   Verificare tutti gli input nelle revisioni del codice.

    Tutti i parametri per i metodi esportati e tutti i dati dei file devono essere verificati attentamente per la validità e rifiutati in modo affidabile in caso di errore, per garantire la protezione da sovraccarichi e sottoeseguimenti del buffer, overflow e underflow aritmetici e tipi imprevisti.

-   Usare tecniche di file fuzzing per individuare potenziali arresti anomali e blocchi.

    Il fuzzing dei file è il processo di test del codec con input permutati casualmente.

    Esistono due forme di fuzzing dei file: fuzzing non indiretto (casuale) e fuzzing diretto. Il fuzzing non indiretto esegue un'operazione di capovolgimento casuale dei bit per verificare se l'input casuale può generare un arresto anomalo del codec. Il fuzzing diretto permuta l'input in base ad alcune informazioni sul formato di file. Ad esempio, se è presente un controllo di ridondanza del ciclo (CRC) all'offset di byte 32, la modifica dei byte senza aggiornare il CRC probabilmente non eserciterà la maggior parte dei percorsi di codice. In questo esempio, un fuzzer diretto dovrebbe correggere il CRC quando vengono modificati byte.

    Il set di immagini di input per il fuzzing dei file deve essere creato in modo che ogni combinazione di parametri che il decodificatore supporta sia testata. Ad esempio, se il decodificatore supporta file little-endian e big-endian e tre impostazioni di compressione, il set di input dell'immagine deve essere costituito da file little-endian di ogni impostazione di compressione e file big-endian per ogni impostazione di compressione. Questo approccio produce un set di immagini di input di grandi dimensioni, ma molto affidabile da testare. Anche se nessuna fotocamera produce ognuna delle combinazioni, ma il decodificatore supporta queste combinazioni teoriche, gli autori di codec devono eseguire il fuzz di questi input.

    La sicurezza può essere notevolmente migliorata eseguendo regolarmente test fuzz dei file di immagine durante lo sviluppo di codec. I codec devono essere sempre in grado di rilevare il danneggiamento del file di immagine e non riescono normalmente in caso di richiesta in formato non valido o di dati in formato non valido.

-   Stress del codice.

    Testare lo stress del codec eseguendolo continuamente in più processi simultanei, eseguendo tutte le operazioni supportate in tutte le sequenze possibili, su immagini di dimensioni variabili (incluse immagini di dimensioni molto grandi) da ogni fotocamera supportata.

-   Thread safety.

    A Windows 7, WIC richiede che RAW CODECs sia di tipo apartment COM "Both". Ciò significa che è necessario eseguire il blocco appropriato per gestire chiamanti e chiamanti tra apartment in scenari multi-thread. Gli oggetti all'interno di un apartment a thread multipli (MTA) possono essere chiamati contemporaneamente da un numero qualsiasi di thread all'interno dell'MTA, consentendo prestazioni migliori nei sistemi multi-core e in determinati scenari server. Inoltre, i CODICI WIC che si verificano all'interno di un MTA possono chiamare altri oggetti che si verificano all'interno dell'MTA senza il costo di marshalling associato alla chiamata tra thread che si trova in apartment STA diversi. Nella Windows 7, tutti i CODICI WIC inclusi sono stati aggiornati per supportare gli mtA, tra cui JPEG, TIFF, PNG, GIF, ICO e BMP. I CODICI di terze parti che non supportano gli MTA causeranno costi significativi in termini di prestazioni nelle applicazioni multithreading a causa del marshalling. L'abilitazione del supporto MTA richiede l'implementazione corretta della sincronizzazione nel CODEC di terze parti. L'implementazione esatta di queste tecniche di sincronizzazione non è in linea con l'ambito di questo documento. Di seguito è riportato un riferimento generale per la sincronizzazione di oggetti COM.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



