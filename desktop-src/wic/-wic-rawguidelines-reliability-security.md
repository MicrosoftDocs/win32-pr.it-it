---
description: Affidabilità e sicurezza
ms.assetid: 1cbfabce-3d56-4e23-b9a7-02369c67e392
title: Affidabilità e sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0f0e4a244de2c1463cdadb76162c18b041812b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315941"
---
# <a name="reliability-and-security"></a>Affidabilità e sicurezza

Poiché i codec di Windows Imaging Component (WIC) verranno richiamati dalla shell di Windows e dalla raccolta foto, gli autori di codec dovranno eseguire ogni sforzo per garantire un elevato livello di affidabilità e sicurezza nei propri codec WIC.

La scrittura di codice affidabile in gran parte dipende da procedure di codifica valide, revisioni del codice efficaci e test completi di unit test e test dello scenario. Inoltre, le linee guida seguenti consentiranno di garantire che il codec sia conforme ai criteri di Windows Vista relativi all'affidabilità.

-   Abilita l'annullamento I/O.

    Gli autori di codec devono consentire all'utente finale di annullare qualsiasi operazione a esecuzione prolungata. I codec WIC supportano questa operazione implementando IWICBitmapProgressNotification. Questo consente a un'applicazione chiamante di specificare una funzione di callback per il codec da chiamare a intervalli specificati per notificare al chiamante lo stato dell'operazione corrente. Quando un'applicazione restituisce un errore \_ annullato dalla funzione di callback, il codec deve annullare qualsiasi operazione in corso e propagare di nuovo HRESULT al chiamante. Questa operazione è particolarmente importante per i codec non ELABORAti, perché potrebbero essere necessari alcuni secondi per decodificare un'immagine non ELABORAta di dimensioni complete e le applicazioni necessitano di un modo per interrompere l'elaborazione.

-   Verificare che il codice venga eseguito nell'ambito più piccolo necessario per eseguire la relativa funzione.

    Gli autori di codec devono assicurarsi che il codec non utilizzi più risorse del necessario o abbia un ambito maggiore di quello necessario. L'ambito di un codec in WIC è un singolo file di immagine; il codec viene creato quando viene caricato un file di immagine e il codec viene rilasciato quando l'immagine viene chiusa. Poiché WIC è una piattaforma estensibile basata su componenti, i codec WIC avranno carichi e Scaricamenti sovrapposti e verranno avviati e arrestati, tutti all'interno dello stesso processo. Se l'infrastruttura sottostante di un codec richiede operazioni di avvio e arresto in un ambito più grande di una singola immagine, l'affidabilità sarà interessata. I codec abilitati per WIC verranno utilizzati da Esplora risorse, nonché da altre applicazioni. Se pertanto un codec rimane caricato per tutta la durata del processo, la memoria non verrà rilasciata in modo efficiente e un errore del codec potrebbe bloccare Esplora risorse e potenzialmente richiedere il riavvio del computer. Tenere presente che il codec verrà richiamato ogni volta che un'immagine viene visualizzata per la prima volta in Esplora risorse: è essenziale che questa sia un'operazione semplice.

-   Usare gli strumenti di analisi del codice statico e dinamico.

    -   Strumenti di analisi statica:

        Prefisso: per il rilevamento degli errori in fase di compilazione.

        PREfast: per l'analisi del codice per i bug.

    -   Strumenti di analisi dinamica:

        AppVerifier: consente di rendere le applicazioni più resilienti simulando problemi comuni del software reale.

-   Verificare tutti gli input nelle revisioni del codice.

    Tutti i parametri per i metodi esportati e tutti i dati dei file devono essere verificati con attenzione e rifiutati in modo affidabile in caso di errori, per proteggersi da sovraccarichi del buffer e sottoesecuzioni, overflow aritmetici e sottoflussi e tipi imprevisti.

-   Usare tecniche di fuzzing di file per individuare potenziali arresti anomali e blocchi.

    Il fuzzing dei file è il processo di test del codec con input permutati in modo casuale.

    Esistono due forme di fuzzing dei file: fuzzing non indirizzato (casuale) e fuzzing diretto. Il fuzzing non diretto esegue un capovolgimento casuale dei bit per verificare se l'input casuale può causare l'arresto anomalo del codec. Il fuzzing diretto permuta l'input in base a una certa conoscenza del formato di file. Se, ad esempio, è presente un controllo di ridondanza del ciclo (CRC) a offset di byte 32, la modifica di qualsiasi byte senza aggiornare il CRC probabilmente non eserciterà la maggior parte dei percorsi di codepath. In questo esempio, un fuzzer diretto deve correggere il CRC quando vengono modificati tutti i byte.

    Il set di input di immagini per il fuzzing dei file deve essere creato in modo che ogni combinazione di parametri supportata dal decodificatore venga testata. Se, ad esempio, il decodificatore supporta file Little e Big-Endian e tre impostazioni di compressione, il set di input dell'immagine deve essere costituito da file Little-Endian di ogni impostazione di compressione e file big-endian per ogni impostazione di compressione. Questo approccio produrrà un set di immagini di input di grandi dimensioni, ma molto affidabili, da testare. Anche se nessuna fotocamera produce ognuna delle combinazioni, ma il decodificatore supporta queste combinazioni teoriche, gli autori di codec dovrebbero fuzzare questi input.

    La sicurezza può essere migliorata mediante l'esecuzione regolare di test fuzzy dei file di immagine durante lo sviluppo di codec. I codec devono essere sempre in grado di rilevare il danneggiamento dei file di immagine e non vengono eseguiti normalmente in caso di una richiesta in formato non valido o di dati in formato non valido.

-   Evidenziare il codice.

    Sottoporre a test il codec eseguendolo continuamente in più processi simultanei, eseguendo tutte le operazioni supportate in tutte le sequenze possibili, su immagini di dimensioni variabili (incluse immagini di grandi dimensioni) da ogni fotocamera supportata.

-   Thread safety.

    A partire da Windows 7, per WIC è necessario che i CODEC non ELABORAti siano di tipo apartment COM "both". Ciò significa che è necessario eseguire il blocco appropriato per gestire i chiamanti e i chiamanti tra più Apartment negli scenari multithread. Gli oggetti all'interno di un Apartment a thread multipli (MTA) possono essere chiamati simultaneamente da un numero qualsiasi di thread all'interno dell'MTA, consentendo prestazioni migliori nei sistemi multicore e in alcuni scenari server. Inoltre, i CODEC WIC che risiedono all'interno di un MTA possono chiamare altri oggetti che risiedono all'interno dell'MTA senza il costo di marshalling associato alla chiamata tra thread che si trovano in diversi apartment STA. In Windows 7, tutti i CODEC WIC inclusi sono stati aggiornati per supportare gli MTA, tra cui JPEG, TIFF, PNG, GIF, ICO e BMP. i CODEC di terze parti che non supportano gli MTA provocheranno costi significativi in termini di prestazioni nelle applicazioni multithread a causa del marshalling. Per abilitare il supporto MTA, è necessario implementare una corretta sincronizzazione nel CODEC di terze parti. L'implementazione esatta di queste tecniche di sincronizzazione esula dall'ambito di questo documento. Di seguito è riportato un riferimento generale per la sincronizzazione di oggetti COM.

    https://msdn.microsoft.com/library/ms809971.aspx

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida per WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



