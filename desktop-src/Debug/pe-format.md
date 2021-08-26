---
description: Questa specifica descrive la struttura dei file eseguibili (immagine) e dei file oggetto nella Windows di sistemi operativi. Questi file sono denominati file eseguibili portabili (PE) e coff (Common Object File Format), rispettivamente.
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: Formato PE
ms.topic: article
ms.date: 03/31/2021
ms.custom: contperf-fy21q1
ms.openlocfilehash: f20431f7f56c64d5d430c9992da72ea4331cbf21
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812200"
---
# <a name="pe-format"></a>Formato PE

Questa specifica descrive la struttura dei file eseguibili (immagine) e dei file oggetto nella Windows di sistemi operativi. Questi file sono denominati file eseguibili portabili (PE) e coff (Common Object File Format), rispettivamente.

> [!Note]  
> Questo documento viene fornito per facilitare lo sviluppo di strumenti e applicazioni per Windows, ma non è garantito come una specifica completa a tutti gli aspetti. Microsoft si riserva il diritto di modificare questo documento senza preavviso.

Questa revisione di Microsoft Portable Executable e Common Object File Format Specification sostituisce tutte le revisioni precedenti di questa specifica.

## <a name="general-concepts"></a>Concetti generali

Questo documento specifica la struttura dei file eseguibili (immagine) e dei file oggetto nella famiglia di Windows microsoft. Questi file sono denominati file eseguibili portabili (PE) e coff (Common Object File Format), rispettivamente. Il nome "Eseguibile portabile" si riferisce al fatto che il formato non è specifico dell'architettura.

Alcuni concetti presenti in questa specifica sono descritti nella tabella seguente:

| Nome                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| certificato dell'attributo <br/> | Certificato utilizzato per associare istruzioni verificabili a un'immagine. A un file è possibile associare diverse istruzioni verificabili. una delle più utili è un'istruzione di un produttore di software che indica il digest del messaggio dell'immagine. Un digest del messaggio è simile a un checksum, ad eccezione del fatto che è estremamente difficile da forgiare. Pertanto, è molto difficile modificare un file in modo che abbia lo stesso digest del messaggio del file originale. L'istruzione può essere verificata dal produttore usando schemi di crittografia a chiave pubblica o privata. Questo documento descrive i dettagli sui certificati di attributo diversi da per consentire l'inserimento nei file di immagine. <br/> |
| timestamp di data/ora <br/>       | Timbro usato per scopi diversi in diverse posizioni in un file PE o COFF. Nella maggior parte dei casi, il formato di ogni timbro è lo stesso usato dalle funzioni di tempo nella libreria di runtime C. Per le eccezioni, vedere il descripton di IMAGE \_ DEBUG \_ TYPE \_ REPRO in Tipo di [debug](#debug-type). Se il valore del timbro è 0 o 0xFFFFFFFF, non rappresenta un timestamp di data/ora reale o significativo. <br/>                                                                                                                                                                                                                                                                                                                                            |
| puntatore di file <br/>          | Percorso di un elemento all'interno del file stesso, prima di essere elaborato dal linker (nel caso di file oggetto) o dal caricatore (nel caso dei file di immagine). In altre parole, si tratta di una posizione all'interno del file archiviato su disco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| linker <br/>                | Riferimento al linker fornito con Microsoft Visual Studio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| file oggetto <br/>           | File fornito come input per il linker. Il linker produce un file di immagine, che a sua volta viene usato come input dal caricatore. Il termine "file oggetto" non implica necessariamente alcuna connessione alla programmazione orientata a oggetti. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| riservato, deve essere 0 <br/>   | Descrizione di un campo che indica che il valore del campo deve essere zero per i generatori e che i consumer devono ignorare il campo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indirizzo virtuale relativo (RVA) <br/>                   | In un file di immagine si tratta dell'indirizzo di un elemento dopo che è stato caricato in memoria, con l'indirizzo di base del file di immagine sottratto da esso. L'RVA di un elemento è quasi sempre diversa dalla posizione all'interno del file su disco (puntatore file). <br/> In un file oggetto un'RVA è meno significativa perché i percorsi di memoria non sono assegnati. In questo caso, un'RVA è un indirizzo all'interno di una sezione (descritta più avanti in questa tabella), a cui viene successivamente applicata una rilocazione durante il collegamento. Per semplicità, un compilatore deve semplicemente impostare la prima RVA in ogni sezione su zero. <br/>                                                                                                                                         |
| section <br/>               | Unità di base del codice o dei dati all'interno di un file PE o COFF. Ad esempio, tutto il codice in un file oggetto può essere combinato all'interno di una singola sezione o (a seconda del comportamento del compilatore) ogni funzione può occupare la propria sezione. Con altre sezioni, il sovraccarico dei file è maggiore, ma il linker è in grado di collegarsi nel codice in modo più selettivo. Una sezione è simile a un segmento nell'architettura Intel 8086. Tutti i dati non elaborati in una sezione devono essere caricati in modo contiguo. Inoltre, un file di immagine può contenere diverse sezioni, ad esempio tls o reloc , che hanno scopi speciali. <br/>                                                                                                                                                                      |
| Indirizzo virtuale (VA) <br/>                    | Uguale a RVA, ad eccezione del fatto che l'indirizzo di base del file di immagine non viene sottratto. L'indirizzo viene chiamato va perché Windows uno spazio va distinto per ogni processo, indipendentemente dalla memoria fisica. Per quasi tutti gli scopi, un'istanza di va deve essere considerata solo un indirizzo. Un va va non è prevedibile come un'RVA perché il caricatore potrebbe non caricare l'immagine nella posizione preferita. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Panoramica

L'elenco seguente descrive il formato eseguibile Microsoft PE, con la base dell'intestazione dell'immagine nella parte superiore. La sezione dall'intestazione EXE compatibile MS-DOS 2.0 alla sezione inutilizzata subito prima dell'intestazione PE è la sezione MS-DOS 2.0 e viene usata solo per la compatibilità CON MS-DOS.

-   Intestazione EXE compatibile con MS-DOS 2.0
-   unused
-   Identificatore OEM

    Informazioni OEM

    Offset all'intestazione PE

-   MS-DOS 2.0 Stub Program and Relocation Table

-   unused

-   Intestazione PE (allineata sul limite a 8 byte)

-   Intestazioni di sezione
-   Pagine immagine:

    importare informazioni

    esportare informazioni

    rilocazioni di base

    informazioni sulle risorse

L'elenco seguente descrive il formato del modulo oggetto COFF Microsoft:

-   Intestazione COFF Microsoft
-   Intestazioni di sezione
-   Dati non elaborati:

    codice

    data

    informazioni di debug

    Rilocazioni

## <a name="file-headers"></a>Intestazioni di file

- [Stub MS-DOS (solo immagine)](#ms-dos-stub-image-only)
- [Firma (solo immagine)](#signature-image-only)
- [Intestazione del file COFF (oggetto e immagine)](#coff-file-header-object-and-image)
  - [Tipi di computer](#machine-types)
  - [Caratteristiche](#characteristics)
- [Intestazione facoltativa (solo immagine)](#optional-header-image-only)
  - [Campi standard dell'intestazione facoltativi (solo immagine)](#optional-header-standard-fields-image-only)
  - [Intestazione facoltativa Windows-Specific campi (solo immagine)](#optional-header-windows-specific-fields-image-only)
  - [Directory dei dati di intestazione facoltative (solo immagine)](#optional-header-data-directories-image-only)

L'intestazione del file PE è costituita da uno stub Microsoft MS-DOS, la firma PE, l'intestazione del file COFF e un'intestazione facoltativa. Un'intestazione del file oggetto COFF è costituita da un'intestazione di file COFF e da un'intestazione facoltativa. In entrambi i casi, le intestazioni di file sono seguite immediatamente dalle intestazioni di sezione.

### <a name="ms-dos-stub-image-only"></a>Stub MS-DOS (solo immagine)

Lo stub MS-DOS è un'applicazione valida che viene eseguita in MS-DOS. Viene posizionato nella parte anteriore dell'immagine EXE. Il linker inserisce qui uno stub predefinito, che stampa il messaggio "Questo programma non può essere eseguito in modalità DOS" quando l'immagine viene eseguita in MS-DOS. L'utente può specificare uno stub diverso usando l'opzione del linker /STUB.

Nella posizione 0x3c, lo stub ha l'offset del file per la firma PE. Queste informazioni consentono Windows eseguire correttamente il file di immagine, anche se dispone di uno stub MS-DOS. Questo offset di file viene posizionato nella posizione 0x3c durante il collegamento.

### <a name="signature-image-only"></a>Firma (solo immagine)

Dopo lo stub MS-DOS, in corrispondenza dell'offset del file specificato in corrispondenza dell'offset 0x3c, è una firma a 4 byte che identifica il file come file di immagine in formato PE. Questa firma è "PE \\ 0 \\ 0" (le lettere "P" ed "E" seguite da due byte Null).

### <a name="coff-file-header-object-and-image"></a>Intestazione del file COFF (oggetto e immagine)

All'inizio di un file oggetto, o immediatamente dopo la firma di un file di immagine, è un'intestazione di file COFF standard nel formato seguente. Si noti che Windows caricatore limita il numero di sezioni a 96.

| Offset         | Dimensione          | Campo                            | Descrizione                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Computer <br/>              | Numero che identifica il tipo di computer di destinazione. Per altre informazioni, vedere [Tipi di computer.](#machine-types) <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | NumberOfSections <br/>     | Numero di sezioni. Indica la dimensione della tabella della sezione che segue immediatamente le intestazioni. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | I 32 bit bassi del numero di secondi trascorsi dalle 00.00 del 1° gennaio 1970 (un valore t in fase di esecuzione C), che indica quando è stato creato il \_ file. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | PointerToSymbolTable <br/> | Offset del file della tabella dei simboli COFF oppure zero se non è presente alcuna tabella dei simboli COFF. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                                                                           |
| 12 <br/> | 4 <br/> | NumberOfSymbols <br/>      | Numero di voci nella tabella dei simboli. Questi dati possono essere usati per individuare la tabella di stringhe che segue immediatamente la tabella dei simboli. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                        |
| 16 <br/> | 2 <br/> | SizeOfOptionalHeader <br/> | Dimensione dell'intestazione facoltativa, necessaria per i file eseguibili, ma non per i file oggetto. Questo valore deve essere zero per file oggetto. Per una descrizione del formato dell'intestazione, vedere [Intestazione facoltativa (solo immagine).](#optional-header-image-only) <br/> |
| 18 <br/> | 2 <br/> | Caratteristiche <br/>      | Flag che indicano gli attributi del file. Per valori di flag specifici, vedere [Caratteristiche.](#characteristics) <br/>                                                                                                                               |

#### <a name="machine-types"></a>Tipi di computer

Il campo Computer ha uno dei valori seguenti, che specificano il tipo di CPU. Un file di immagine può essere eseguito solo nel computer specificato o in un sistema che emula il computer specificato.

| Costante                                    | Valore              | Descrizione                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| COMPUTER \_ DEL FILE DI IMMAGINE \_ \_ SCONOSCIUTO <br/>   | 0x0 <br/>    | Si presuppone che il contenuto di questo campo sia applicabile a qualsiasi tipo di computer <br/> |
| IMAGE \_ FILE \_ MACHINE \_ AM33 <br/>      | 0x1d3 <br/>  | Matsushita AM33 <br/>                                                             |
| IMAGE \_ FILE \_ MACHINE \_ AMD64 <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| IMAGE \_ FILE \_ MACHINE \_ ARM <br/>       | 0x1c0 <br/>  | Arm little endian <br/>                                                           |
| IMAGE \_ FILE \_ MACHINE \_ ARM64 <br/>     | 0xaa64 <br/> | Arm64 little endian <br/>                                                         |
| IMAGE \_ FILE \_ MACHINE \_ ARMNT <br/>     | 0x1c4 <br/>  | Arm Thumb-2 little endian <br/>                                                   |
| IMAGE \_ FILE \_ MACHINE \_ EBC <br/>       | 0xebc <br/>  | Codice byte EFI <br/>                                                               |
| IMAGE \_ FILE \_ MACHINE \_ I386 <br/>      | 0x14c <br/>  | Processori Intel 386 o versioni successive e processori compatibili <br/>                     |
| IMAGE \_ FILE \_ MACHINE \_ IA64 <br/>      | 0x200 <br/>  | Famiglia di processori Intel Itanium <br/>                                              |
| IMAGE \_ FILE \_ MACHINE \_ M32R <br/>      | 0x9041 <br/> | Mitsubishi M32R little endian <br/>                                               |
| IMAGE \_ FILE \_ MACHINE \_ MIPS16 <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| IMAGE \_ FILE \_ MACHINE \_ MIPSFPU <br/>   | 0x366 <br/>  | MIPS con FPU <br/>                                                               |
| IMAGE \_ FILE \_ MACHINE \_ MIPSFPU16 <br/> | 0x466 <br/>  | MIPS16 con FPU <br/>                                                             |
| IMAGE \_ FILE \_ MACHINE \_ POWERPC <br/>   | 0x1f0 <br/>  | Power PC little endian <br/>                                                      |
| IMAGE \_ FILE \_ MACHINE \_ POWERPCFP <br/> | 0x1f1 <br/>  | Power PC con supporto a virgola mobile <br/>                                        |
| IMAGE \_ FILE \_ MACHINE \_ R4000 <br/>     | 0x166 <br/>  | MiPS little endian <br/>                                                          |
| FILE \_ DI \_ IMMAGINE \_ RISCV32 <br/>   | 0x5032 <br/> | Spazio indirizzi RISC-V a 32 bit <br/>                                                 |
| FILE \_ DI \_ IMMAGINE \_ RISCV64 <br/>   | 0x5064 <br/> | Spazio indirizzi RISC-V a 64 bit <br/>                                                 |
| IMAGE \_ FILE \_ MACHINE \_ RISCV128 <br/>  | 0x5128 <br/> | Spazio indirizzi RISC-V a 128 bit <br/>                                                |
| IMAGE \_ FILE \_ MACHINE \_ SH3 <br/>       | 0x1a2 <br/>  | Hitachi SH3 <br/>                                                                 |
| IMAGE \_ FILE \_ MACHINE \_ SH3DSP <br/>    | 0x1a3 <br/>  | Hitachi SH3 DSP <br/>                                                             |
| IMAGE \_ FILE \_ MACHINE \_ SH4 <br/>       | 0x1a6 <br/>  | Hitachi SH4 <br/>                                                                 |
| IMAGE \_ FILE \_ MACHINE \_ SH5 <br/>       | 0x1a8 <br/>  | Hitachi SH5 <br/>                                                                 |
| IMAGE \_ FILE \_ MACHINE \_ THUMB <br/>     | 0x1c2 <br/>  | Thumb <br/>                                                                       |
| IMAGE \_ FILE \_ MACHINE \_ WCEMIPSV2 <br/> | 0x169 <br/>  | MIPS little-endian WCE v2 <br/>                                                   |

#### <a name="characteristics"></a>Caratteristiche

Il campo Caratteristiche contiene flag che indicano gli attributi dell'oggetto o del file di immagine. Attualmente sono definiti i flag seguenti:

| Flag                                                 | valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RILOCAZIONE DEI FILE DI IMMAGINE CON \_ \_ STRIPED <br/>            | 0x0001 <br/> | Solo immagine, Windows CE e Microsoft Windows NT e versioni successive. Ciò indica che il file non contiene rilocazioni di base e pertanto deve essere caricato nell'indirizzo di base preferito. Se l'indirizzo di base non è disponibile, il caricatore segnala un errore. Il comportamento predefinito del linker è lo striping delle rilocazioni di base da file eseguibili (EXE). <br/> |
| IMMAGINE \_ ESEGUIBILE DEL FILE \_ DI \_ IMMAGINE <br/>           | 0x0002 <br/> | Solo immagine. Ciò indica che il file di immagine è valido e può essere eseguito. Se questo flag non è impostato, indica un errore del linker. <br/>                                                                                                                                                                                                                          |
| RIGA \_ DEL FILE DI IMMAGINE CON NUMERO DI RIGHE \_ \_ \_ STRIPED <br/>        | 0x0004 <br/> | I numeri di riga COFF sono stati rimossi. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                                                                                       |
| SIMBOLI \_ LOCALI DEL FILE DI IMMAGINE CON \_ \_ \_ STRIPED <br/>       | 0x0008 <br/> | Le voci della tabella dei simboli COFF per i simboli locali sono state rimosse. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                                                             |
| FILE DI \_ IMMAGINE \_ AGGRESSIVE \_ WS \_ TRIM <br/>        | 0x0010 <br/> | Obsoleta. Tagliare in modo aggressivo working set. Questo flag è deprecato per Windows 2000 e versioni successive e deve essere zero. <br/>                                                                                                                                                                                                                                          |
| FILE DI \_ IMMAGINE \_ CON INFORMAZIONI \_ SULL'INDIRIZZO DI GRANDI \_ DIMENSIONI <br/>      | 0x0020 <br/> | L'applicazione può > indirizzi da 2 GB. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Questo flag è riservato per un uso futuro. <br/>                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ FILE \_ BYTES \_ REVERSED \_ LO <br/>         | 0x0080 <br/> | Little Endian: il bit meno significativo (LSB) precede il bit più significativo (MSB) in memoria. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                          |
| IMAGE \_ FILE \_ 32BIT \_ MACHINE <br/>              | 0x0100 <br/> | Il computer è basato su un'architettura a 32 bit. <br/>                                                                                                                                                                                                                                                                                                        |
| DEBUG \_ DEL FILE DI IMMAGINE CON \_ \_ STRIPED <br/>             | 0x0200 <br/> | Le informazioni di debug vengono rimosse dal file di immagine. <br/>                                                                                                                                                                                                                                                                                                  |
| ESECUZIONE \_ \_ RIMOVIBILE DEL FILE \_ DI IMMAGINE \_ DALLO \_ SCAMBIO <br/> | 0x0400 <br/> | Se l'immagine si trova su supporti rimovibili, caricarla completamente e copiarla nel file di scambio. <br/>                                                                                                                                                                                                                                                                        |
| FILE \_ DI IMMAGINE NET RUN FROM \_ \_ \_ \_ SWAP <br/>        | 0x0800 <br/> | Se l'immagine si trova su un supporto di rete, caricarla completamente e copiarla nel file di scambio. <br/>                                                                                                                                                                                                                                                                          |
| FILE \_ \_ SYSTEM DI IMMAGINI <br/>                      | 0x1000 <br/> | Il file di immagine è un file di sistema, non un programma utente. <br/>                                                                                                                                                                                                                                                                                                   |
| \_DLL DEL FILE DI \_ IMMAGINE <br/>                         | 0x2000 <br/> | Il file di immagine è una libreria a collegamento dinamico (DLL). Tali file sono considerati file eseguibili per quasi tutti gli scopi, anche se non possono essere eseguiti direttamente. <br/>                                                                                                                                                                                              |
| IMAGE \_ FILE \_ UP \_ SYSTEM \_ ONLY <br/>            | 0x4000 <br/> | Il file deve essere eseguito solo in un computer uniprocessore. <br/>                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ FILE \_ BYTES \_ REVERSED \_ HI <br/>         | 0x8000 <br/> | Big endian: il file MSB precede l'LSB in memoria. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>Intestazione facoltativa (solo immagine)

Ogni file di immagine ha un'intestazione facoltativa che fornisce informazioni al caricatore. Questa intestazione è facoltativa nel senso che alcuni file (in particolare, i file oggetto) non lo hanno. Per i file di immagine, questa intestazione è obbligatoria. Un file oggetto può avere un'intestazione facoltativa, ma in genere questa intestazione non ha alcuna funzione in un file oggetto se non per aumentarne le dimensioni.

Si noti che le dimensioni dell'intestazione facoltativa non sono fisse. Il **campo SizeOfOptionalHeader** nell'intestazione COFF deve essere usato per convalidare che un probe nel file per una determinata directory di dati non va oltre **SizeOfOptionalHeader.** Per altre informazioni, vedere [Intestazione file COFF (oggetto e immagine).](#coff-file-header-object-and-image)

Il **campo NumberOfRvaAndSizes dell'intestazione** facoltativa deve essere usato anche per assicurarsi che nessun probe per una determinata voce della directory di dati eserciti l'intestazione facoltativa. Inoltre, è importante convalidare il numero magic di intestazione facoltativo per la compatibilità del formato.

Il numero magic di intestazione facoltativo determina se un'immagine è un eseguibile PE32 o PE32+.

| Numero magic      | Formato PE         |
|-------------------|-------------------|
| 0x10b <br/> | PE32 <br/>  |
| 0x20b <br/> | PE32+ <br/> |

Le immagini PE32+ consentono uno spazio indirizzi a 64 bit limitando al tempo stesso le dimensioni dell'immagine a 2 gigabyte. Altre modifiche PE32+ sono descritte nelle rispettive sezioni.

L'intestazione facoltativa stessa ha tre parti principali.

| Offset (PE32/PE32+) | Dimensioni (PE32/PE32+)    | Parte dell'intestazione                         | Descrizione                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Campi standard <br/>         | Campi definiti per tutte le implementazioni di COFF, inclusi i UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | Windows specifici dei campi <br/> | Campi aggiuntivi per supportare funzionalità specifiche di Windows (ad esempio, sottosistemi). <br/>                                                                              |
| 96/112 <br/>  | Variabile <br/> | Directory dati <br/>        | Coppie indirizzo/dimensione per tabelle speciali trovate nel file di immagine e usate dal sistema operativo, ad esempio la tabella di importazione e la tabella di esportazione. <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Campi standard dell'intestazione facoltativi (solo immagine)

I primi otto campi dell'intestazione facoltativa sono campi standard definiti per ogni implementazione di COFF. Questi campi contengono informazioni generali utili per il caricamento e l'esecuzione di un file eseguibile. Rimangono invariati per il formato PE32+.

| Offset         | Dimensione          | Campo                               | Descrizione                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Magic <br/>                   | Intero senza segno che identifica lo stato del file di immagine. Il numero più comune è 0x10B, che lo identifica come un normale file eseguibile. 0x107 identifica come immagine ROM e 0x20B come eseguibile PE32+. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | MajorLinkerVersion <br/>      | Numero di versione principale del linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | MinorLinkerVersion <br/>      | Numero di versione secondaria del linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | SizeOfCode <br/>              | Dimensioni della sezione di codice (testo) o somma di tutte le sezioni di codice se sono presenti più sezioni. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | SizeOfInitializedData <br/>   | Dimensioni della sezione di dati inizializzati o somma di tutte queste sezioni se sono presenti più sezioni di dati. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | SizeOfUninitializedData <br/> | Le dimensioni della sezione di dati non inizializzati (BSS) o la somma di tutte queste sezioni se sono presenti più sezioni BSS. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | AddressOfEntryPoint <br/>     | Indirizzo del punto di ingresso relativo alla base dell'immagine quando il file eseguibile viene caricato in memoria. Per le immagini del programma, questo è l'indirizzo iniziale. Per i driver di dispositivo, questo è l'indirizzo della funzione di inizializzazione. Un punto di ingresso è facoltativo per le DLL. Quando non è presente alcun punto di ingresso, questo campo deve essere zero. <br/> |
| 20 <br/> | 4 <br/> | BaseOfCode <br/>              | Indirizzo relativo alla base dell'immagine della sezione di inizio del codice quando viene caricata in memoria. <br/>                                                                                                                                                                                                                    |

PE32 contiene questo campo aggiuntivo, assente in PE32+, dopo BaseOfCode.

| Offset         | Dimensione          | Campo                  | Descrizione                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | BaseOfData <br/> | Indirizzo relativo alla base dell'immagine della sezione di inizio dei dati quando viene caricata in memoria. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Campi di intestazione Windows-Specific facoltativi (solo immagine)

I 21 campi successivi sono un'estensione del formato di intestazione facoltativo COFF. Contengono informazioni aggiuntive richieste dal linker e dal caricatore in Windows.

| Offset (PE32/PE32+) | Dimensioni (PE32/PE32+) | Campo                                   | Descrizione                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | ImageBase <br/>                   | Indirizzo preferito del primo byte dell'immagine quando viene caricato in memoria. deve essere un multiplo di 64 K. Il valore predefinito per le DLL è 0x10000000. Il valore predefinito per Windows CE ES È 0x00010000. Il valore predefinito per Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 e Windows Me è 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | Allineamento (in byte) delle sezioni quando vengono caricate in memoria. Deve essere maggiore o uguale a FileAlignment. Il valore predefinito è la dimensione della pagina per l'architettura. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | Fattore di allineamento (in byte) usato per allineare i dati non elaborati delle sezioni nel file di immagine. Il valore deve essere una potenza di 2 compresa tra 512 e 64 K inclusi. Il valore predefinito è 512. Se SectionAlignment è minore delle dimensioni di pagina dell'architettura, FileAlignment deve corrispondere a SectionAlignment. <br/> |
| 40/40 <br/>    | 2 <br/>      | MajorOperatingSystemVersion <br/> | Numero di versione principale del sistema operativo richiesto. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | MinorOperatingSystemVersion <br/> | Numero di versione secondaria del sistema operativo richiesto. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | MajorImageVersion <br/>           | Numero di versione principale dell'immagine. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | MinorImageVersion <br/>           | Numero di versione secondaria dell'immagine. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | MajorSubsystemVersion <br/>       | Numero di versione principale del sottosistema. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | MinorSubsystemVersion <br/>       | Numero di versione secondaria del sottosistema. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Riservato, deve essere zero. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | SizeOfImage <br/>                 | Dimensioni (in byte) dell'immagine, incluse tutte le intestazioni, quando l'immagine viene caricata in memoria. Deve essere un multiplo di SectionAlignment. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | SizeOfHeaders <br/>               | Dimensioni combinate di uno stub MS-DOS, di un'intestazione PE e di intestazioni di sezione arrotondate a un multiplo di FileAlignment. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | Checksum <br/>                    | Checksum del file di immagine. L'algoritmo per il calcolo del checksum viene incorporato in IMAGHELP.DLL. In fase di caricamento viene verificata la convalida degli elementi seguenti: tutti i driver, qualsiasi DLL caricata in fase di avvio e qualsiasi DLL caricata in un processo Windows critico. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsystem <br/>                   | Sottosistema necessario per eseguire l'immagine. Per altre informazioni, vedere [Sottosistema Windows .](#windows-subsystem) <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Per altre informazioni, vedere [Caratteristiche della DLL](#dll-characteristics) più avanti in questa specifica. <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | Dimensioni dello stack da riservare. Viene eseguito il commit solo di SizeOfStackCommit. il resto viene reso disponibile una pagina alla volta fino a quando non viene raggiunta la dimensione di riserva. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | SizeOfStackCommit <br/>           | Dimensioni dello stack di cui eseguire il commit. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | SizeOfHeapReserve <br/>           | Dimensioni dello spazio dell'heap locale da riservare. Viene eseguito il commit solo di SizeOfHeapCommit. il resto viene reso disponibile una pagina alla volta fino a quando non viene raggiunta la dimensione di riserva. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | SizeOfHeapCommit <br/>            | Dimensioni dello spazio dell'heap locale di cui eseguire il commit. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | LoaderFlags <br/>                 | Riservato, deve essere zero. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | NumberOfRvaAndSizes <br/>         | Numero di voci della directory di dati nel resto dell'intestazione facoltativa. Ognuna descrive una posizione e una dimensione. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Windows Sottosistema

I valori seguenti definiti per il campo Subsystem dell'intestazione facoltativa determinano quale sottosistema Windows (se presente) è necessario per eseguire l'immagine.

| Costante                                                  | Valore          | Descrizione                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| \_SOTTOSISTEMA \_ IMMAGINE SCONOSCIUTO <br/>                     | 0 <br/>  | Sottosistema sconosciuto <br/>                                 |
| \_SOTTOSISTEMA \_ IMMAGINE NATIVO <br/>                      | 1 <br/>  | Driver di dispositivo e processi Windows nativi <br/>          |
| INTERFACCIA \_ UTENTE GRAFICA DI WINDOWS DEL SOTTOSISTEMA \_ \_ IMMAGINE <br/>                | 2 <br/>  | Sottosistema Windows interfaccia utente grafica (GUI) <br/> |
| INTERFACCIA UTENTE \_ DI WINDOWS DEL \_ SOTTOSISTEMA \_ IMMAGINE <br/>                | 3 <br/>  | Sottosistema Windows carattere <br/>                      |
| INTERFACCIA \_ UTENTE DEL \_ SOTTOSISTEMA DI IMMAGINI \_ OS2 <br/>                    | 5 <br/>  | Sottosistema di caratteri OS/2 <br/>                         |
| \_SOTTOSISTEMA IMMAGINE \_ POSIX \_ CUI <br/>                  | 7 <br/>  | Sottosistema di caratteri Posix <br/>                        |
| \_SOTTOSISTEMA \_ IMMAGINE WINDOWS \_ NATIVO <br/>             | 8 <br/>  | Driver Win9x nativo <br/>                                  |
| IMMAGINE \_ SOTTOSISTEMA \_ WINDOWS CE \_ \_ GUI <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| APPLICAZIONE \_ \_ EFI DEL SOTTOSISTEMA \_ IMMAGINE <br/>            | 10 <br/> | Applicazione Extensible Firmware Interface (EFI) <br/>   |
| DRIVER \_ DEL SERVIZIO DI AVVIO \_ EFI DEL SOTTOSISTEMA \_ \_ \_ IMMAGINE <br/> | 11 <br/> | Un driver EFI con servizi di avvio <br/>                     |
| DRIVER \_ DI RUNTIME \_ EFI DEL SOTTOSISTEMA \_ \_ IMMAGINE <br/>       | 12 <br/> | Un driver EFI con servizi di run-time <br/>                 |
| IMMAGINE \_ SOTTOSISTEMA \_ EFI \_ ROM <br/>                    | 13 <br/> | Immagine ROM EFI <br/>                                     |
| \_SOTTOSISTEMA \_ IMMAGINE XBOX <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| \_SOTTOSISTEMA IMMAGINE \_ APPLICAZIONE DI \_ AVVIO WINDOWS \_ <br/>  | 16 <br/> | Windows'applicazione di avvio. <br/>                            |

##### <a name="dll-characteristics"></a>Caratteristiche dll

I valori seguenti sono definiti per il campo DllCharacteristics dell'intestazione facoltativa.

| Costante                                                             | Valore              | Descrizione                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Riservato, deve essere zero. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Riservato, deve essere zero. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Riservato, deve essere zero. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Riservato, deve essere zero. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ HIGH \_ ENTROPY \_ VA <br/>             | 0x0020 <br/> | L'immagine può gestire uno spazio di indirizzi virtuali a 64 bit con entropia elevata. <br/>                               |
| \_DLLCHARACTERISTICS IMMAGINE\_ <br/> BASE \_ DINAMICA <br/>    | 0x0040 <br/> | La DLL può essere rilocata in fase di caricamento. <br/>                                                          |
| \_DLLCHARACTERISTICS IMMAGINE\_ <br/> FORZARE \_ L'INTEGRITÀ <br/> | 0x0080 <br/> | Vengono applicati i controlli di integrità del codice. <br/>                                                         |
| \_DLLCHARACTERISTICS IMMAGINE\_ <br/> NX \_ COMPAT <br/>       | 0x0100 <br/> | L'immagine è compatibile con NX. <br/>                                                                     |
| \_DLLCHARACTERISTICS IMMAGINE \_ SENZA \_ ISOLAMENTO <br/>                | 0x0200 <br/> | Riconoscere l'isolamento, ma non isolare l'immagine. <br/>                                              |
| \_DLLCHARACTERISTICS \_ IMMAGINE NO \_ SEH <br/>                      | 0x0400 <br/> | Non usa la gestione delle eccezioni strutturate (edizione Standard). In questa edizione Standard non può essere chiamato alcun gestore. <br/> |
| IMAGE \_ DLLCHARACTERISTICS \_ NO \_ BIND <br/>                     | 0x0800 <br/> | Non associare l'immagine. <br/>                                                                      |
| IMAGE \_ DLLCHARACTERISTICS \_ APPCONTAINER <br/>                  | 0x1000 <br/> | L'immagine deve essere eseguita in un AppContainer. <br/>                                                      |
| DRIVER \_ WDM DLLCHARACTERISTICS \_ \_ IMMAGINE <br/>                  | 0x2000 <br/> | Un driver WDM. <br/>                                                                               |
| IMMAGINE \_ DLLCHARACTERISTICS \_ GUARD \_ CF <br/>                     | 0x4000 <br/> | Image supporta Control Flow Guard. <br/>                                                          |
| IMMAGINE \_ DLLCHARACTERISTICS IN GRADO DI RICONOSCERE \_ TERMINAL \_ SERVER \_ <br/>      | 0x8000 <br/> | In grado di riconoscere Terminal Server. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Directory dei dati di intestazione facoltative (solo immagine)

Ogni directory di dati fornisce l'indirizzo e le dimensioni di una tabella o di una stringa Windows utilizzata. Queste voci della directory di dati vengono tutte caricate in memoria in modo che il sistema possa usarle in fase di esecuzione. Una directory di dati è un campo a 8 byte con la dichiarazione seguente:

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

Il primo campo, VirtualAddress, è in realtà l'RVA della tabella. L'RVA è l'indirizzo della tabella relativo all'indirizzo di base dell'immagine quando la tabella viene caricata. Il secondo campo fornisce le dimensioni in byte. Le directory dei dati, che formano l'ultima parte dell'intestazione facoltativa, sono elencate nella tabella seguente.

Si noti che il numero di directory non è fisso. Prima di cercare una directory specifica, controllare il campo NumberOfRvaAndSizes nell'intestazione facoltativa.

Inoltre, non presupporre che gli oggetti RVA in questa tabella puntino all'inizio di una sezione o che le sezioni che contengono tabelle specifiche hanno nomi specifici.

| Offset (PE/PE32+)   | Dimensione          | Campo                               | Descrizione                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Esporta tabella <br/>            | Indirizzo e dimensioni della tabella di esportazione. Per altre informazioni, vedere [la sezione .edata (solo immagine).](#the-edata-section-image-only) <br/>                                                |
| 104/120 <br/> | 8 <br/> | Importa tabella <br/>            | Indirizzo e dimensioni della tabella di importazione. Per altre informazioni, vedere [la sezione .idata.](#the-idata-section)<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Tabella delle risorse <br/>          | Indirizzo e dimensioni della tabella delle risorse. Per altre informazioni, vedere [la sezione .rsrc.](#the-rsrc-section)<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Tabella delle eccezioni <br/>         | Indirizzo e dimensioni della tabella delle eccezioni. Per altre informazioni, vedere [la sezione .pdata.](#the-pdata-section) <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Tabella dei certificati <br/>       | Indirizzo e dimensioni della tabella del certificato dell'attributo. Per altre informazioni, vedere [Tabella dei certificati degli attributi (solo immagine).](#the-attribute-certificate-table-image-only) <br/> |
| 136/152 <br/> | 8 <br/> | Tabella di rilocazione di base <br/>   | Indirizzo e dimensioni della tabella di rilocazione di base. Per altre informazioni, vedere [la sezione .reloc (solo immagine).](#the-reloc-section-image-only)<br/>                                   |
| 144/160 <br/> | 8 <br/> | Debug <br/>                   | Indirizzo iniziale e dimensioni dei dati di debug. Per altre informazioni, vedere [la sezione .debug](#the-debug-section).<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Architettura <br/>            | Riservato, deve essere 0 <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | Ptr globale <br/>              | Valore RVA del valore da archiviare nel registro puntatore globale. Il membro size di questa struttura deve essere impostato su zero. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | Tabella TLS <br/>               | Indirizzo e dimensioni della tabella di archiviazione thread-local (TLS). Per altre informazioni, vedere [la sezione .tls.](#the-tls-section)<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Caricare la tabella di configurazione <br/>       | Indirizzo e dimensioni della tabella di configurazione del carico. Per altre informazioni, vedere [La struttura di configurazione del caricamento (solo immagine).](#the-load-configuration-structure-image-only)<br/>       |
| 184/200 <br/> | 8 <br/> | Importazione associata <br/>            | Indirizzo e dimensioni della tabella di importazione associata. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | Iat <br/>                     | Indirizzo e dimensioni della tabella degli indirizzi di importazione. Per altre informazioni, vedere [Importare una tabella indirizzi.](#import-address-table)<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Ritardare il descrittore di importazione <br/> | Indirizzo e dimensioni del descrittore di importazione ritardata. Per altre informazioni, vedere [Tabelle di importazione a caricamento ritardato (solo immagine).](#delay-load-import-tables-image-only)<br/>                    |
| 208/224 <br/> | 8 <br/> | Intestazione runtime CLR <br/>      | Indirizzo e dimensioni dell'intestazione del runtime CLR. Per altre informazioni, vedere [la sezione .cormeta (solo oggetto).](#the-cormeta-section-object-only)<br/>                                |
| 216/232 <br/> | 8 <br/> | Riservato, deve essere zero <br/>  |                                                                                                                                                                                      |

La voce Tabella certificati punta a una tabella di certificati di attributo. Questi certificati non vengono caricati in memoria come parte dell'immagine. Di conseguenza, il primo campo di questa voce, che in genere è un RVA, è invece un puntatore di file.

## <a name="section-table-section-headers"></a>Tabella delle sezioni (intestazioni di sezione)

- [Flag di sezione](#section-flags)
- [Sezioni raggruppate (solo oggetti)](#grouped-sections-object-only)

Ogni riga della tabella di sezione è, in effetti, un'intestazione di sezione. Questa tabella segue immediatamente l'intestazione facoltativa, se presente. Questo posizionamento è necessario perché l'intestazione del file non contiene un puntatore diretto alla tabella di sezioni. Al contrario, la posizione della tabella delle sezioni viene determinata calcolando la posizione del primo byte dopo le intestazioni. Assicurarsi di usare le dimensioni dell'intestazione facoltativa come specificato nell'intestazione del file.

Il numero di voci nella tabella delle sezioni viene specificato dal campo NumberOfSections nell'intestazione del file. Le voci nella tabella della sezione sono numerate a partire da uno (1). Le voci della sezione relativa al codice e alla memoria dei dati sono nell'ordine scelto dal linker.

In un file di immagine, le macchine virtuali per le sezioni devono essere assegnate dal linker in modo che siano in ordine crescente e adiacenti e devono essere un multiplo del valore SectionAlignment nell'intestazione facoltativa.

Ogni intestazione di sezione (voce della tabella di sezione) ha il formato seguente, per un totale di 40 byte per voce.



| Offset         | Dimensione          | Campo                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nome <br/>                 | Stringa con codifica UTF-8 a 8 byte con riempimento Null. Se la stringa è lunga esattamente 8 caratteri, non esiste alcun carattere Null di terminazione. Per i nomi più lunghi, questo campo contiene una barra (/) seguita da una rappresentazione ASCII di un numero decimale che rappresenta un offset nella tabella di stringhe. Le immagini eseguibili non usano una tabella di stringhe e non supportano nomi di sezione più lunghi di 8 caratteri. I nomi lunghi nei file oggetto vengono troncati se vengono generati in un file eseguibile. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | Dimensione totale della sezione quando viene caricata in memoria. Se questo valore è maggiore di SizeOfRawData, la sezione viene riempita con zero. Questo campo è valido solo per le immagini eseguibili e deve essere impostato su zero per i file oggetto. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | Per le immagini eseguibili, l'indirizzo del primo byte della sezione relativo alla base dell'immagine quando la sezione viene caricata in memoria. Per i file oggetto, questo campo è l'indirizzo del primo byte prima dell'applicazione della rilocazione. Per semplicità, i compilatori devono impostare questa proprietà su zero. In caso contrario, è un valore arbitrario sottratto dagli offset durante la rilocazione. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | SizeOfRawData <br/>        | Dimensioni della sezione (per i file oggetto) o dimensioni dei dati inizializzati su disco (per i file di immagine). Per le immagini eseguibili, deve essere un multiplo di FileAlignment dall'intestazione facoltativa. Se è minore di VirtualSize, il resto della sezione viene riempito con zero. Poiché il campo SizeOfRawData è arrotondato, ma il campo VirtualSize non lo è, è possibile che SizeOfRawData sia maggiore anche di VirtualSize. Quando una sezione contiene solo dati non inizializzati, questo campo deve essere zero. <br/> |
| 20 <br/> | 4 <br/> | PointerToRawData <br/>     | Puntatore del file alla prima pagina della sezione all'interno del file COFF. Per le immagini eseguibili, deve essere un multiplo di FileAlignment dall'intestazione facoltativa. Per i file oggetto, il valore deve essere allineato su un limite di 4 byte per ottenere prestazioni ottimali. Quando una sezione contiene solo dati non inizializzati, questo campo deve essere zero. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | PointerToRelocations <br/> | Puntatore del file all'inizio delle voci di rilocazione per la sezione. È impostato su zero per le immagini eseguibili o se non sono presenti rilocazioni. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | PointerToLinenumbers <br/> | Puntatore del file all'inizio delle voci relative ai numeri di riga per la sezione. Viene impostato su zero se non sono presenti numeri di riga COFF. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | NumberOfRelocations <br/>  | Numero di voci di rilocazione per la sezione. È impostato su zero per le immagini eseguibili. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | NumberOfLinenumbers <br/>  | Numero di voci di numeri di riga per la sezione. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Caratteristiche <br/>      | Flag che descrivono le caratteristiche della sezione. Per altre informazioni, vedere [Flag di sezione.](#section-flags)<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Flag di sezione

I flag di sezione nel campo Caratteristiche dell'intestazione di sezione indicano le caratteristiche della sezione.



| Flag                                              | valore                  | Descrizione                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ TYPE \_ NO \_ PAD <br/>             | 0x00000008 <br/> | La sezione non deve essere riempita fino al limite successivo. Questo flag è obsoleto e viene sostituito da IMAGE \_ SCN \_ ALIGN \_ 1BYTES. Questa opzione è valida solo per i file oggetto. <br/> |
|                                                   | 0x00000010 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ CNT CODE (CODICE CNT SCN \_ IMMAGINE) <br/>                 | 0x00000020 <br/> | La sezione contiene codice eseguibile. <br/>                                                                                                                           |
| IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA <br/>    | 0x00000040 <br/> | La sezione contiene dati inizializzati. <br/>                                                                                                                          |
| IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA <br/> | 0x00000080 <br/> | La sezione contiene dati non inizializzati. <br/>                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ OTHER <br/>                | 0x00000100 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ INFO <br/>                 | 0x00000200 <br/> | La sezione contiene commenti o altre informazioni. La sezione .drectve ha questo tipo. Questa opzione è valida solo per i file oggetto. <br/>                                    |
|                                                   | 0x00000400 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ REMOVE <br/>               | 0x00000800 <br/> | La sezione non diventerà parte dell'immagine. Questa opzione è valida solo per i file oggetto. <br/>                                                                             |
| IMAGE \_ SCN \_ LNK \_ COMDAT <br/>               | 0x00001000 <br/> | La sezione contiene dati COMDAT. Per altre informazioni, vedere [Sezioni COMDAT (solo oggetto).](#comdat-sections-object-only) Questa opzione è valida solo per i file oggetto. <br/> |
| \_GPREL SCN \_ IMMAGINE <br/>                     | 0x00008000 <br/> | La sezione contiene i dati a cui si fa riferimento tramite il puntatore globale (GP). <br/>                                                                                           |
| IMAGE \_ SCN \_ MEM \_ PURGEABLE <br/>            | 0x00020000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ 16BIT <br/>                | 0x00020000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ LOCKED <br/>               | 0x00040000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ PRELOAD (PRECARICAMENTO MEM SCN IMMAGINE) <br/>              | 0x00080000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| ALLINEAMENTO \_ SCN \_ IMMAGINE \_ 1BYTE <br/>             | 0x00100000 <br/> | Allineare i dati su un limite di 1 byte. Valido solo per i file oggetto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ ALIGN \_ 2BYTES <br/>             | 0x00200000 <br/> | Allineare i dati su un limite di 2 byte. Valido solo per i file oggetto. <br/>                                                                                                   |
| ALLINEAMENTO \_ SCN \_ IMMAGINE \_ 4BYTE <br/>             | 0x00300000 <br/> | Allineare i dati su un limite di 4 byte. Valido solo per i file oggetto. <br/>                                                                                                   |
| ALLINEAMENTO \_ SCN \_ IMMAGINE \_ 8BYTE <br/>             | 0x00400000 <br/> | Allineare i dati su un limite di 8 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| ALLINEAMENTO \_ SCN \_ IMMAGINE \_ 16BYTE <br/>            | 0x00500000 <br/> | Allineare i dati su un limite di 16 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| ALLINEAMENTO \_ SCN \_ IMMAGINE \_ 32BYTE <br/>            | 0x00600000 <br/> | Allineare i dati su un limite di 32 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 64BYTES <br/>            | 0x00700000 <br/> | Allineare i dati su un limite di 64 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| ALLINEAMENTO \_ SCN \_ IMMAGINE \_ 128BYTE <br/>           | 0x00800000 <br/> | Allineare i dati su un limite di 128 byte. Valido solo per i file oggetto. <br/>                                                                                                 |
| ALLINEAMENTO \_ SCN \_ IMMAGINE \_ 256BYTE <br/>           | 0x00900000 <br/> | Allineare i dati su un limite di 256 byte. Valido solo per i file oggetto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 512BYTES <br/>           | 0x00A00000 <br/> | Allineare i dati su un limite di 512 byte. Valido solo per i file oggetto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 1024BYTES <br/>          | 0x00B00000 <br/> | Allineare i dati su un limite di 1024 byte. Valido solo per i file oggetto. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 2048BYTES <br/>          | 0x00C00000 <br/> | Allineare i dati su un limite di 2048 byte. Valido solo per i file oggetto. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 4096BYTES <br/>          | 0x00D00000 <br/> | Allineare i dati su un limite di 4096 byte. Valido solo per i file oggetto. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 8192BYTES <br/>          | 0x00E00000 <br/> | Allineare i dati su un limite di 8192 byte. Valido solo per i file oggetto. <br/>                                                                                               |
| IMAGE \_ SCN \_ LNK \_ NRELOC \_ OVFL <br/>         | 0x01000000 <br/> | La sezione contiene rilocazioni estese. <br/>                                                                                                                      |
| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>          | 0x02000000 <br/> | La sezione può essere rimossa in base alle esigenze. <br/>                                                                                                                         |
| IMAGE \_ SCN \_ MEM \_ NOT \_ CACHED <br/>          | 0x04000000 <br/> | La sezione non può essere memorizzata nella cache. <br/>                                                                                                                                   |
| IMAGE \_ SCN \_ MEM \_ NOT \_ PAGED <br/>           | 0x08000000 <br/> | La sezione non è paginabile. <br/>                                                                                                                                    |
| IMAGE \_ SCN \_ MEM \_ SHARED <br/>               | 0x10000000 <br/> | La sezione può essere condivisa in memoria. <br/>                                                                                                                            |
| IMAGE \_ SCN \_ MEM \_ EXECUTE <br/>              | 0x20000000 <br/> | La sezione può essere eseguita come codice. <br/>                                                                                                                            |
| IMAGE \_ SCN \_ MEM \_ READ <br/>                 | 0x40000000 <br/> | La sezione può essere letta. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                | 0x80000000 <br/> | La sezione può essere scritta in . <br/>                                                                                                                                  |



 

IMAGE \_ SCN \_ LNK \_ NRELOC OVFL indica che il numero di rilocazioni per la sezione supera i 16 bit riservati nell'intestazione \_ di sezione. Se il bit è impostato e il campo NumberOfRelocations nell'intestazione di sezione è 0xffff, il numero effettivo di rilocazioni viene archiviato nel campo VirtualAddress a 32 bit della prima rilocazione. Si tratta di un errore se l'opzione IMAGE \_ SCN \_ LNK \_ NRELOC OVFL è impostata e nella sezione sono presenti meno 0xffff \_ rilocazioni.

### <a name="grouped-sections-object-only"></a>Sezioni raggruppate (solo oggetto)

"$"? il carattere (simbolo del dollaro) ha un'interpretazione speciale nei nomi di sezione nei file oggetto.

Quando si determina la sezione dell'immagine che conterrà il contenuto di una sezione dell'oggetto, il linker rimuove "$"? e tutti i caratteri che lo seguono. Di conseguenza, una sezione dell'oggetto denominata . **text$X** contribuisce effettivamente alla **sezione .text** nell'immagine.

Tuttavia, i caratteri che segue "$"? determinare l'ordinamento dei contributi alla sezione dell'immagine. Tutti i contributi con lo stesso nome della sezione oggetto vengono allocati in modo contiguo nell'immagine e i blocchi di contributi vengono ordinati in ordine lessicale in base al nome della sezione dell'oggetto. Di conseguenza, tutti gli elementi nei file oggetto con il nome di sezione **.text$X** finisce insieme, dopo i contributi **.text$W** e prima dei contributi **.text$Y.**

Il nome della sezione in un file di immagine non contiene mai "$"? .

## <a name="other-contents-of-the-file"></a>Altri contenuti del file

- [Dati della sezione](#section-data)
- [Rilocazioni COFF (solo oggetto)](#coff-relocations-object-only)
  - [Indicatori di tipo](#type-indicators)
- [Numeri di riga COFF (deprecati)](#coff-line-numbers-deprecated)
- [Tabella dei simboli COFF](#coff-symbol-table)
  - [Rappresentazione del nome del simbolo](#symbol-name-representation)
  - [Valori dei numeri di sezione](#section-number-values)
  - [Rappresentazione dei tipi](#type-representation)
  - [Archiviazione Classe](#storage-class)
- [Record di simboli ausiliari](#auxiliary-symbol-records)
  - [Formato ausiliario 1: definizioni di funzione](#auxiliary-format-1-function-definitions)
  - [Formato ausiliario 2: simboli .bf ed .ef](#auxiliary-format-2-bf-and-ef-symbols)
  - [Formato ausiliario 3: esterni deboli](#auxiliary-format-3-weak-externals)
  - [Formato ausiliario 4: file](#auxiliary-format-4-files)
  - [Formato ausiliario 5: definizioni di sezione](#auxiliary-format-5-section-definitions)
  - [Sezioni COMDAT (solo oggetto)](#comdat-sections-object-only)
  - [Definizione di token CLR (solo oggetto)](#clr-token-definition-object-only)
- [Tabella delle stringhe COFF](#coff-string-table)
- [Tabella del certificato dell'attributo (solo immagine)](#the-attribute-certificate-table-image-only)
  - [Dati certificato](#certificate-data)
- [Tabelle di importazione con caricamento ritardato (solo immagine)](#delay-load-import-tables-image-only)
  - [Tabella Delay-Load directory](#the-delay-load-directory-table)
  - [Attributes (Attributi)](#attributes)
  - [Nome](#name)
  - [Handle del modulo](#module-handle)
  - [Tabella degli indirizzi di importazione ritardata](#delay-import-address-table)
  - [Ritardare la tabella dei nomi di importazione](#delay-import-name-table)
  - [Tabella degli indirizzi di importazione con associazione ritardata e timestamp](#delay-bound-import-address-table-and-time-stamp)
  - [Ritardare lo scaricamento della tabella degli indirizzi di importazione](#delay-unload-import-address-table)

Le strutture di dati descritte finora, fino all'intestazione facoltativa inclusa, si trovano tutte a un offset fisso dall'inizio del file (o dall'intestazione PE se il file è un'immagine che contiene uno stub MS-DOS).

Il resto di un file di immagine o di oggetto COFF contiene blocchi di dati che non sono necessariamente in corrispondenza di un offset di file specifico. Le posizioni vengono invece definite dai puntatori nell'intestazione facoltativa o in un'intestazione di sezione.

Un'eccezione è per le immagini con un valore SectionAlignment inferiore alle dimensioni della pagina dell'architettura (4 K per Intel x86 e MIPS e 8 K per Itanium). Per una descrizione di SectionAlignment, vedere [Intestazione facoltativa (solo immagine).](#optional-header-image-only) In questo caso, sono presenti vincoli sull'offset di file dei dati della sezione, come descritto nella sezione 5.1, "Dati della sezione". Un'altra eccezione è che le informazioni di debug e il certificato dell'attributo devono essere posizionati alla fine di un file di immagine, con la tabella del certificato dell'attributo immediatamente precedente alla sezione di debug, perché il caricatore non esegue il mapping in memoria. La regola sul certificato dell'attributo e sulle informazioni di debug non si applica tuttavia ai file oggetto.

### <a name="section-data"></a>Dati della sezione

I dati inizializzati per una sezione sono costituiti da semplici blocchi di byte. Tuttavia, per le sezioni che contengono tutti zeri, i dati della sezione non devono essere inclusi.

I dati per ogni sezione si trovano in corrispondenza dell'offset di file specificato dal campo PointerToRawData nell'intestazione di sezione. Le dimensioni di questi dati nel file sono indicate dal campo SizeOfRawData. Se SizeOfRawData è minore di VirtualSize, il resto viene riempito con zeri.

In un file di immagine i dati della sezione devono essere allineati su un limite come specificato dal campo FileAlignment nell'intestazione facoltativa. I dati della sezione devono essere visualizzati in ordine dei valori RVA per le sezioni corrispondenti( come le singole intestazioni di sezione nella tabella delle sezioni).

Esistono restrizioni aggiuntive sui file di immagine se il valore SectionAlignment nell'intestazione facoltativa è minore delle dimensioni della pagina dell'architettura. Per tali file, il percorso dei dati della sezione nel file deve corrispondere alla posizione in memoria quando l'immagine viene caricata, in modo che l'offset fisico per i dati della sezione corrisponda a quello dell'RVA.

### <a name="coff-relocations-object-only"></a>Rilocazioni COFF (solo oggetto)

I file oggetto contengono rilocazioni COFF, che specificano la modalità di modifica dei dati della sezione quando vengono inseriti nel file di immagine e successivamente caricati in memoria.

I file di immagine non contengono rilocazioni COFF, perché a tutti i simboli di riferimento sono già stati assegnati indirizzi in uno spazio indirizzi flat. Un'immagine contiene informazioni di rilocazione sotto forma di rilocazioni di base nella sezione .reloc (a meno che l'immagine non abbia l'attributo STRIPPED IMAGE \_ FILE \_ RELOCS). \_ Per altre informazioni, vedere [La sezione .reloc (solo immagine)](#the-reloc-section-image-only).

Per ogni sezione in un file oggetto, una matrice di record a lunghezza fissa contiene le rilocazioni COFF della sezione. La posizione e la lunghezza della matrice vengono specificate nell'intestazione di sezione. Ogni elemento della matrice ha il formato seguente.



| Offset        | Dimensione          | Campo                        | Descrizione                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Indirizzo dell'elemento a cui viene applicata la rilocazione. Si tratta dell'offset dall'inizio della sezione, più il valore del campo RVA/Offset della sezione. Vedere [Tabella di sezione (intestazioni di sezione).](#section-table-section-headers) Ad esempio, se il primo byte della sezione ha un indirizzo 0x10, il terzo byte ha un indirizzo di 0x12. <br/> |
| 4 <br/> | 4 <br/> | SymbolTableIndex <br/> | Indice in base zero nella tabella dei simboli. Questo simbolo indica l'indirizzo da usare per la rilocazione. Se il simbolo specificato ha una classe di archiviazione di sezione, l'indirizzo del simbolo è l'indirizzo con la prima sezione con lo stesso nome. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | Tipo <br/>             | Valore che indica il tipo di rilocazione da eseguire. I tipi di rilocazione validi dipendono dal tipo di computer. Vedere [Indicatori di tipo](#type-indicators). <br/>                                                                                                                                                                                     |



 

Se il simbolo a cui fa riferimento il campo SymbolTableIndex ha la classe di archiviazione IMAGE SYM CLASS SECTION, l'indirizzo del simbolo è \_ \_ \_ l'inizio della sezione. La sezione si trova in genere nello stesso file, tranne quando il file oggetto fa parte di un archivio (libreria). In tal caso, la sezione è disponibile in qualsiasi altro file oggetto nell'archivio con lo stesso nome del membro di archivio del file oggetto corrente. La relazione con il nome del membro di archivio viene usata nel collegamento di tabelle di importazione, ovvero nella sezione .idata.

#### <a name="type-indicators"></a>Indicatori di tipo

Il campo Tipo del record di rilocazione indica il tipo di rilocazione da eseguire. Per ogni tipo di computer vengono definiti tipi di rilocazione diversi.

##### <a name="x64-processors"></a>Processori x64

Gli indicatori di tipo di rilocazione seguenti sono definiti per i processori x64 e compatibili.



| Costante                                | Valore              | Descrizione                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ AMD64 \_ ABSOLUTE <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                        |
| IMAGE \_ REL \_ AMD64 \_ ADDR64 <br/>   | 0x0001 <br/> | Va a 64 bit della destinazione di rilocazione. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32 <br/>   | 0x0002 <br/> | Va a 32 bit della destinazione di rilocazione. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32NB <br/> | 0x0003 <br/> | Indirizzo a 32 bit senza una base di immagini (RVA). <br/>                                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ REL32 <br/>    | 0x0004 <br/> | Indirizzo relativo a 32 bit dal byte che segue la rilocazione. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | Indirizzo a 32 bit relativo alla distanza in byte 1 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | Indirizzo a 32 bit relativo alla distanza in byte 2 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | Indirizzo a 32 bit relativo alla distanza in byte 3 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | Indirizzo a 32 bit relativo alla distanza in byte 4 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | Indirizzo a 32 bit relativo alla distanza in byte 5 dalla rilocazione. <br/>                                                                               |
| SEZIONE \_ IMAGE REL \_ AMD64 \_ <br/>  | 0x000A <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Viene usato per supportare le informazioni di debug. <br/>                                  |
| IMAGE \_ REL \_ AMD64 \_ SECREL <br/>   | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/> |
| IMAGE \_ REL \_ AMD64 \_ SECREL7 <br/>  | 0x000C <br/> | Offset senza segno a 7 bit dalla base della sezione che contiene la destinazione. <br/>                                                                    |
| IMAGE \_ REL \_ AMD64 \_ TOKEN <br/>    | 0x000D <br/> | Token CLR. <br/>                                                                                                                                       |
| IMAGE \_ REL \_ AMD64 \_ SREL32 <br/>   | 0x000E <br/> | Valore dipendente dall'intervallo con segno a 32 bit generato nell'oggetto . <br/>                                                                                     |
| COPPIA \_ IMAGE REL \_ AMD64 \_ <br/>     | 0x000F <br/> | Coppia che deve seguire immediatamente ogni valore dipendente dall'intervallo. <br/>                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ SSPAN32 <br/>  | 0x0010 <br/> | Valore dipendente dall'intervallo con segno a 32 bit applicato in fase di collegamento. <br/>                                                                                |



 

##### <a name="arm-processors"></a>Processori ARM

Per i processori ARM sono definiti gli indicatori di tipo di rilocazione seguenti.



| Costante                                | Valore              | Descrizione                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM \_ ABSOLUTE <br/>   | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ ARM \_ ADDR32 <br/>     | 0x0001 <br/> | Va a 32 bit della destinazione. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ ARM \_ ADDR32NB <br/>   | 0x0002 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ ARM \_ BRANCH24 <br/>   | 0x0003 <br/> | Spostamento relativo a 24 bit alla destinazione. <br/>                                                                                                                                                                                                            |
| IMAGE \_ REL \_ ARM \_ BRANCH11 <br/>   | 0x0004 <br/> | Riferimento a una chiamata di subroutine. Il riferimento è costituito da due istruzioni a 16 bit con offset a 11 bit. <br/>                                                                                                                                                 |
| IMMAGINE \_ REL \_ ARM \_ REL32 <br/>      | 0x000A <br/> | Indirizzo relativo a 32 bit dal byte che segue la rilocazione. <br/>                                                                                                                                                                                        |
| SEZIONE IMAGE \_ REL \_ \_ ARM <br/>    | 0x000E <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Viene usato per supportare le informazioni di debug. <br/>                                                                                                                                           |
| IMAGE \_ REL \_ ARM \_ SECREL <br/>     | 0x000F <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                          |
| IMMAGINE \_ REL \_ ARM \_ MOV32 <br/>      | 0x0010 <br/> | Va a 32 bit della destinazione. Questa rilocazione viene applicata usando un'istruzione MOVW per i 16 bit bassi seguiti da un MOVT per i 16 bit alti. <br/>                                                                                                              |
| IMMAGINE \_ REL \_ THUMB \_ MOV32 <br/>    | 0x0011 <br/> | Va a 32 bit della destinazione. Questa rilocazione viene applicata usando un'istruzione MOVW per i 16 bit bassi seguiti da un MOVT per i 16 bit alti. <br/>                                                                                                              |
| IMAGE \_ REL \_ THUMB \_ BRANCH20 <br/> | 0x0012 <br/> | L'istruzione è fissata con lo spostamento relativo a 21 bit alla destinazione allineata a 2 byte. Il bit meno significativo dello spostamento è sempre zero e non viene archiviato. Questa rilocazione corrisponde a un'istruzione B condizionale Thumb-2 a 32 bit. <br/> |
| Non utilizzato <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ THUMB \_ BRANCH24 <br/> | 0x0014 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 2 byte. Il bit meno significativo dello spostamento è zero e non viene archiviato. Questa rilocazione corrisponde a un'istruzione Thumb-2 B. <br/>                            |
| IMMAGINE \_ REL \_ THUMB \_ BLX23 <br/>    | 0x0015 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 4 byte. I 2 bit bassi dello spostamento sono pari a zero e non vengono archiviati. <br/> Questa rilocazione corrisponde a un'istruzione Thumb-2 BLX. <br/>                      |
| IMAGE \_ REL \_ ARM \_ PAIR <br/>       | 0x0016 <br/> | La rilocazione è valida solo quando segue immediatamente un REFHI ARM \_ o THUMB \_ REFHI. SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>Processori ARM64

Per i processori ARM64 sono definiti gli indicatori di tipo di rilocazione seguenti.



| Costante                                       | Valore              | Descrizione                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM64 \_ ABSOLUTE <br/>        | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                        |
| IMAGE \_ REL \_ ARM64 \_ ADDR32 <br/>          | 0x0001 <br/> | Va a 32 bit della destinazione. <br/>                                                                                                                      |
| IMMAGINE \_ REL \_ ARM64 \_ ADDR32NB <br/>        | 0x0002 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                     |
| IMMAGINE \_ REL \_ ARM64 \_ BRANCH26 <br/>        | 0x0003 <br/> | Spostamento relativo a 26 bit alla destinazione, per le istruzioni B e BL. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ PAGEBASE \_ REL21 <br/> | 0x0004 <br/> | Base di pagina della destinazione, per l'istruzione ADRP. <br/>                                                                                                |
| IMMAGINE \_ REL \_ ARM64 \_ REL21 <br/>           | 0x0005 <br/> | Spostamento relativo a 12 bit alla destinazione, per l'istruzione ADR <br/>                                                                               |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12A <br/> | 0x0006 <br/> | Offset di pagina a 12 bit della destinazione, per le istruzioni ADD/ADDS (immediate) con spostamento zero. <br/>                                                      |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12L <br/> | 0x0007 <br/> | Offset di pagina a 12 bit della destinazione, per l'istruzione LDR (indicizzata, immediata senza segno). <br/>                                                          |
| IMAGE \_ REL \_ ARM64 \_ SECREL <br/>          | 0x0008 <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/> |
| IMMAGINE \_ REL \_ ARM64 \_ SECREL \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 dell'offset di sezione della destinazione, per istruzioni ADD/ADDS (immediate) con spostamento zero. <br/>                                                  |
| IMMAGINE \_ REL \_ ARM64 \_ SECREL \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 dell'offset di sezione della destinazione, per istruzioni ADD/ADDS (immediate) con spostamento zero. <br/>                                                 |
| IMMAGINE \_ REL \_ ARM64 \_ SECREL \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 dell'offset di sezione della destinazione, per l'istruzione LDR (indicizzata, senza segno immediata). <br/>                                                      |
| TOKEN \_ \_ ARM64 DI IMAGE REL \_ <br/>           | 0x000C <br/> | Token CLR. <br/>                                                                                                                                        |
| SEZIONE \_ IMAGE REL \_ \_ ARM64 <br/>         | 0x000D <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Viene usato per supportare le informazioni di debug. <br/>                                  |
| IMAGE \_ REL \_ ARM64 \_ ADDR64 <br/>          | 0x000E <br/> | Va a 64 bit della destinazione di rilocazione. <br/>                                                                                                           |
| IMMAGINE \_ REL \_ ARM64 \_ BRANCH19 <br/>        | 0x000F <br/> | Offset a 19 bit per la destinazione di rilocazione, per l'istruzione B condizionale. <br/>                                                                        |
| IMMAGINE \_ REL \_ ARM64 \_ BRANCH14 <br/>        | 0x0010 <br/> | Offset a 14 bit per la destinazione di rilocazione, per istruzioni TBZ e TBNZ. <br/>                                                                        |
| IMMAGINE \_ REL \_ ARM64 \_ REL32 <br/>           | 0x0011 <br/> | Indirizzo relativo a 32 bit dal byte che segue la rilocazione. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>Processori SuperH Hitachi

Gli indicatori di tipo di rilocazione seguenti sono definiti per i processori SH3 e SH4. Le rilocazioni specifiche di SH5 vengono notate come SHM (SH Media).



| Costante                                      | Valore              | Descrizione                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ SH3 \_ ABSOLUTE <br/>         | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                     |
| IMAGE \_ REL \_ SH3 \_ DIRECT16 <br/>         | 0x0001 <br/> | Riferimento alla posizione a 16 bit che contiene la va del simbolo di destinazione. <br/>                                                                                                                                  |
| IMMAGINE \_ REL \_ SH3 \_ DIRECT32 <br/>         | 0x0002 <br/> | Va a 32 bit del simbolo di destinazione. <br/>                                                                                                                                                                            |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 <br/>          | 0x0003 <br/> | Riferimento alla posizione a 8 bit che contiene l'indirizzo VA del simbolo di destinazione. <br/>                                                                                                                                   |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ WORD <br/>    | 0x0004 <br/> | Riferimento all'istruzione a 8 bit che contiene l'effettiva vago a 16 bit del simbolo di destinazione. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ LONG <br/>    | 0x0005 <br/> | Riferimento all'istruzione a 8 bit che contiene l'effettivo va va a 32 bit del simbolo di destinazione. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 <br/>          | 0x0006 <br/> | Riferimento alla posizione a 8 bit i cui 4 bit bassi contengono l'va va del simbolo di destinazione. <br/>                                                                                                                        |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ WORD <br/>    | 0x0007 <br/> | Riferimento all'istruzione a 8 bit i cui 4 bit bassi contengono l'effettivo va va a 16 bit del simbolo di destinazione. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ LONG <br/>    | 0x0008 <br/> | Riferimento all'istruzione a 8 bit i cui 4 bit bassi contengono l'effettivo va va a 32 bit del simbolo di destinazione. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ WORD <br/>     | 0x0009 <br/> | Riferimento all'istruzione a 8 bit che contiene l'offset relativo effettivo a 16 bit del simbolo di destinazione. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ LONG <br/>     | 0x000A <br/> | Riferimento all'istruzione a 8 bit che contiene l'offset relativo effettivo a 32 bit del simbolo di destinazione. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL12 \_ WORD <br/>    | 0x000B <br/> | Riferimento all'istruzione a 16 bit i cui 12 bit bassi contengono l'offset relativo effettivo a 16 bit del simbolo di destinazione. <br/>                                                                                     |
| SEZIONE IMAGE \_ REL \_ SH3 \_ STARTOF \_ <br/> | 0x000C <br/> | Riferimento a una posizione a 32 bit che rappresenta la va della sezione che contiene il simbolo di destinazione. <br/>                                                                                                                |
| SEZIONE IMAGE \_ REL \_ SH3 \_ SIZEOF \_ <br/>  | 0x000D <br/> | Riferimento alla posizione a 32 bit che rappresenta le dimensioni della sezione che contiene il simbolo di destinazione. <br/>                                                                                                            |
| SEZIONE IMAGE \_ REL \_ SH3 \_ <br/>          | 0x000E <br/> | Indice di sezione a 16 bit della sezione che contiene la destinazione. Viene utilizzato per supportare le informazioni di debug. <br/>                                                                                               |
| IMAGE \_ REL \_ SH3 \_ SECREL <br/>           | 0x000F <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                              |
| IMAGE \_ REL \_ SH3 \_ DIRECT32 \_ NB <br/>     | 0x0010 <br/> | RVA a 32 bit del simbolo di destinazione. <br/>                                                                                                                                                                           |
| IMAGE \_ REL \_ SH3 \_ GPREL4 \_ LONG <br/>     | 0x0011 <br/> | Relativo del gruppo di criteri di gruppo. <br/>                                                                                                                                                                                                   |
| IMAGE \_ REL \_ SH3 \_ TOKEN <br/>            | 0x0012 <br/> | Token CLR. <br/>                                                                                                                                                                                                     |
| IMAGE \_ REL \_ SHM \_ PCRELPT <br/>          | 0x0013 <br/> | Offset dall'istruzione corrente in longwords. Se il bit NOMODE non è impostato, inserire l'inverso del bit basso nel bit 32 per selezionare PTA o PTB. <br/>                                                          |
| IMAGE \_ REL \_ SHM \_ REFLO <br/>            | 0x0014 <br/> | 16 bit bassi dell'indirizzo a 32 bit. <br/>                                                                                                                                                                         |
| IMAGE \_ REL \_ SHM \_ REFHALF <br/>          | 0x0015 <br/> | 16 bit alti dell'indirizzo a 32 bit. <br/>                                                                                                                                                                        |
| IMAGE \_ REL \_ SHM \_ RELLO <br/>            | 0x0016 <br/> | 16 bit bassi dell'indirizzo relativo. <br/>                                                                                                                                                                       |
| IMAGE \_ REL \_ SHM \_ RELHALF <br/>          | 0x0017 <br/> | 16 bit alti dell'indirizzo relativo. <br/>                                                                                                                                                                      |
| COPPIA IMAGE \_ REL \_ \_ SHM <br/>             | 0x0018 <br/> | La rilocazione è valida solo quando segue immediatamente una rilocazione REFHALF, RELHALF o RELLO. Il campo SymbolTableIndex della rilocazione contiene uno spostamento e non un indice nella tabella dei simboli. <br/> |
| IMAGE \_ REL \_ SHM \_ NOMODE <br/>           | 0x8000 <br/> | La rilocazione ignora la modalità sezione. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>Processori IBM PowerPC

I seguenti indicatori del tipo di rilocazione sono definiti per PowerPC processori.



| Costante                              | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ PPC \_ ABSOLUTE <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ PPC \_ ADDR64 <br/>   | 0x0001 <br/> | Va a 64 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR32 <br/>   | 0x0002 <br/> | Va a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR24 <br/>   | 0x0003 <br/> | 24 bit bassi dell'va va della destinazione. Questa opzione è valida solo quando il simbolo di destinazione è assoluto e può essere esteso al valore originale. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ PPC \_ ADDR16 <br/>   | 0x0004 <br/> | I 16 bit bassi dell'va va della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ PPC \_ ADDR14 <br/>   | 0x0005 <br/> | I 14 bit bassi dell'oggetto VA della destinazione. Questa opzione è valida solo quando il simbolo di destinazione è assoluto e può essere esteso al valore originale. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ PPC \_ REL24 <br/>    | 0x0006 <br/> | Offset PC-relative a 24 bit rispetto alla posizione del simbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ REL14 <br/>    | 0x0007 <br/> | Offset pc-relative a 14 bit rispetto alla posizione del simbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ ADDR32NB <br/> | 0x000A <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ PPC \_ SECREL <br/>   | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                       |
| SEZIONE \_ IMAGE REL \_ \_ PPC <br/>  | 0x000C <br/> | Indice di sezione a 16 bit della sezione che contiene la destinazione. Viene utilizzato per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECREL16 <br/> | 0x000F <br/> | Offset a 16 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ REL \_ PPC \_ REFHI <br/>    | 0x0010 <br/> | I 16 bit alti dell'va va a 32 bit della destinazione. Viene usato per la prima istruzione in una sequenza a due istruzioni che carica un indirizzo completo. La rilocazione deve essere seguita immediatamente da una rilocazione PAIR la cui proprietà SymbolTableIndex contiene uno spostamento a 16 bit con segno che viene aggiunto ai 16 bit superiori prelevati dalla posizione da spostare. <br/> |
| IMAGE \_ REL \_ PPC \_ REFLO <br/>    | 0x0011 <br/> | I 16 bit bassi dell'va va della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                     |
| COPPIA \_ IMAGE REL \_ \_ PPC <br/>     | 0x0012 <br/> | Rilocazione valida solo quando segue immediatamente una rilocazione REFHI o SECRELHI. L'oggetto SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECRELLO <br/> | 0x0013 <br/> | 16 bit bassi dell'offset a 32 bit della destinazione dall'inizio della relativa sezione. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ GPREL <br/>    | 0x0015 <br/> | Spostamento con segno a 16 bit della destinazione rispetto al registro criteri di gruppo. <br/>                                                                                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ PPC \_ TOKEN <br/>    | 0x0016 <br/> | Token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Processori Intel 386

I seguenti indicatori del tipo di rilocazione sono definiti per i processori Intel 386 e compatibili.



| Costante                               | Valore              | Descrizione                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ I386 \_ ABSOLUTE <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                        |
| IMAGE \_ REL \_ I386 \_ DIR16 <br/>    | 0x0001 <br/> | Non supportata. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ REL16 <br/>    | 0x0002 <br/> | Non supportata. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ DIR32 <br/>    | 0x0006 <br/> | Va a 32 bit della destinazione. <br/>                                                                                                                           |
| IMAGE \_ REL \_ I386 \_ DIR32NB <br/>  | 0x0007 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                          |
| IMAGE \_ REL \_ I386 \_ SEG12 <br/>    | 0x0009 <br/> | Non supportata. <br/>                                                                                                                                    |
| SEZIONE \_ IMAGE REL \_ I386 \_ <br/>  | 0x000A <br/> | Indice di sezione a 16 bit della sezione che contiene la destinazione. Viene utilizzato per supportare le informazioni di debug. <br/>                                  |
| IMAGE \_ REL \_ I386 \_ SECREL <br/>   | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/> |
| IMAGE \_ REL \_ I386 \_ TOKEN <br/>    | 0x000C <br/> | Token CLR. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ SECREL7 <br/>  | 0x000D <br/> | Offset a 7 bit dalla base della sezione che contiene la destinazione. <br/>                                                                             |
| IMAGE \_ REL \_ I386 \_ REL32 <br/>    | 0x0014 <br/> | Spostamento relativo a 32 bit alla destinazione. Supporta il ramo relativo x86 e le istruzioni di chiamata. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Famiglia di processori Intel Itanium (IPF)

I seguenti indicatori del tipo di rilocazione sono definiti per la famiglia di processori Intel Itanium e i processori compatibili. Si noti che le rilocazioni nelle istruzioni usano l'offset del bundle e il numero di slot per l'offset di rilocazione.



| Costante                                 | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ IA64 \_ ABSOLUTE <br/>   | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ IA64 \_ IMM14 <br/>      | 0x0001 <br/> | La rilocazione dell'istruzione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione prima che venga inserito nello slot specificato nel bundle IMM14. La destinazione di rilocazione deve essere assoluta o l'immagine deve essere fissa. <br/>                                                                                 |
| IMAGE \_ REL \_ IA64 \_ IMM22 <br/>      | 0x0002 <br/> | La rilocazione dell'istruzione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione prima che venga inserito nello slot specificato nel bundle IMM22. La destinazione di rilocazione deve essere assoluta o l'immagine deve essere fissa. <br/>                                                                                 |
| IMAGE \_ REL \_ IA64 \_ IMM64 <br/>      | 0x0003 <br/> | Il numero di slot di questa rilocazione deve essere uno (1). La rilocazione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione prima che venga archiviato in tutti e tre gli slot del bundle IMM64. <br/>                                                                                                                   |
| IMMAGINE \_ REL \_ IA64 \_ DIR32 <br/>      | 0x0004 <br/> | Va a 32 bit della destinazione. Questa opzione è supportata solo per le immagini /LARGEADDRESSAWARE:NO. <br/>                                                                                                                                                                                                                                                    |
| IMAGE \_ REL \_ IA64 \_ DIR64 <br/>      | 0x0005 <br/> | Va a 64 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                             |
| IMMAGINE \_ REL \_ IA64 \_ PCREL21B <br/>   | 0x0006 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 16 bit. I 4 bit bassi dello spostamento sono pari a zero e non vengono archiviati. <br/>                                                                                                                                                                     |
| IMMAGINE \_ REL \_ IA64 \_ PCREL21M <br/>   | 0x0007 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 16 bit. I 4 bit bassi dello spostamento, che sono pari a zero, non vengono archiviati. <br/>                                                                                                                                                                 |
| IMMAGINE \_ REL \_ IA64 \_ PCREL21F <br/>   | 0x0008 <br/> | Gli LSB dell'offset di questa rilocazione devono contenere il numero di slot, mentre il resto è l'indirizzo del bundle. L'aggregazione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 16 bit. I 4 bit bassi dello spostamento sono pari a zero e non vengono archiviati. <br/>                                                                |
| IMMAGINE \_ REL \_ IA64 \_ GPREL22 <br/>    | 0x0009 <br/> | La rilocazione dell'istruzione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione e quindi da un offset relativo ai Criteri di gruppo a 22 bit calcolato e applicato al bundle GPREL22. <br/>                                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ LTOFF22 <br/>    | 0x000A <br/> | L'istruzione è fissata con l'offset relativo a 22 bit gp alla voce di tabella letterale del simbolo di destinazione. Il linker crea questa voce di tabella letterale in base a questa rilocazione e alla rilocazione ADDEND che potrebbe seguire. <br/>                                                                                                        |
| SEZIONE \_ IMAGE REL \_ IA64 \_ <br/>    | 0x000B <br/> | L'indice della sezione a 16 bit della sezione contiene la destinazione. Viene usato per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                         |
| IMMAGINE \_ REL \_ IA64 \_ SECREL22 <br/>   | 0x000C <br/> | L'istruzione è fissata con l'offset a 22 bit della destinazione dall'inizio della relativa sezione. Questa rilocazione può essere seguita immediatamente da una rilocazione ADDEND, il cui campo Value contiene l'offset senza segno a 32 bit della destinazione dall'inizio della sezione. <br/>                                                     |
| IMMAGINE \_ REL \_ IA64 \_ SECREL64I <br/>  | 0x000D <br/> | Il numero di slot per questa rilocazione deve essere uno (1). L'istruzione è fissata con l'offset a 64 bit della destinazione dall'inizio della relativa sezione. Questa rilocazione può essere seguita immediatamente da una rilocazione ADDEND il cui campo Valore contiene l'offset senza segno a 32 bit della destinazione dall'inizio della sezione. <br/> |
| IMMAGINE \_ REL \_ IA64 \_ SECREL32 <br/>   | 0x000E <br/> | Indirizzo dei dati da risolvere con l'offset a 32 bit della destinazione dall'inizio della relativa sezione. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ IA64 \_ DIR32NB <br/>    | 0x0010 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ SREL14 <br/>     | 0x0011 <br/> | Viene applicato a un oggetto immediato a 14 bit con segno che contiene la differenza tra due destinazioni rilocabili. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già generato questo valore. <br/>                                                                                                              |
| IMAGE \_ REL \_ IA64 \_ SREL22 <br/>     | 0x0012 <br/> | Viene applicato a un oggetto immediato a 22 bit con segno che contiene la differenza tra due destinazioni rilocabili. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già generato questo valore. <br/>                                                                                                              |
| IMAGE \_ REL \_ IA64 \_ SREL32 <br/>     | 0x0013 <br/> | Viene applicato a un oggetto immediato a 32 bit con segno che contiene la differenza tra due valori rilocabili. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già generato questo valore. <br/>                                                                                                               |
| IMAGE \_ REL \_ IA64 \_ UREL32 <br/>     | 0x0014 <br/> | Viene applicato a un oggetto immediato senza segno a 32 bit che contiene la differenza tra due valori rilocabili. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già generato questo valore. <br/>                                                                                                            |
| IMMAGINE \_ REL \_ IA64 \_ PCREL60X <br/>   | 0x0015 <br/> | Correzione relativa a PC a 60 bit che rimane sempre come istruzione BRL di un bundle MLX. <br/>                                                                                                                                                                                                                                                 |
| IMMAGINE \_ REL \_ IA64 \_ PCREL60B <br/>   | 0x0016 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione rientra in un campo a 25 bit con segno, convertire l'intero bundle in un bundle MBB con NOP. B nello slot 1 e un'istruzione BR a 25 bit (con i 4 bit più bassi tutti zero ed eliminati) nello slot 2. <br/>                                                                                          |
| IMMAGINE \_ REL \_ IA64 \_ PCREL60F <br/>   | 0x0017 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione rientra in un campo con segno a 25 bit, convertire l'intero bundle in un bundle MFB con NOP. F nello slot 1 e un'istruzione BR a 25 bit (4 bit più bassi tutti zero ed eliminati) nello slot 2. <br/>                                                                                                   |
| IMMAGINE \_ REL \_ IA64 \_ PCREL60I <br/>   | 0x0018 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione rientra in un campo a 25 bit con segno, convertire l'intero bundle in un bundle MIB con NOP. I nello slot 1 e un'istruzione BR a 25 bit (4 bit più bassi tutti zero ed eliminati) nello slot 2. <br/>                                                                                                   |
| IMMAGINE \_ REL \_ IA64 \_ PCREL60M <br/>   | 0x0019 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione rientra in un campo con segno a 25 bit, convertire l'intero bundle in un bundle MMB con NOP. M nello slot 1 e un'istruzione BR a 25 bit (4 bit più bassi tutti zero ed eliminati) nello slot 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ IMMGPREL64 <br/> | 0x001a <br/> | Correzione relativa ai Criteri di gruppo a 64 bit. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ IA64 \_ TOKEN <br/>      | 0x001b <br/> | Token CLR. <br/>                                                                                                                                                                                                                                                                                                                        |
| IMMAGINE \_ REL \_ IA64 \_ GPREL32 <br/>    | 0x001c <br/> | Correzione relativa a Criteri di gruppo a 32 bit. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ IA64 \_ ADDEND <br/>     | 0x001F <br/> | La rilocazione è valida solo quando segue immediatamente una delle seguenti rilocazioni: IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I o SECREL32. Il valore contiene l'addend da applicare alle istruzioni all'interno di un bundle, non ai dati. <br/>                                                                  |



 

##### <a name="mips-processors"></a>Processori MIPS

I seguenti indicatori del tipo di rilocazione sono definiti per i processori MIPS.



| Costante                                | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ MIPS \_ ABSOLUTE <br/>  | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ MIPS \_ REFHALF <br/>   | 0x0001 <br/> | I 16 bit alti della va a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ MIPS \_ REFWORD <br/>   | 0x0002 <br/> | Va a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ MIPS \_ JMPADDR <br/>   | 0x0003 <br/> | I 26 bit bassi dell'istanza di va della destinazione. Supporta le istruzioni J e JAL MIPS. <br/>                                                                                                                                                                                                                                                                                      |
| IMAGE \_ REL \_ MIPS \_ REFHI <br/>     | 0x0004 <br/> | I 16 bit alti della va a 32 bit della destinazione. Viene usato per la prima istruzione in una sequenza di due istruzioni che carica un indirizzo completo. Questa rilocazione deve essere seguita immediatamente da una rilocazione PAIR il cui SymbolTableIndex contiene uno spostamento a 16 bit con segno che viene aggiunto ai 16 bit superiori prelevati dalla posizione da spostare. <br/> |
| IMAGE \_ REL \_ MIPS \_ REFLO <br/>     | 0x0005 <br/> | I 16 bit bassi dell'istanza di va della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMMAGINE \_ REL \_ MIPS \_ GPREL <br/>     | 0x0006 <br/> | Spostamento con segno a 16 bit della destinazione rispetto al registro criteri di gruppo. <br/>                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ MIPS \_ LITERAL <br/>   | 0x0007 <br/> | Uguale a IMAGE \_ REL \_ MIPS \_ GPREL. <br/>                                                                                                                                                                                                                                                                                                                                    |
| SEZIONE \_ IMAGE REL \_ \_ MIPS <br/>   | 0x000A <br/> | L'indice della sezione a 16 bit della sezione contiene la destinazione. Viene usato per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                                                             |
| IMMAGINE \_ REL \_ MIPS \_ SECREL <br/>    | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                       |
| SECRELLO MIPS DI IMAGE \_ REL \_ \_ <br/>  | 0x000C <br/> | I 16 bit bassi dell'offset a 32 bit della destinazione dall'inizio della relativa sezione. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ MIPS \_ SECRELHI <br/>  | 0x000D <br/> | I 16 bit alti dell'offset a 32 bit della destinazione dall'inizio della relativa sezione. Una \_ rilocazione IMAGE REL \_ MIPS \_ PAIR deve seguire immediatamente questa. SymbolTableIndex della rilocazione PAIR contiene uno spostamento a 16 bit con segno che viene aggiunto ai 16 bit superiori che vengono presi dalla posizione che viene rilocata. <br/>                            |
| IMAGE \_ REL \_ MIPS \_ JMPADDR16 <br/> | 0x0010 <br/> | I 26 bit bassi dell'istanza di va della destinazione. Supporta l'istruzione JAL MIPS16. <br/>                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ MIPS \_ REFWORDNB <br/> | 0x0022 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                |
| COPPIA \_ MIPS REL \_ \_ IMMAGINE <br/>      | 0x0025 <br/> | La rilocazione è valida solo quando segue immediatamente una rilocazione REFHI o SECRELHI. SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>Mitsubishi M32R

Gli indicatori di tipo di rilocazione seguenti sono definiti per i processori Mitsubishi M32R.



| Costante                               | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ M32R \_ ABSOLUTE <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ M32R \_ ADDR32 <br/>   | 0x0001 <br/> | Va a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ M32R \_ ADDR32NB <br/> | 0x0002 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ M32R \_ ADDR24 <br/>   | 0x0003 <br/> | Va a 24 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMMAGINE \_ REL \_ M32R \_ GPREL16 <br/>  | 0x0004 <br/> | Offset a 16 bit della destinazione dal registro Criteri di gruppo. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| IMMAGINE \_ REL \_ M32R \_ PCREL24 <br/>  | 0x0005 <br/> | Offset a 24 bit della destinazione dal contatore del programma (PC), spostato a sinistra di 2 bit ed esteso con segno <br/>                                                                                                                                                                                                                                                                                                |
| IMMAGINE \_ REL \_ M32R \_ PCREL16 <br/>  | 0x0006 <br/> | Offset a 16 bit della destinazione dal PC, spostato a sinistra di 2 bit ed esteso per il segno <br/>                                                                                                                                                                                                                                                                                                                  |
| IMMAGINE \_ REL \_ M32R \_ PCREL8 <br/>   | 0x0007 <br/> | Offset a 8 bit della destinazione dal PC, spostato a sinistra di 2 bit ed esteso con segno <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ M32R \_ REFHALF <br/>  | 0x0008 <br/> | 16 MSB dell'istanza di va di destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ M32R \_ REFHI <br/>    | 0x0009 <br/> | I 16 MSB dell'istanza di va di destinazione, adattati per l'estensione del segno LSB. Viene usato per la prima istruzione in una sequenza a due istruzioni che carica un indirizzo completo a 32 bit. Questa rilocazione deve essere seguita immediatamente da una rilocazione PAIR il cui SymbolTableIndex contiene uno spostamento a 16 bit con segno che viene aggiunto ai 16 bit superiori prelevati dalla posizione da spostare. <br/> |
| IMAGE \_ REL \_ M32R \_ REFLO <br/>    | 0x000A <br/> | 16 LSB dell'istanza di va di destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| COPPIA \_ IMAGE REL \_ M32R \_ <br/>     | 0x000B <br/> | La rilocazione deve seguire la rilocazione REFHI. SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                                                                                                                                                                                             |
| SEZIONE \_ IMAGE REL \_ M32R \_ <br/>  | 0x000C <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Viene utilizzato per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ SECREL <br/>   | 0x000D <br/> | Offset a 32 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ M32R \_ TOKEN <br/>    | 0x000E <br/> | Token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>Numeri di riga COFF (deprecati)

I numeri di riga COFF non vengono più prodotti e, in futuro, non verranno utilizzati.

I numeri di riga COFF indicano la relazione tra il codice e i numeri di riga nei file di origine. Il formato Microsoft per i numeri di riga COFF è simile al formato COFF standard, ma è stato esteso per consentire a una singola sezione di correlare i numeri di riga in più file di origine.

I numeri di riga COFF sono costituiti da una matrice di record a lunghezza fissa. La posizione (offset del file) e le dimensioni della matrice vengono specificate nell'intestazione di sezione. Ogni record di numeri di riga ha il formato seguente.



| Offset        | Dimensione          | Campo                  | Descrizione                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Tipo ( \* ) <br/>  | Si tratta di un'unione di due campi: SymbolTableIndex e VirtualAddress. L'uso di SymbolTableIndex o RVA dipende dal valore di Linenumber. <br/> |
| 4 <br/> | 2 <br/> | Linenumber <br/> | Se diverso da zero, questo campo specifica un numero di riga in base uno. Se il valore è zero, il campo Tipo viene interpretato come indice della tabella dei simboli per una funzione. <br/>    |



 

Il campo Type è un'unione di due campi a 4 byte: SymbolTableIndex e VirtualAddress.



| Offset        | Dimensione          | Campo                        | Descrizione                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | SymbolTableIndex <br/> | Usato quando Linenumber è zero: indice nella voce della tabella dei simboli per una funzione. Questo formato viene usato per indicare la funzione a cui fa riferimento un gruppo di record di numeri di riga. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Usato quando Linenumber è diverso da zero: RVA del codice eseguibile che corrisponde alla riga di origine indicata. In un file oggetto contiene l'va all'interno della sezione . <br/> |



 

Un record di numeri di riga può impostare il campo Linenumber su zero e puntare a una definizione di funzione nella tabella dei simboli oppure può funzionare come voce standard del numero di riga fornendo un numero intero positivo (numero di riga) e l'indirizzo corrispondente nel codice oggetto.

Un gruppo di voci di numeri di riga inizia sempre con il primo formato: l'indice di un simbolo di funzione. Se si tratta del primo record di numero di riga nella sezione , è anche il nome del simbolo COMDAT per la funzione se è impostato il flag COMDAT della sezione. Vedere [Sezioni COMDAT (solo oggetto).](#comdat-sections-object-only) Il record ausiliario della funzione nella tabella dei simboli ha un puntatore al campo Linenumber che punta a questo stesso record di numero di riga.

Un record che identifica una funzione è seguito da un numero qualsiasi di voci di numeri di riga che forniscono informazioni effettive sul numero di riga, ovvero le voci con Numero di riga maggiore di zero. Queste voci sono in base uno, relative all'inizio della funzione e rappresentano ogni riga di origine nella funzione, ad eccezione della prima riga.

Ad esempio, il primo record di numero di riga per l'esempio seguente specifica la funzione ReverseSign (SymbolTableIndex di ReverseSign e Linenumber impostato su zero). Seguono quindi i record con valori Linenumber 1, 2 e 3, corrispondenti alle righe di origine come illustrato:


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>Tabella dei simboli COFF

La tabella dei simboli in questa sezione viene ereditata dal formato COFF tradizionale. È diverso dalle informazioni Microsoft Visual C++ debug. Un file può contenere sia una tabella dei simboli COFF che Visual C++ informazioni di debug e i due file vengono mantenuti separati. Alcuni strumenti Microsoft usano la tabella dei simboli per scopi limitati ma importanti, ad esempio per comunicare informazioni COMDAT al linker. Nella tabella dei simboli sono elencati i nomi di sezione e i nomi di file, nonché i simboli di codice e di dati.

La posizione della tabella dei simboli è indicata nell'intestazione COFF.

La tabella dei simboli è una matrice di record, ogni 18 byte. Ogni record è un record standard o ausiliario della tabella dei simboli. Un record standard definisce un simbolo o un nome e ha il formato seguente.



| Offset         | Dimensione          | Campo                          | Descrizione                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nome ( \* ) <br/>          | Nome del simbolo, rappresentato da un'unione di tre strutture . Se il nome non è lungo più di 8 byte, viene usata una matrice di 8 byte. Per altre informazioni, vedere [Rappresentazione del nome del simbolo.](https://www.bing.com/search?q=Symbol+Name+Representation) <br/> |
| 8 <br/>  | 4 <br/> | Valore <br/>              | Valore associato al simbolo. L'interpretazione di questo campo dipende da SectionNumber e StorageClass. Un significato tipico è l'indirizzo rilocabile. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | Intero con segno che identifica la sezione, utilizzando un indice in base uno nella tabella della sezione. Alcuni valori hanno un significato speciale, come definito nella sezione 5.4.2, "Valori dei numeri di sezione". <br/>                                         |
| 14 <br/> | 2 <br/> | Tipo <br/>               | Numero che rappresenta il tipo. Gli strumenti Microsoft impostano questo campo 0x20 (funzione) o 0x0 (non una funzione). Per altre informazioni, vedere [Rappresentazione del tipo.](#type-representation) <br/>                                                |
| 16 <br/> | 1 <br/> | StorageClass <br/>       | Valore enumerato che rappresenta la classe di archiviazione. Per altre informazioni, vedere [classe Archiviazione .](#storage-class) <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | NumberOfAuxSymbols <br/> | Numero di voci della tabella dei simboli ausiliari che seguono questo record. <br/>                                                                                                                                                           |



 

Zero o più record ausiliari della tabella dei simboli seguono immediatamente ogni record standard della tabella dei simboli. Tuttavia, in genere non più di un record di tabella dei simboli ausiliario segue un record standard della tabella simboli (ad eccezione dei record con estensione file con nomi di file lunghi). Ogni record ausiliario ha le stesse dimensioni di un record standard della tabella dei simboli (18 byte), ma anziché definire un nuovo simbolo, il record ausiliario fornisce informazioni aggiuntive sull'ultimo simbolo definito. La scelta dei diversi formati da usare dipende dal campo StorageClass. I formati attualmente definiti per i record della tabella dei simboli ausiliari sono illustrati nella sezione 5.5, "Record di simboli ausiliari".

Gli strumenti che leggono le tabelle dei simboli COFF devono ignorare i record dei simboli ausiliari la cui interpretazione è sconosciuta. In questo modo è possibile estendere il formato della tabella dei simboli per aggiungere nuovi record ausiliari, senza interrompere gli strumenti esistenti.

#### <a name="symbol-name-representation"></a>Rappresentazione del nome del simbolo

Il campo ShortName in una tabella dei simboli è costituito da 8 byte che contengono il nome stesso, se non è lungo più di 8 byte oppure il campo ShortName fornisce un offset nella tabella di stringhe. Per determinare se viene specificato il nome stesso o un offset, testare i primi 4 byte per verificarne l'uguaglianza su zero.

Per convenzione, i nomi vengono considerati come stringhe con codifica UTF-8 con terminazione zero.



| Offset        | Dimensione          | Campo                 | Descrizione                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | ShortName <br/> | Matrice di 8 byte. Questa matrice viene riempita con valori Null a destra se il nome è lungo meno di 8 byte. <br/> |
| 0 <br/> | 4 <br/> | Zeri <br/>    | Campo impostato su tutti gli zeri se il nome è più lungo di 8 byte. <br/>                                     |
| 4 <br/> | 4 <br/> | Offset <br/>    | Offset nella tabella di stringhe. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Valori dei numeri di sezione

In genere, il campo Valore sezione in una voce della tabella dei simboli è un indice in base uno nella tabella di sezione. Tuttavia, questo campo è un intero con segno e può assumere valori negativi. I valori seguenti, minori di uno, hanno significati speciali.



| Costante                          | Valore          | Descrizione                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ SYM \_ UNDEFINED <br/> | 0 <br/>  | Al record del simbolo non è ancora assegnata una sezione. Il valore zero indica che un riferimento a un simbolo esterno è definito altrove. Un valore diverso da zero è un simbolo comune con una dimensione specificata dal valore . <br/> |
| IMAGE \_ SYM \_ ABSOLUTE <br/>  | -1 <br/> | Il simbolo ha un valore assoluto (non rilocabile) e non è un indirizzo. <br/>                                                                                                                                                  |
| DEBUG \_ DI IMAGE SYM \_ <br/>     | -2 <br/> | Il simbolo fornisce informazioni generali sul tipo o sul debug, ma non corrisponde a una sezione. Gli strumenti Microsoft usano questa impostazione insieme ai record con estensione file (classe di archiviazione FILE). <br/>                                            |



 

#### <a name="type-representation"></a>Rappresentazione dei tipi

Il campo Tipo di una voce della tabella dei simboli contiene 2 byte, in cui ogni byte rappresenta informazioni sul tipo. LSB rappresenta il tipo di dati semplice (base) e msb rappresenta il tipo complesso, se presente:



| Msb                                                       | Lsb                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Tipo complesso: nessuno, puntatore, funzione, matrice. <br/> | Tipo di base: integer, a virgola mobile e così via. <br/> |



 

I valori seguenti sono definiti per il tipo di base, anche se gli strumenti Microsoft in genere non usano questo campo e impostano l'LSB su 0. Vengono invece Visual C++ informazioni di debug per indicare i tipi. Tuttavia, i possibili valori COFF sono elencati qui per completezza.



| Costante                             | Valore          | Descrizione                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| IMAGE \_ SYM \_ TYPE \_ NULL <br/>   | 0 <br/>  | Nessuna informazione sul tipo o tipo di base sconosciuto. Gli strumenti Microsoft usano questa impostazione <br/> |
| TIPO \_ DI SIM DI IMMAGINE \_ \_ VOID <br/>   | 1 <br/>  | Nessun tipo valido. usato con puntatori void e funzioni <br/>                       |
| IMAGE \_ SYM \_ TYPE \_ CHAR <br/>   | 2 <br/>  | Carattere (byte con segno) <br/>                                                  |
| IMAGE \_ SYM \_ TYPE \_ SHORT <br/>  | 3 <br/>  | Intero con segno a 2 byte <br/>                                                    |
| IMAGE \_ SYM \_ TYPE \_ INT <br/>    | 4 <br/>  | Tipo integer naturale (in genere 4 byte in Windows) <br/>                       |
| IMAGE \_ SYM \_ TYPE \_ LONG <br/>   | 5 <br/>  | Intero con segno a 4 byte <br/>                                                    |
| TIPO \_ DI SIM DI IMMAGINE \_ \_ FLOAT <br/>  | 6 <br/>  | Numero a virgola mobile a 4 byte <br/>                                             |
| IMAGE \_ SYM \_ TYPE \_ DOUBLE <br/> | 7 <br/>  | Numero a virgola mobile a 8 byte <br/>                                            |
| IMAGE \_ SYM \_ TYPE \_ STRUCT <br/> | 8 <br/>  | Struttura <br/>                                                                |
| IMAGE \_ SYM \_ TYPE \_ UNION <br/>  | 9 <br/>  | Un'unione <br/>                                                                    |
| ENUMERAZIONE IMAGE \_ SYM \_ TYPE \_ <br/>   | 10 <br/> | Tipo enumerato <br/>                                                         |
| MOE \_ DI TIPO \_ IMAGE SYM \_ <br/>    | 11 <br/> | Membro dell'enumerazione (un valore specifico) <br/>                                 |
| BYTE \_ DI TIPO IMAGE \_ SYM \_ <br/>   | 12 <br/> | Un byte; Intero senza segno a 1 byte <br/>                                            |
| IMAGE \_ SYM \_ TYPE \_ WORD <br/>   | 13 <br/> | Una parola; Intero senza segno a 2 byte <br/>                                            |
| UINT \_ DI TIPO \_ IMAGE SYM \_ <br/>   | 14 <br/> | Intero senza segno di dimensioni naturali (in genere, 4 byte) <br/>                    |
| IMAGE \_ SYM \_ TYPE \_ DWORD <br/>  | 15 <br/> | Intero senza segno a 4 byte <br/>                                                 |



 

Il byte più significativo specifica se il simbolo è un puntatore, una funzione restituita o una matrice del tipo di base specificato nell'LSB. Gli strumenti Microsoft usano questo campo solo per indicare se il simbolo è una funzione, in modo che gli unici due valori risultanti siano 0x0 e 0x20 per il campo Tipo. Tuttavia, altri strumenti possono usare questo campo per comunicare altre informazioni.

È molto importante specificare correttamente l'attributo della funzione. Queste informazioni sono necessarie per il corretto funzionamento del collegamento incrementale. Per alcune architetture, le informazioni potrebbero essere necessarie per altri scopi.



| Costante                                | Valore         | Descrizione                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| IMAGE \_ SYM \_ DTYPE \_ NULL <br/>     | 0 <br/> | Nessun tipo derivato. il simbolo è una variabile scalare semplice. <br/> |
| PUNTATORE IMAGE \_ SYM \_ DTYPE \_ <br/>  | 1 <br/> | Il simbolo è un puntatore al tipo di base. <br/>                    |
| FUNZIONE IMAGE \_ SYM \_ \_ DTYPE <br/> | 2 <br/> | Il simbolo è una funzione che restituisce un tipo di base. <br/>       |
| IMAGE \_ SYM \_ DTYPE \_ ARRAY <br/>    | 3 <br/> | Il simbolo è una matrice di tipo base. <br/>                     |



 

#### <a name="storage-class"></a>Classe di archiviazione

Il campo StorageClass della tabella dei simboli indica il tipo di definizione rappresentato da un simbolo. La tabella seguente illustra i valori possibili. Si noti che il campo StorageClass è un intero senza segno a 1 byte. Il valore speciale -1 deve pertanto essere utilizzato per indicare l'equivalente senza segno, 0xFF.

Anche se il formato COFF tradizionale usa molti valori di classe di archiviazione, gli strumenti Microsoft si basano sul formato di debug Visual C++ per la maggior parte delle informazioni simboliche e in genere usano solo quattro valori di classe di archiviazione: EXTERNAL (2), STATIC (3), FUNCTION (101) e FILE (103). Fatta eccezione per la seconda intestazione di colonna seguente, "Valore" deve essere impostato sul campo Valore del record del simbolo (la cui interpretazione dipende dal numero trovato come classe di archiviazione).



| Costante                                          | Valore                 | Descrizione/interpretazione del campo Valore                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FINE \_ DELLA CLASSE IMAGE SYM DELLA \_ \_ \_ \_ FUNZIONE <br/>  | -1 (0xFF) <br/> | Simbolo speciale che rappresenta la fine della funzione, a scopo di debug. <br/>                                                                                                                                                                                                                                                  |
| CLASSE \_ IMAGE SYM \_ \_ NULL <br/>               | 0 <br/>         | Nessuna classe di archiviazione assegnata. <br/>                                                                                                                                                                                                                                                                                                     |
| CLASSE \_ IMAGE SYM \_ \_ AUTOMATIC <br/>          | 1 <br/>         | Variabile automatica (stack). Il campo Valore specifica l'stack frame offset. <br/>                                                                                                                                                                                                                                              |
| CLASSE \_ IMAGE SYM \_ \_ EXTERNAL <br/>           | 2 <br/>         | Valore che gli strumenti Microsoft usano per i simboli esterni. Il campo Valore indica le dimensioni se il numero di sezione è IMAGE \_ SYM \_ UNDEFINED (0). Se il numero di sezione non è zero, il campo Valore specifica l'offset all'interno della sezione. <br/>                                                                                 |
| CLASSE \_ IMAGE SYM \_ \_ STATIC <br/>             | 3 <br/>         | Offset del simbolo all'interno della sezione. Se il campo Valore è zero, il simbolo rappresenta un nome di sezione. <br/>                                                                                                                                                                                                            |
| REGISTRO \_ DI CLASSI IMAGE SYM \_ \_ <br/>           | 4 <br/>         | Variabile di registro. Il campo Valore specifica il numero di registro. <br/>                                                                                                                                                                                                                                                            |
| DEF \_ ESTERNO DELLA CLASSE IMAGE SYM \_ \_ \_ <br/>      | 5 <br/>         | Simbolo definito esternamente. <br/>                                                                                                                                                                                                                                                                                           |
| ETICHETTA \_ DELLA CLASSE IMAGE SYM \_ \_ <br/>              | 6 <br/>         | Etichetta di codice definita all'interno del modulo. Il campo Valore specifica l'offset del simbolo all'interno della sezione. <br/>                                                                                                                                                                                                         |
| ETICHETTA \_ NON DEFINITA DELLA CLASSE IMAGE \_ \_ \_ SYM <br/>   | 7 <br/>         | Riferimento a un'etichetta di codice non definita. <br/>                                                                                                                                                                                                                                                                               |
| MEMBRO \_ DELLA CLASSE IMAGE SYM DELLO \_ \_ \_ \_ STRUCT <br/> | 8 <br/>         | Membro della struttura . Il campo Valore specifica l'eesimo membro. <br/>                                                                                                                                                                                                                                                               |
| ARGOMENTO \_ DELLA CLASSE IMAGE SYM \_ \_ <br/>           | 9 <br/>         | Argomento formale (parametro) di una funzione. Il campo Valore specifica l'esesimo argomento. <br/>                                                                                                                                                                                                                                      |
| TAG \_ STRUCT \_ DELLA CLASSE IMAGE \_ SYM \_ <br/>        | 10 <br/>        | Voce tag-name della struttura. <br/>                                                                                                                                                                                                                                                                                                  |
| MEMBRO DELLA \_ CLASSE IMAGE SYM \_ DI \_ \_ \_ UNION <br/>  | 11 <br/>        | Membro dell'unione. Il campo Valore specifica l'eesimo membro. <br/>                                                                                                                                                                                                                                                                     |
| TAG DI \_ UNIONE DELLA CLASSE IMAGE SYM \_ \_ \_ <br/>         | 12 <br/>        | Voce union tag-name. <br/>                                                                                                                                                                                                                                                                                                      |
| DEFINIZIONE \_ DEL TIPO DI CLASSE IMAGE \_ \_ \_ SYM <br/>   | 13 <br/>        | Voce Typedef. <br/>                                                                                                                                                                                                                                                                                                               |
| CLASSE \_ IMAGE SYM \_ NON DEFINITA \_ \_ STATIC <br/>  | 14 <br/>        | Dichiarazione di dati statici. <br/>                                                                                                                                                                                                                                                                                                     |
| TAG \_ DI ENUMERAZIONE DELLA CLASSE IMAGE \_ \_ SYM \_ <br/>          | 15 <br/>        | Voce tagname di tipo enumerata. <br/>                                                                                                                                                                                                                                                                                              |
| MEMBRO \_ DELLA CLASSE IMAGE SYM \_ \_ \_ \_ DELL'ENUMERAZIONE <br/>   | 16 <br/>        | Membro di un'enumerazione. Il campo Valore specifica il membro n. <br/>                                                                                                                                                                                                                                                         |
| IMAGE \_ SYM \_ CLASS \_ REGISTER \_ PARAM <br/>    | 17 <br/>        | Parametro register. <br/>                                                                                                                                                                                                                                                                                                          |
| CAMPO DI \_ BIT DELLA CLASSE IMAGE \_ \_ \_ SYM <br/>         | 18 <br/>        | Riferimento a un campo di bit. Il campo Valore specifica il bit n nel campo di bit. <br/>                                                                                                                                                                                                                                                |
| BLOCCO \_ DI CLASSI IMAGE \_ \_ SYM <br/>              | 100 <br/>       | Un record .bb (inizio del blocco) o .eb (fine del blocco). Il campo Valore è l'indirizzo rilocabile della posizione del codice. <br/>                                                                                                                                                                                                      |
| FUNZIONE \_ DELLA CLASSE IMAGE \_ \_ SYM <br/>           | 101 <br/>       | Valore utilizzato da Microsoft Tools per i record di simboli che definiscono l'estensione di una funzione: begin function (.bf), end function ( .ef ) e lines in function ( .lf ). Per i record con estensione lf, il campo Valore indica il numero di righe di origine nella funzione. Per i record con estensione ef, il campo Valore fornisce le dimensioni del codice della funzione. <br/> |
| FINE \_ STRUCT \_ DELLA CLASSE IMAGE \_ \_ \_ SYM <br/>    | 102 <br/>       | Voce di fine struttura. <br/>                                                                                                                                                                                                                                                                                                     |
| FILE DI \_ CLASSE IMAGE \_ SYM \_ <br/>               | 103 <br/>       | Valore utilizzato da Microsoft Tools, nonché dal formato COFF tradizionale, per il record di simboli del file di origine. Il simbolo è seguito da record ausiliari che deno il file. <br/>                                                                                                                                                       |
| SEZIONE IMAGE \_ SYM \_ CLASS \_ <br/>            | 104 <br/>       | Definizione di una sezione (gli strumenti Microsoft usano invece la classe di archiviazione STATIC). <br/>                                                                                                                                                                                                                                                  |
| CLASSE \_ IMAGE SYM \_ WEAK \_ \_ EXTERNAL <br/>     | 105 <br/>       | Oggetto esterno debole. Per altre informazioni, vedere [Formato ausiliario 3: esterni deboli.](#auxiliary-format-3-weak-externals) <br/>                                                                                                                                                                                                           |
| \_TOKEN CLR DELLA CLASSE \_ \_ IMAGE SYM \_ <br/>         | 107 <br/>       | Simbolo di token CLR. Il nome è una stringa ASCII costituita dal valore esadecimale del token. Per altre informazioni, vedere [Definizione di token CLR (solo oggetto).](#clr-token-definition-object-only) <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Record di simboli ausiliari

I record della tabella dei simboli ausiliari seguono e si applicano sempre ad alcuni record della tabella dei simboli standard. Un record ausiliario può avere qualsiasi formato che gli strumenti siano in grado di riconoscere, ma è necessario allocare 18 byte per essi in modo che la tabella dei simboli sia mantenuta come matrice di dimensioni normali. Attualmente, gli strumenti Microsoft riconoscono i formati ausiliari per i tipi di record seguenti: definizioni di funzioni, simboli di inizio e fine delle funzioni (con estensione bf ed ef), esterni deboli, nomi di file e definizioni di sezione.

La progettazione COFF tradizionale include anche formati di record ausiliari per matrici e strutture. Gli strumenti Microsoft non usano queste informazioni, ma posizionano tali informazioni simboliche Visual C++ formato di debug nelle sezioni di debug.

#### <a name="auxiliary-format-1-function-definitions"></a>Formato ausiliario 1: definizioni di funzione

Un record della tabella dei simboli contrassegna l'inizio di una definizione di funzione se contiene tutti gli elementi seguenti: una classe di archiviazione external (2), un valore Type che indica che si tratta di una funzione (0x20) e un numero di sezione maggiore di zero. Si noti che un record della tabella dei simboli con un numero di sezione UNDEFINED (0) non definisce la funzione e non dispone di un record ausiliario. I record di simboli di definizione della funzione sono seguiti da un record ausiliario nel formato descritto di seguito:



| Offset         | Dimensione          | Campo                             | Descrizione                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | TagIndex <br/>              | Indice della tabella dei simboli del record di simboli BF (begin function) corrispondente. <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | Dimensione del codice eseguibile per la funzione stessa. Se la funzione si trova in una sezione specifica, SizeOfRawData nell'intestazione di sezione è maggiore o uguale a questo campo, a seconda delle considerazioni sull'allineamento. <br/> |
| 8 <br/>  | 4 <br/> | PointerToLinenumber <br/>   | Offset di file della prima voce del numero di riga COFF per la funzione oppure zero se non ne esiste alcuna. Per altre informazioni, vedere [Numeri di riga COFF (deprecati).](#coff-line-numbers-deprecated) <br/>                          |
| 12 <br/> | 4 <br/> | PointerToNextFunction <br/> | Indice della tabella dei simboli del record per la funzione successiva. Se la funzione è l'ultima nella tabella dei simboli, questo campo è impostato su zero. <br/>                                                                           |
| 16 <br/> | 2 <br/> | Non utilizzato <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Formato ausiliario 2: simboli .bf ed .ef

Per ogni definizione di funzione nella tabella dei simboli, tre elementi descrivono l'inizio, la fine e il numero di righe. Ognuno di questi simboli ha la classe di archiviazione FUNCTION (101):

Un record di simboli denominato .bf (begin function). Il campo Valore non è usato.

Un record di simboli denominato .lf (righe nella funzione). Il campo Valore indica il numero di righe nella funzione.

Un record di simboli denominato .ef (fine della funzione). Il campo Valore ha lo stesso numero del campo Dimensioni totali nel record di simboli di definizione della funzione.

I record di simboli con estensione bf ed ef (ma non i record con estensione lf) sono seguiti da un record ausiliario con il formato seguente:



| Offset         | Dimensione          | Campo                                         | Descrizione                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Non utilizzato <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | Linenumber <br/>                        | Numero di riga ordinale effettivo (1, 2, 3 e così via) all'interno del file di origine, corrispondente al record BF o EF. <br/>                                               |
| 6 <br/>  | 6 <br/> | Non utilizzato <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | PointerToNextFunction (solo con estensione bf) <br/> | Indice della tabella dei simboli del record del simbolo BF successivo. Se la funzione è l'ultima nella tabella dei simboli, questo campo viene impostato su zero. Non viene usato per i record con estensione ef. <br/> |
| 16 <br/> | 2 <br/> | Non utilizzato <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Formato ausiliario 3: esterni deboli

Gli "esterni deboli" sono un meccanismo per i file oggetto che consente flessibilità in fase di collegamento. Un modulo può contenere un simbolo esterno non risolto (sym1), ma può anche includere un record ausiliario che indica che se sym1 non è presente in fase di collegamento, viene usato un altro simbolo esterno (sym2) per risolvere i riferimenti.

Se una definizione di sym1 è collegata, un riferimento esterno al simbolo viene risolto normalmente. Se una definizione di sym1 non è collegata, tutti i riferimenti all'esterno debole per sym1 fanno invece riferimento a sym2. Il simbolo esterno, sym2, deve essere sempre collegato. in genere è definito nel modulo che contiene il riferimento debole a sym1.

Gli esterni deboli sono rappresentati da un record di tabella dei simboli con classe di archiviazione EXTERNAL, numero di sezione UNDEF e valore zero. Il record del simbolo esterno debole è seguito da un record ausiliario con il formato seguente:



| Offset        | Dimensione           | Campo                       | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | TagIndex <br/>        | Indice della tabella dei simboli di sym2, il simbolo da collegare se sym1 non viene trovato. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Caratteristiche <br/> | Il valore IMAGE WEAK EXTERN SEARCH NOLIBRARY indica che non deve essere eseguita alcuna ricerca di \_ \_ libreria per \_ \_ sym1. <br/> Il valore IMAGE WEAK EXTERN SEARCH LIBRARY indica che deve essere eseguita una ricerca di \_ \_ libreria per \_ \_ sym1. <br/> Il valore IMAGE \_ WEAK \_ EXTERN SEARCH ALIAS indica che \_ \_ sym1 è un alias per sym2. <br/> |
| 8 <br/> | 10 <br/> | Non utilizzato <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Si noti che il campo Caratteristiche non è definito in WINNT. H; viene invece usato il campo Dimensioni totali.

#### <a name="auxiliary-format-4-files"></a>Formato ausiliario 4: file

Questo formato segue un record di tabella simboli con la classe di archiviazione FILE (103). Il nome del simbolo stesso deve essere file e il record ausiliario che lo segue fornisce il nome di un file di codice sorgente.



| Offset        | Dimensione           | Campo                 | Descrizione                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | File Name <br/> | Stringa ANSI che fornisce il nome del file di origine. Viene riempito con valori Null se è minore della lunghezza massima. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Formato ausiliario 5: definizioni di sezione

Questo formato segue un record di tabella simboli che definisce una sezione. Un record di questo tipo ha un nome di simbolo che è il nome di una sezione (ad esempio .text o .drectve) e ha la classe di archiviazione STATIC (3). Il record ausiliario fornisce informazioni sulla sezione a cui fa riferimento. Di conseguenza, duplica alcune delle informazioni nell'intestazione di sezione.



| Offset         | Dimensione          | Campo                           | Descrizione                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Length <br/>              | Dimensioni dei dati della sezione. uguale a SizeOfRawData nell'intestazione di sezione. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | NumberOfRelocations <br/> | Numero di voci di rilocazione per la sezione. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | NumberOfLinenumbers <br/> | Numero di voci del numero di riga per la sezione. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | Checksum <br/>            | Checksum per i dati comuni. È applicabile se il \_ flag IMAGE SCN \_ LNK \_ COMDAT è impostato nell'intestazione di sezione. Per altre informazioni, vedere [Sezioni COMDAT (solo oggetto).](#comdat-sections-object-only) <br/> |
| 12 <br/> | 2 <br/> | Numero <br/>              | Indice in base uno nella tabella di sezione per la sezione associata. Viene usato quando l'impostazione di selezione COMDAT è 5. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Selezione <br/>           | Numero di selezione COMDAT. Ciò è applicabile se la sezione è una sezione COMDAT. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | Non utilizzato <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>Sezioni COMDAT (solo oggetto)

Il campo Selezione del formato ausiliario della definizione di sezione è applicabile se la sezione è una sezione COMDAT. Una sezione COMDAT è una sezione che può essere definita da più di un file oggetto. (Il flag IMAGE \_ SCN \_ LNK \_ COMDAT è impostato nel campo Flag di sezione dell'intestazione di sezione. Il campo Selezione determina il modo in cui il linker risolve le più definizioni delle sezioni COMDAT.

Il primo simbolo con il valore di sezione della sezione COMDAT deve essere il simbolo di sezione. Questo simbolo ha il nome della sezione, il campo Value uguale a zero, il numero di sezione della sezione COMDAT in questione, il campo Type uguale a IMAGE SYM TYPE NULL, il campo Class uguale a IMAGE SYM CLASS STATIC e un \_ \_ record \_ \_ \_ \_ ausiliario. Il secondo simbolo è denominato "simbolo COMDAT" e viene usato dal linker insieme al campo Selection.

I valori per il campo Selezione sono indicati di seguito.



| Costante                                        | Valore         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ COMDAT \_ SELECT \_ NODUPLICATES <br/> | 1 <br/> | Se questo simbolo è già definito, il linker verifica un errore di moltiplicazione del simbolo definito. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ COMDAT \_ SELECT \_ ANY <br/>          | 2 <br/> | Qualsiasi sezione che definisce lo stesso simbolo COMDAT può essere collegata; le altre vengono rimosse. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ SELECT \_ SAME \_ SIZE <br/>   | 3 <br/> | Il linker sceglie una sezione arbitraria tra le definizioni per questo simbolo. Se tutte le definizioni non hanno le stesse dimensioni, viene generato un errore di tipo "simbolo definito moltiplicato". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ COMDAT \_ SELECT \_ EXACT \_ MATCH <br/> | 4 <br/> | Il linker sceglie una sezione arbitraria tra le definizioni per questo simbolo. Se tutte le definizioni non corrispondono esattamente, viene generato un errore di tipo "simbolo definito moltiplicato". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ SELECT \_ ASSOCIATIVE <br/>  | 5 <br/> | La sezione è collegata se è collegata un'altra sezione COMDAT. Questa altra sezione è indicata dal campo Number del record di simboli ausiliari per la definizione della sezione. Questa impostazione è utile per le definizioni che dispongono di componenti in più sezioni (ad esempio, codice in una e dati in un'altra), ma in cui tutti devono essere collegati o eliminati come set. L'altra sezione a cui è associata questa sezione deve essere una sezione COMDAT, che può essere un'altra sezione COMDAT associativa. La catena di associazioni di sezione di una sezione COMDAT associativa non può formare un ciclo. La catena di associazioni di sezione deve infine arrivare a una sezione COMDAT in cui non è impostato IMAGE \_ COMDAT \_ SELECT \_ ASSOCIATIVE. <br/> |
| IMAGE \_ COMDAT \_ SELECT \_ LARGEST <br/>      | 6 <br/> | Il linker sceglie la definizione più grande tra tutte le definizioni per questo simbolo. Se più definizioni hanno queste dimensioni, la scelta tra di esse è arbitraria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>Definizione del token CLR (solo oggetto)

Questo simbolo ausiliario segue in genere IMAGE \_ SYM \_ CLASS CLR \_ \_ TOKEN. Viene usato per associare un token allo spazio dei nomi della tabella dei simboli COFF.



| Offset        | Dimensione           | Campo                        | Descrizione                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bAuxType <br/>         | Deve essere IMAGE \_ AUX \_ SYMBOL TYPE TOKEN DEF \_ \_ \_ (1). <br/>                              |
| 1 <br/> | 1 <br/>  | bReserved <br/>        | Riservato, deve essere zero. <br/>                                                        |
| 2 <br/> | 4 <br/>  | SymbolTableIndex <br/> | Indice dei simboli del simbolo COFF a cui fa riferimento questa definizione di token CLR. <br/> |
| 6 <br/> | 12 <br/> |                              | Riservato, deve essere zero. <br/>                                                        |



 

### <a name="coff-string-table"></a>Tabella delle stringhe COFF

Subito dopo la tabella dei simboli COFF è riportata la tabella delle stringhe COFF. La posizione di questa tabella viene trovata prendendo l'indirizzo della tabella dei simboli nell'intestazione COFF e aggiungendo il numero di simboli moltiplicato per le dimensioni di un simbolo.

All'inizio della tabella delle stringhe COFF sono presenti 4 byte che contengono le dimensioni totali (in byte) del resto della tabella di stringhe. Questa dimensione include il campo delle dimensioni stesso, in modo che il valore in questa posizione sia 4 se non sono presenti stringhe.

Dopo le dimensioni sono presenti stringhe con terminazione Null a cui puntano i simboli nella tabella dei simboli COFF.

### <a name="the-attribute-certificate-table-image-only"></a>Tabella del certificato dell'attributo (solo immagine)

I certificati di attributo possono essere associati a un'immagine aggiungendo una tabella di certificati di attributo. La tabella del certificato dell'attributo è costituita da un set di voci di certificato di attributo contigue allineate a quadword. Per ottenere questo allineamento, viene inserita una spaziatura interna pari a zero tra la fine originale del file e l'inizio della tabella del certificato dell'attributo. Ogni voce del certificato dell'attributo contiene i campi seguenti.



| Offset       | Dimensione                         | Campo                       | Descrizione                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Specifica la lunghezza della voce del certificato dell'attributo. <br/>                                       |
| 4<br/> | 2<br/>                 | wRevision<br/>        | Contiene il numero di versione del certificato. Per informazioni dettagliate, vedere il testo seguente.<br/>                   |
| 6<br/> | 2<br/>                 | wCertificateType<br/> | Specifica il tipo di contenuto in bCertificate. Per informazioni dettagliate, vedere il testo seguente.<br/>             |
| 8<br/> | Vedere quanto segue<br/> | bCertificate<br/>     | Contiene un certificato, ad esempio una firma Authenticode. Per informazioni dettagliate, vedere il testo seguente.<br/> |



 

Il valore dell'indirizzo virtuale dalla voce Tabella certificati nella directory dei dati dell'intestazione facoltativa è un offset di file rispetto alla prima voce del certificato dell'attributo. Le voci successive sono accessibili facendo avanzare i byte dwLength di tale voce, arrotondati per esere a un multiplo di 8 byte, dall'inizio della voce del certificato dell'attributo corrente. Questa operazione continua fino a quando la somma dei valori dwLength arrotondati è uguale al valore Size della voce Certificates Table nella directory dei dati di intestazione facoltativi. Se la somma dei valori dwLength arrotondati non è uguale al valore di Size, la tabella del certificato dell'attributo o il campo Size è danneggiato.

Ad esempio, se la voce della tabella dei certificati della directory dei dati dell'intestazione facoltativa contiene:


```C++
virtual address = 0x5000
size = 0x1000
```



Il primo certificato inizia in corrispondenza 0x5000'offset dall'inizio del file su disco. Per avanzare in tutte le voci di certificato dell'attributo:

1.  Aggiungere il valore dwLength del primo attributo all'offset iniziale.
2.  Arrotondare il valore dal passaggio 1 al multiplo di 8 byte più vicino per trovare l'offset della seconda voce di certificato dell'attributo.
3.  Aggiungere il valore di offset dal passaggio 2 al valore dwLength della voce del certificato del secondo attributo e arrotondare per e per esere al multiplo di 8 byte più vicino per determinare l'offset della terza voce di certificato dell'attributo.
4.  Ripetere il passaggio 3 per ogni certificato successivo fino a quando l'offset calcolato non è uguale 0x6000 (0x5000 start + 0x1000 total size), che indica che è stata aperta l'intera tabella.

In alternativa, è possibile enumerare le voci del certificato chiamando la funzione **Win32 ImageEnumerateCertificates** in un ciclo. Per un collegamento alla pagina di riferimento della funzione, vedere [Riferimenti](#references).

Le voci della tabella dei certificati degli attributi possono contenere qualsiasi tipo di certificato, purché la voce abbia il valore dwLength corretto, un valore wRevision univoco e un valore wCertificateType univoco. Il tipo più comune di voce della tabella dei certificati è una struttura \_ WIN CERTIFICATE, documentata in Wintrust.h e illustrata nella parte restante di questa sezione.

Le opzioni per il membro \_ win CERTIFICATE **wRevision** includono( ma non sono limitate a) quanto segue.



| Valore             | Nome                                 | Note                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | WIN \_ CERT \_ REVISION \_ 1 \_ 0<br/> | Versione 1, versione legacy della struttura del \_ certificato Win. È supportato solo ai fini della verifica delle firme Authenticode legacy<br/> |
| 0x0200<br/> | WIN \_ CERT \_ REVISION \_ 2 \_ 0<br/> | La versione 2 è la versione corrente della struttura del \_ certificato Win. <br/>                                                                       |



 

Le opzioni per il membro \_ WIN CERTIFICATE **wCertificateType** includono (ma non solo) gli elementi nella tabella seguente. Si noti che alcuni valori non sono attualmente supportati.



| Valore             | Nome                                           | Note                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | TIPO \_ DI CERTIFICATO WIN \_ \_ X509 <br/>              | bCertificate contiene un certificato X.509 <br/> Non supportato<br/>         |
| 0x0002<br/> | WIN \_ CERT \_ TYPE \_ PKCS \_ SIGNED \_ DATA<br/> | bCertificate contiene una struttura PkcS \# 7 SignedData<br/>                         |
| 0x0003<br/> | TIPO \_ DI CERTIFICATO WIN RISERVATO \_ \_ \_ 1<br/>        | Riservato <br/>                                                                    |
| 0x0004<br/> | WIN \_ CERT \_ TYPE \_ TS \_ STACK \_ SIGNED<br/>  | Firma del certificato dello stack di protocolli di Terminal Server <br/> Non supportato<br/> |



 

Il membro bCertificate della struttura WIN CERTIFICATE contiene una matrice di byte a lunghezza variabile con il tipo \_ di contenuto specificato da **wCertificateType**.  Il tipo supportato da Authenticode è WIN \_ CERT \_ TYPE \_ PKCS \_ SIGNED \_ DATA, una struttura PKCS \# 7 **SignedData.** Per informazioni dettagliate sul formato di firma digitale Authenticode, vedere Windows [Authenticode Portable Executable Signature Format](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Se il **contenuto bCertificate** non termina su un limite di quattro parole, la voce del certificato dell'attributo viene riempita con zeri, dalla fine di **bCertificate** al limite successivo della quadword.

Il **valore dwLength** è la lunghezza della struttura WIN CERTIFICATE finalizzata \_ e viene calcolato come:

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Questa lunghezza deve includere le dimensioni di qualsiasi spaziatura interna usata per soddisfare il requisito che ogni struttura WIN \_ CERTIFICATE sia allineata a quattro parole:

` dwLength += (8 - (dwLength & 7)) & 7;`

La **dimensione della tabella dei** certificati specificata nella voce Certificates **Table** (Tabella certificati) nelle directory dei dati di intestazione [facoltative (solo immagine)](#optional-header-data-directories-image-only)include la spaziatura interna.

Per altre informazioni sull'uso dell'API ImageHlp per enumerare, aggiungere e rimuovere certificati da file PE, vedere [Funzioni imageHlp](imagehlp-functions.md).

#### <a name="certificate-data"></a>Dati certificato

Come indicato nella sezione precedente, i certificati nella tabella dei certificati dell'attributo possono contenere qualsiasi tipo di certificato. I certificati che garantiscono l'integrità di un file PE possono includere un hash di immagine PE.

Un hash di immagine PE (o hash di file) è simile a un checksum di file in cui l'algoritmo hash produce un digest del messaggio correlato all'integrità di un file. Tuttavia, un checksum viene generato da un algoritmo semplice e viene usato principalmente per rilevare se un blocco di memoria su disco è andato storto e i valori archiviati sono danneggiati. Un hash di file è simile a un checksum in quanto rileva anche il danneggiamento dei file. Tuttavia, a differenza della maggior parte degli algoritmi di checksum, è molto difficile modificare un file senza modificare l'hash del file dal valore originale non modificato. Un hash di file può quindi essere usato per rilevare modifiche intenzionali e anche sottili a un file, ad esempio quelle introdotte da virus, hacker o programmi Trojan horse.

Se incluso in un certificato, il digest dell'immagine deve escludere determinati campi nell'immagine PE, ad esempio la voce Checksum e la tabella dei certificati nelle directory dei dati di intestazione facoltative. Ciò è dovuto al fatto che l'aggiunta di un certificato modifica questi campi e determina il calcolo di un valore hash diverso.

La funzione Win32 **ImageGetDigestStream** fornisce un flusso di dati da un file PE di destinazione con cui eseguire l'hashing delle funzioni. Questo flusso di dati rimane coerente quando i certificati vengono aggiunti o rimossi da un file PE. In base ai parametri passati a **ImageGetDigestStream,** altri dati dell'immagine PE possono essere omessi dal calcolo hash. Per un collegamento alla pagina di riferimento della funzione, vedere [Riferimenti](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load importare tabelle (solo immagine)

Queste tabelle sono state aggiunte all'immagine per supportare un meccanismo uniforme che consente alle applicazioni di ritardare il caricamento di una DLL fino alla prima chiamata a tale DLL. Il layout delle tabelle corrisponde a quello delle tabelle di importazione tradizionali descritte nella sezione 6.4, [Sezione .idata](#the-idata-section)." Di seguito vengono illustrati solo alcuni dettagli.

#### <a name="the-delay-load-directory-table"></a>Tabella Delay-Load directory

La tabella della directory delay-load è la controparte della tabella della directory di importazione. Può essere recuperato tramite la voce Delay Import Descriptor nell'elenco delle directory dei dati di intestazione facoltative (offset 200). La tabella viene disposta come segue:



| Offset         | Dimensione          | Campo                                  | Descrizione                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Attributi <br/>                 | Deve essere zero. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Nome <br/>                       | RVA del nome della DLL da caricare. Il nome si trova nella sezione dei dati di sola lettura dell'immagine. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Handle del modulo <br/>              | Valore RVA dell'handle del modulo (nella sezione dei dati dell'immagine) della DLL da caricare in ritardo. Viene usato per l'archiviazione dalla routine fornita per gestire il caricamento ritardato. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Tabella degli indirizzi di importazione ritardata <br/> | Valore RVA della tabella degli indirizzi di importazione con caricamento ritardato. Per altre informazioni, vedere [Delay Import Address Table (IAT)](#delay-import-address-table). <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Ritardare la tabella dei nomi di importazione <br/>    | Valore RVA della tabella dei nomi di caricamento ritardato, che contiene i nomi delle importazioni che potrebbero dover essere caricate. Corrisponde al layout della tabella dei nomi di importazione. Per altre informazioni, vedere [Hint/Name Table](#hintname-table).<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Tabella di importazione con ritardo associato <br/>   | Valore RVA della tabella degli indirizzi di caricamento ritardato associato, se esistente. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Scarica tabella di importazione ritardata <br/>  | Valore RVA della tabella degli indirizzi di caricamento ritardato di scaricamento, se esistente. Si tratta di una copia esatta della tabella degli indirizzi di importazione ritardata. Se il chiamante scarica la DLL, questa tabella deve essere copiata sulla tabella degli indirizzi di importazione ritardata in modo che le chiamate successive alla DLL continuino a usare correttamente il meccanismo di thunking. <br/> |
| 28 <br/> | 4 <br/> | Timestamp <br/>                 | Timestamp della DLL a cui è stata associata l'immagine. <br/>                                                                                                                                                                                                                                                     |



 

Le tabelle a cui si fa riferimento in questa struttura di dati sono organizzate e ordinate esattamente come le relative controparti per le importazioni tradizionali. Per informazioni dettagliate, [vedere la sezione .idata](#the-idata-section).

#### <a name="attributes"></a>Attributi

Non sono ancora definiti flag di attributo. Il linker imposta questo campo su zero nell'immagine. Questo campo può essere usato per estendere il record indicando la presenza di nuovi campi oppure può essere usato per indicare comportamenti alle funzioni helper delay o unload.

#### <a name="name"></a>Nome

Il nome della DLL da caricare in ritardo si trova nella sezione dei dati di sola lettura dell'immagine. Viene fatto riferimento tramite il campo szName.

#### <a name="module-handle"></a>Handle del modulo

L'handle della DLL da caricare in ritardo si trova nella sezione dei dati dell'immagine. Il campo phmod punta all'handle. L'helper delay-load fornito usa questo percorso per archiviare l'handle per la DLL caricata.

#### <a name="delay-import-address-table"></a>Tabella degli indirizzi di importazione ritardata

Il descrittore di importazione ritardata fa riferimento alla tabella degli indirizzi di importazione ritardata tramite il campo pIAT. L'helper di caricamento ritardato aggiorna questi puntatori con i punti di ingresso reali in modo che i thunk non siano più nel ciclo chiamante. I puntatori a funzione sono accessibili tramite l'espressione `pINT->u1.Function` .

#### <a name="delay-import-name-table"></a>Ritardare la tabella dei nomi di importazione

La tabella dei nomi di importazione ritardata (INT) contiene i nomi delle importazioni che potrebbero richiedere il caricamento. Sono ordinati nello stesso modo dei puntatori a funzione in IAT. Sono costituite dalle stesse strutture dell'INT standard e sono accessibili tramite l'espressione `pINT->u1.AddressOfData->Name[0]` .

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Tabella degli indirizzi di importazione con associazione ritardata e timestamp

La tabella degli indirizzi di importazione con associazione a ritardo è una tabella facoltativa di elementi IMAGE THUNK DATA usata insieme al campo timestamp della tabella della directory delay-load da una fase di associazione \_ \_ post-elaborazione.

#### <a name="delay-unload-import-address-table"></a>Ritardare lo scaricamento della tabella degli indirizzi di importazione

La tabella degli indirizzi di importazione con scaricamento ritardato è una tabella facoltativa di elementi IMAGE THUNK DATA che il codice di scaricamento usa per gestire una richiesta \_ \_ di scaricamento esplicita. È costituito da dati inizializzati nella sezione di sola lettura che è una copia esatta dell'IAT originale che ha fatto riferimento al codice ai thunk di caricamento ritardato. Nella richiesta di scaricamento, la libreria può essere liberata, il phmod cancellato e l'interfaccia utente scritta su IAT per ripristinare tutto allo \* stato di precaricamento.

## <a name="special-sections"></a>Sezioni speciali

- [Sezione .debug](#the-debug-section)
  - [Directory di debug (solo immagine)](#debug-directory-image-only)
  - [Tipo di debug](#debug-type)
  - [.debug$F (solo oggetto)](#debugf-object-only)
  - [.debug$S (solo oggetto)](#debugs-object-only)
  - [.debug$P (solo oggetto)](#debugp-object-only)
  - [.debug$T (solo oggetto)](#debugt-object-only)
  - [Supporto del linker per le informazioni di debug Microsoft](#linker-support-for-microsoft-debug-information)
- [Sezione .drectve (solo oggetto)](#the-drectve-section-object-only)
- [Sezione .edata (solo immagine)](#the-edata-section-image-only)
  - [Esporta tabella directory](#export-directory-table)
  - [Tabella degli indirizzi di esportazione](#export-address-table)
  - [Tabella dei puntatori per l'esportazione dei nomi](#export-name-pointer-table)
  - [Esporta tabella ordinale](#export-ordinal-table)
  - [Tabella dei nomi di esportazione](#export-name-table)
- [Sezione .idata](#the-idata-section)
  - [Importa tabella directory](#import-directory-table)
  - [Importa tabella di ricerca](#import-lookup-table)
  - [Tabella hint/nome](#hintname-table)
  - [Importa tabella indirizzi](#delay-import-address-table)
- [Sezione .pdata](#the-pdata-section)
- [Sezione .reloc (solo immagine)](#the-reloc-section-image-only)
  - [Blocco di rilocazione di base](#base-relocation-block)
  - [Tipi di rilocazione di base](#base-relocation-types)
- [Sezione .tls](#the-tls-section)
  - [The TLS Directory](#the-tls-directory)
  - [Funzioni di callback TLS](#tls-callback-functions)
- [Struttura di configurazione del caricamento (solo immagine)](#the-load-configuration-structure-image-only)
  - [Caricare la directory di configurazione](#load-configuration-directory)
  - [Caricare il layout di configurazione](#load-configuration-layout)
- [Sezione .rsrc](#the-rsrc-section)
  - [Tabella della directory delle risorse](#resource-directory-table)
  - [Voci della directory delle risorse](#resource-directory-entries)
  - [Stringa della directory delle risorse](#resource-directory-string)
  - [Immissione di dati delle risorse](#resource-data-entry)
- [Sezione .cormeta (solo oggetto)](#the-cormeta-section-object-only)
- [Sezione .sxdata](#the-sxdata-section)

Le sezioni COFF tipiche contengono codice o dati che i linker e i caricatori Microsoft Win32 elaborano senza una conoscenza specifica del contenuto della sezione. Il contenuto è rilevante solo per l'applicazione che viene collegata o eseguita.

Tuttavia, alcune sezioni COFF hanno significati speciali quando si trovano nei file oggetto o nei file di immagine. Gli strumenti e i caricatori riconoscono queste sezioni perché hanno flag speciali impostati nell'intestazione di sezione, perché le posizioni speciali nell'intestazione facoltativa dell'immagine puntano a tali sezioni o perché il nome della sezione indica una funzione speciale della sezione. Anche se il nome della sezione non indica una funzione speciale della sezione, il nome della sezione viene determinato per convenzione, quindi gli autori di questa specifica possono fare riferimento a un nome di sezione in tutti i casi.

Le sezioni riservate e i relativi attributi sono descritti nella tabella seguente, seguiti da descrizioni dettagliate per i tipi di sezione persistenti nei file eseguibili e i tipi di sezione che contengono metadati per le estensioni.



| Nome della sezione          | Content                                                                                                                                                                  | Caratteristiche                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bss <br/>      | Dati non inizializzati (formato gratuito) <br/>                                                                                                                             | IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                               |
| .cormeta <br/>  | Metadati CLR che indicano che il file oggetto contiene codice gestito <br/>                                                                                       | IMAGE \_ SCN \_ LNK \_ INFO <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .data <br/>     | Dati inizializzati (formato gratuito) <br/>                                                                                                                               | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .debug$F <br/>  | Informazioni di debug FPO generate (solo oggetti, solo architettura x86 e ora obsolete) <br/>                                                                       | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$P <br/>  | Tipi di debug precompilati (solo oggetto) <br/>                                                                                                                        | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$S <br/>  | Simboli di debug (solo oggetto) <br/>                                                                                                                                  | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$T <br/>  | Tipi di debug (solo oggetto) <br/>                                                                                                                                    | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .drective <br/> | Opzioni del linker <br/>                                                                                                                                               | IMAGE \_ SCN \_ LNK \_ INFO <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .edata <br/>    | Esportare tabelle <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .idata <br/>    | Importare tabelle <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .idlsym <br/>   | Include seH registrato (solo immagine) per supportare gli attributi IDL. Per informazioni, vedere "Attributi IDL" in [Riferimenti](#references) alla fine di questo argomento. <br/> | IMAGE \_ SCN \_ LNK \_ INFO <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| PDATA <br/>    | Informazioni sulle eccezioni <br/>                                                                                                                                        | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .rdata <br/>    | Dati inizializzati di sola lettura <br/>                                                                                                                                   | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .reloc <br/>    | Rilocazioni di immagini <br/>                                                                                                                                            | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .rsrc <br/>     | Directory delle risorse <br/>                                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .sbss <br/>     | Dati non inizializzati relativi ai Criteri di gruppo (formato gratuito) <br/>                                                                                                                 | IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM READ IMAGE \_ \| \_ SCN \_ MEM WRITE IMAGE \_ \| \_ SCN \_ GPREL Il flag GPREL IMAGE SCN \_ DEVE \_ essere impostato solo per le architetture IA64. Questo flag non è valido per altre architetture. Il flag GPREL IMAGE SCN è solo per i file oggetto. Quando questo tipo di sezione viene visualizzato in un file di immagine, il \_ \_ flag GPREL DI IMAGE SCN non \_ deve essere \_ impostato. <br/> |
| .sdata <br/>    | Dati inizializzati relativi ai Criteri di gruppo (formato gratuito) <br/>                                                                                                                   | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM READ IMAGE \_ \| \_ SCN WRITE IMAGE \_ \_ \| \_ SCN \_ GPREL Il flag GPREL IMAGE SCN \_ DEVE \_ essere impostato solo per le architetture IA64. Questo flag non è valido per altre architetture. Il flag GPREL IMAGE SCN è solo per i file oggetto. Quando questo tipo di sezione viene visualizzato in un file di immagine, il \_ \_ flag GPREL DI IMAGE SCN non \_ deve essere \_ impostato. <br/>   |
| .srdata <br/>   | Dati di sola lettura relativi ai Criteri di gruppo (formato gratuito) <br/>                                                                                                                     | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN \_ MEM READ IMAGE \_ \| SCN GPREL Il flag GPREL IMAGE SCN \_ deve \_ \_ \_ essere impostato solo per le architetture IA64. Questo flag non è valido per altre architetture. Il flag GPREL IMAGE SCN è solo per i file oggetto. Quando questo tipo di sezione viene visualizzato in un file di immagine, il \_ \_ flag GPREL DI IMAGE SCN non \_ deve essere \_ impostato. <br/>                             |
| .sxdata <br/>   | Dati del gestore eccezioni registrati (solo formato gratuito e x86/oggetto) <br/>                                                                                          | IMAGE \_ SCN LNK INFO Contiene l'indice dei simboli di ognuno dei gestori eccezioni a cui fa riferimento \_ il codice nel file \_ oggetto. Il simbolo può essere per un simbolo UNDEF o uno definito in tale modulo. <br/>                                                                                                                                                                     |
| text <br/>     | Codice eseguibile (formato gratuito) <br/>                                                                                                                                | IMMAGINE \_ SCN \_ CNT \_ CODE IMAGE \| \_ SCN \_ MEM EXECUTE \_ \| IIMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                           |
| .tls <br/>      | Archiviazione locale di thread (solo oggetto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .tls$ <br/>     | Archiviazione locale di thread (solo oggetto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .vsdata <br/>   | Dati inizializzati relativi ai Criteri di gruppo (formato gratuito e solo per architetture ARM, SH4 e Thumb) <br/>                                                                    | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .xdata <br/>    | Informazioni sull'eccezione (formato gratuito) <br/>                                                                                                                          | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |



 

Alcune delle sezioni elencate di seguito sono contrassegnate rispettivamente come "solo oggetto" o "solo immagine" per indicare che la semantica speciale è rilevante solo per i file oggetto o i file di immagine. Una sezione contrassegnata come "solo immagine" potrebbe comunque essere visualizzata in un file oggetto come modo per accedere al file di immagine, ma la sezione non ha alcun significato particolare per il linker, solo per il caricatore del file di immagine.

### <a name="the-debug-section"></a>Sezione .debug

La sezione .debug viene usata nei file oggetto per contenere informazioni di debug generate dal compilatore e nei file di immagine per contenere tutte le informazioni di debug generate. Questa sezione descrive la creazione di pacchetti di informazioni di debug nei file oggetto e immagine.

La sezione successiva descrive il formato della directory di debug, che può essere in qualsiasi punto dell'immagine. Le sezioni successive descrivono i "gruppi" nei file oggetto che contengono informazioni di debug.

L'impostazione predefinita per il linker è che non viene eseguito il mapping delle informazioni di debug nello spazio degli indirizzi dell'immagine. Una sezione .debug esiste solo quando viene eseguito il mapping delle informazioni di debug nello spazio degli indirizzi.

#### <a name="debug-directory-image-only"></a>Directory di debug (solo immagine)

I file di immagine contengono una directory di debug facoltativa che indica quale forma di informazioni di debug è presente e dove si trova. Questa directory è costituita da una matrice di voci della directory di debug la cui posizione e le cui dimensioni sono indicate nell'intestazione facoltativa dell'immagine.

La directory di debug può essere inclusa in una sezione .debug eliminabile (se presente) oppure in qualsiasi altra sezione del file di immagine oppure non essere inclusa in una sezione.

Ogni voce della directory di debug identifica il percorso e le dimensioni di un blocco di informazioni di debug. L'RVA specificata può essere zero se le informazioni di debug non sono coperte da un'intestazione di sezione, ovvero risiede nel file di immagine e non viene mappata nello spazio degli indirizzi di run-time. Se è stato eseguito il mapping, l'RVA è il relativo indirizzo.

Una voce della directory di debug ha il formato seguente:



| Offset         | Dimensione          | Campo                        | Descrizione                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Caratteristiche <br/>  | Riservato, deve essere zero. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | Ora e data di creazione dei dati di debug. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | Numero di versione principale del formato dati di debug. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | Numero di versione secondaria del formato dati di debug. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | Tipo <br/>             | Formato delle informazioni di debug. Questo campo consente il supporto di più debugger. Per altre informazioni, vedere [Tipo di debug](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | SizeOfData <br/>       | Dimensioni dei dati di debug (senza includere la directory di debug stessa). <br/>                                                                     |
| 20 <br/> | 4 <br/> | AddressOfRawData <br/> | Indirizzo dei dati di debug al momento del caricamento, relativo alla base dell'immagine. <br/>                                                                     |
| 24 <br/> | 4 <br/> | PointerToRawData <br/> | Puntatore di file ai dati di debug. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Tipo di debug

Per il campo Tipo della voce della directory di debug sono definiti i valori seguenti:



| Costante                                        | Valore          | Descrizione                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO \_ DI DEBUG IMMAGINE \_ \_ SCONOSCIUTO <br/>         | 0 <br/>  | Valore sconosciuto ignorato da tutti gli strumenti. <br/>                                                                                                                                                       |
| COFF DI \_ TIPO DI DEBUG \_ \_ IMMAGINE <br/>            | 1 <br/>  | Informazioni di debug COFF (numeri di riga, tabella dei simboli e tabella di stringhe). Questo tipo di informazioni di debug è indicato anche dai campi nelle intestazioni dei file. <br/>                                          |
| TIPO \_ DI DEBUG IMMAGINE \_ \_ CODEVIEW <br/>        | 2 <br/>  | Informazioni Visual C++ di debug. <br/>                                                                                                                                                                    |
| FPO \_ TIPO DI DEBUG \_ \_ IMMAGINE <br/>             | 3 <br/>  | Informazioni sull'omissione del puntatore ai frame (FPO). Queste informazioni indica al debugger come interpretare gli stack frame non standard, che usano il registro EBP per uno scopo diverso da come puntatore a frame. <br/> |
| TIPO \_ DI DEBUG IMMAGINE \_ \_ MISC <br/>            | 4 <br/>  | Percorso del file DBG. <br/>                                                                                                                                                                            |
| ECCEZIONE DEL \_ TIPO DI DEBUG \_ \_ DELL'IMMAGINE <br/>       | 5 <br/>  | Copia della sezione .pdata. <br/>                                                                                                                                                                            |
| CORREZIONE DEL \_ TIPO DI DEBUG DELLE \_ \_ IMMAGINI <br/>           | 6 <br/>  | Riservato. <br/>                                                                                                                                                                                            |
| TIPO \_ DI DEBUG IMMAGINE DA \_ \_ OMAP A \_ \_ SRC <br/>   | 7 <br/>  | Mapping da un'RVA nell'immagine a un'RVA nell'immagine di origine. <br/>                                                                                                                                          |
| TIPO \_ DI DEBUG IMMAGINE \_ \_ OMAP DA \_ \_ SRC <br/> | 8 <br/>  | Mapping da un'RVA nell'immagine di origine a un'RVA nell'immagine. <br/>                                                                                                                                          |
| TIPO \_ DI DEBUG IMMAGINE \_ \_ BORLAND <br/>         | 9 <br/>  | Riservato per Borland. <br/>                                                                                                                                                                                |
| TIPO \_ DI DEBUG IMMAGINE \_ \_ RESERVED10 <br/>      | 10 <br/> | Riservato. <br/>                                                                                                                                                                                            |
| \_CLSID DEL TIPO DI DEBUG \_ \_ DELL'IMMAGINE <br/>           | 11 <br/> | Riservato. <br/>                                                                                                                                                                                            |
| REPRO \_ DEL TIPO DI DEBUG \_ \_ DELL'IMMAGINE <br/>           | 16 <br/> | Determinismo o riproducibilità pe. <br/>                                                                                                                                                                   |
| TIPO \_ DI DEBUG IMMAGINE EX \_ \_ \_ DLLCHARACTERISTICS | 20 | Bit delle caratteristiche dll estese. |



 

Se il campo Tipo è impostato su IMAGE \_ DEBUG \_ TYPE FPO, i dati non elaborati di debug sono una matrice in cui ogni membro descrive la stack frame \_ di una funzione. Non tutte le funzioni nel file di immagine devono avere informazioni FPO definite, anche se il tipo di debug è FPO. Si presuppone che le funzioni che non dispongono di informazioni FPO presentino stack frame normali. Il formato delle informazioni FPO è il seguente:


```C++
#define FRAME_FPO   0               
#define FRAME_TRAP  1
#define FRAME_TSS   2
               
typedef struct _FPO_DATA {
    DWORD       ulOffStart;            // offset 1st byte of function code
    DWORD       cbProcSize;            // # bytes in function
    DWORD       cdwLocals;             // # bytes in locals/4
    WORD        cdwParams;             // # bytes in params/4
    WORD        cbProlog : 8;          // # bytes in prolog
    WORD        cbRegs   : 3;          // # regs saved
    WORD        fHasSEH  : 1;          // TRUE if SEH in func
    WORD        fUseBP   : 1;          // TRUE if EBP has been allocated
    WORD        reserved : 1;          // reserved for future use
    WORD        cbFrame  : 2;          // frame type
} FPO_DATA;
```



La presenza di una voce di tipo IMAGE DEBUG TYPE REPRO indica che il file PE è compilato in modo da ottenere \_ \_ \_ determinismo o riproducibilità. Se l'input non cambia, il file PE di output è sempre identico bit per bit, indipendentemente da quando o dove viene prodotto il file PE. Vari campi timestamp di data/ora nel file PE vengono riempiti con parte o tutti i bit di un valore hash calcolato che usa il contenuto del file PE come input e pertanto non rappresentano più la data e l'ora effettive quando viene prodotto un file PE o dati specifici correlati all'interno del file PE. I dati non elaborati di questa voce di debug possono essere vuoti o contenere un valore hash calcolato preceduto da un valore a quattro byte che rappresenta la lunghezza del valore hash.

Se il campo Tipo è impostato su IMAGE \_ DEBUG \_ TYPE EX \_ DLLCHARACTERISTICS, i dati non elaborati di debug contengono bit di caratteristiche DLL estese, oltre a quelli che possono essere impostati \_ nell'intestazione facoltativa dell'immagine. Vedere [Le caratteristiche dll](#dll-characteristics) nella sezione Intestazione facoltativa Windows-Specific campi [(solo immagine)](#optional-header-windows-specific-fields-image-only).

##### <a name="extended-dll-characteristics"></a>Caratteristiche dll estese

I valori seguenti sono definiti per i bit delle caratteristiche dll estese.

| Costante | Valore | Descrizione |
|-|-|-|
| IMAGE \_ DLLCHARACTERISTICS \_ EX \_ CET \_ COMPAT | 0x0001 | L'immagine è compatibile con CET. |

#### <a name="debugf-object-only"></a>.debug$F (solo oggetto)

I dati in questa sezione sono stati sostituiti in Visual C++ versione 7.0 e successive da un set più ampio di dati che viene generato in una sottosezione **.debug$S.**

I file oggetto possono contenere sezioni .debug$F il cui contenuto è uno o più record FPO \_ DATA (informazioni sull'omissione dei puntatori ai frame). Vedere "IMAGE \_ DEBUG \_ TYPE \_ FPO" in [Tipo di debug](#debug-type).

Il linker riconosce questi **record .debug$F.** Se vengono generate informazioni di debug, il linker ordina i record FPO DATA in base alla procedura RVA e genera una \_ voce di directory di debug per essi.

Il compilatore non deve generare record FPO per le procedure con un formato frame standard.

#### <a name="debugs-object-only"></a>.debug$S (solo oggetto)

Questa sezione contiene informazioni Visual C++ di debug (informazioni simboliche).

#### <a name="debugp-object-only"></a>.debug$P (solo oggetto)

Questa sezione contiene Visual C++ di debug (informazioni precompilate). Si tratta di tipi condivisi tra tutti gli oggetti compilati usando l'intestazione precompilata generata con questo oggetto.

#### <a name="debugt-object-only"></a>.debug$T (solo oggetto)

Questa sezione contiene informazioni Visual C++ di debug (informazioni sul tipo).

#### <a name="linker-support-for-microsoft-debug-information"></a>Supporto del linker per le informazioni di debug Microsoft

Per supportare le informazioni di debug, il linker:

-   Raccoglie tutti i dati di debug pertinenti dalle sezioni **.debug$F**, **debug$S,** **.debug$P** e **.debug$T.**

-   Elabora i dati insieme alle informazioni di debug generate dal linker nel file PDB e crea una voce di directory di debug a cui fare riferimento.

### <a name="the-drectve-section-object-only"></a>Sezione .drectve (solo oggetto)

Una sezione è una sezione di direttiva se il flag IMAGE SCN LNK INFO è impostato nell'intestazione di sezione e ha il nome \_ \_ della sezione \_ **.drectve.** Il linker rimuove una **sezione con estensione drectve** dopo l'elaborazione delle informazioni, quindi la sezione non viene visualizzata nel file di immagine collegato.

Una **sezione con estensione drectve** è costituita da una stringa di testo che può essere codificata come ANSI o UTF-8. Se il marcatore dell'ordine dei byte UTF-8 (BOM, un prefisso a tre byte costituito da 0xEF, 0xBB e 0xBF) non è presente, la stringa di direttiva viene interpretata come ANSI. La stringa di direttiva è una serie di opzioni del linker separate da spazi. Ogni opzione contiene un trattino, il nome dell'opzione e qualsiasi attributo appropriato. Se un'opzione contiene spazi, l'opzione deve essere racchiusa tra virgolette. La **sezione .drectve** non deve avere rilocazioni o numeri di riga.

### <a name="the-edata-section-image-only"></a>Sezione .edata (solo immagine)

La sezione relativa all'esportazione dei dati, denominata .edata, contiene informazioni sui simboli a cui altre immagini possono accedere tramite collegamento dinamico. I simboli esportati si trovano in genere nelle DLL, ma possono anche importare simboli.

Di seguito è riportata una panoramica della struttura generale della sezione relativa all'esportazione. Le tabelle descritte sono in genere contigue nel file nell'ordine indicato (anche se non è obbligatorio). Solo la tabella della directory di esportazione e la tabella degli indirizzi di esportazione sono necessarie per esportare i simboli come ordinali. Un ordinale è un'esportazione a cui accede direttamente l'indice della tabella degli indirizzi di esportazione. La tabella dei puntatori al nome, la tabella ordinale e la tabella dei nomi di esportazione esistono tutte per supportare l'uso dei nomi di esportazione.



| Nome tabella                         | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esporta tabella directory <br/> | Tabella con una sola riga (a differenza della directory di debug). Questa tabella indica i percorsi e le dimensioni delle altre tabelle di esportazione. <br/>                                                                                                                                                                                                               |
| Tabella degli indirizzi di esportazione <br/>   | Matrice di RVA di simboli esportati. Questi sono gli indirizzi effettivi delle funzioni e dei dati esportati all'interno del codice eseguibile e delle sezioni dei dati. Altri file di immagine possono importare un simbolo usando un indice in questa tabella (ordinale) o, facoltativamente, usando il nome pubblico che corrisponde all'ordinale se è definito un nome pubblico. <br/> |
| Tabella del puntatore del nome <br/>     | Matrice di puntatori ai nomi di esportazione pubblici, ordinati in ordine crescente. <br/>                                                                                                                                                                                                                                                                    |
| Tabella ordinale <br/>          | Matrice degli ordinali che corrispondono ai membri della tabella del puntatore del nome. La corrispondenza è in base alla posizione; Pertanto, la tabella del puntatore del nome e la tabella ordinale devono avere lo stesso numero di membri. Ogni ordinale è un indice nella tabella degli indirizzi di esportazione. <br/>                                                                        |
| Tabella dei nomi di esportazione <br/>      | Serie di stringhe ASCII con terminazione Null. I membri della tabella del puntatore del nome puntano a questa area. Questi nomi sono i nomi pubblici tramite i quali i simboli vengono importati ed esportati. non sono necessariamente uguali ai nomi privati usati all'interno del file di immagine. <br/>                                                           |



 

Quando un altro file di immagine importa un simbolo in base al nome, il caricatore Win32 cerca una stringa corrispondente nella tabella dei puntatori dei nomi. Se viene trovata una stringa corrispondente, l'ordinale associato viene identificato cercando il membro corrispondente nella tabella ordinale, ovvero il membro della tabella ordinale con lo stesso indice del puntatore di stringa presente nella tabella del puntatore del nome. L'ordinale risultante è un indice nella tabella degli indirizzi di esportazione, che fornisce la posizione effettiva del simbolo desiderato. Ogni simbolo di esportazione è accessibile da un numero ordinale.

Quando un altro file di immagine importa un simbolo in base al numero ordinale, non è necessario cercare una stringa corrispondente nella tabella dei puntatori dei nomi. L'uso diretto di un ordinale è quindi più efficiente. Tuttavia, un nome di esportazione è più facile da ricordare e non richiede all'utente di conoscere l'indice della tabella per il simbolo.

#### <a name="export-directory-table"></a>Esporta tabella directory

Le informazioni sui simboli di esportazione iniziano con la tabella della directory di esportazione, che descrive il resto delle informazioni sui simboli di esportazione. La tabella della directory di esportazione contiene le informazioni sull'indirizzo usate per risolvere le importazioni nei punti di ingresso all'interno dell'immagine.



| Offset         | Dimensione          | Campo                                | Descrizione                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Flag di esportazione <br/>             | Riservato, deve essere 0. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Timestamp data/ora <br/>          | Ora e data di creazione dei dati di esportazione. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Versione principale <br/>            | Numero di versione principale. I numeri di versione principale e secondaria possono essere impostati dall'utente. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Versione secondaria <br/>            | Numero di versione secondario. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Assegnare il nome RVA <br/>                 | Indirizzo della stringa ASCII che contiene il nome della DLL. Questo indirizzo è relativo alla base dell'immagine. <br/>                                                |
| 16 <br/> | 4 <br/> | Base ordinale <br/>             | Numero ordinale iniziale per le esportazioni in questa immagine. Questo campo specifica il numero ordinale iniziale per la tabella degli indirizzi di esportazione. In genere è impostato su 1. <br/> |
| 20 <br/> | 4 <br/> | Voci della tabella address <br/>    | Numero di voci nella tabella degli indirizzi di esportazione. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Numero di puntatori ai nomi <br/>  | Numero di voci nella tabella del puntatore del nome. Questo è anche il numero di voci nella tabella ordinale. <br/>                                                     |
| 28 <br/> | 4 <br/> | RVA della tabella degli indirizzi di esportazione <br/> | Indirizzo della tabella degli indirizzi di esportazione, relativo alla base dell'immagine. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | RVA del puntatore del nome <br/>         | Indirizzo della tabella del puntatore del nome di esportazione, relativo alla base dell'immagine. Le dimensioni della tabella sono specificate dal campo Numero di puntatori nome. <br/>                       |
| 36 <br/> | 4 <br/> | RVA tabella ordinale <br/>        | Indirizzo della tabella ordinale, relativo alla base dell'immagine. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Tabella degli indirizzi di esportazione

La tabella degli indirizzi di esportazione contiene l'indirizzo dei punti di ingresso esportati, i dati esportati e i valori assoluti. Un numero ordinale viene usato come indice nella tabella degli indirizzi di esportazione.

Ogni voce nella tabella degli indirizzi di esportazione è un campo che usa uno dei due formati nella tabella seguente. Se l'indirizzo specificato non è all'interno della sezione export (come definito dall'indirizzo e dalla lunghezza indicati nell'intestazione facoltativa), il campo è un RVA di esportazione, ovvero un indirizzo effettivo nel codice o nei dati. In caso contrario, il campo è un RVA del server d'inoltro, che nomina un simbolo in un'altra DLL.



| Offset        | Dimensione          | Campo                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Esportare RVA <br/>    | Indirizzo del simbolo esportato quando viene caricato in memoria, relativo alla base dell'immagine. Ad esempio, l'indirizzo di una funzione esportata. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | RVA del server d'inoltro <br/> | Puntatore a una stringa ASCII con terminazione Null nella sezione di esportazione. Questa stringa deve essere all'interno dell'intervallo specificato dalla voce della directory dei dati della tabella di esportazione. Vedere [Directory dei dati di intestazione facoltativi (solo immagine).](#optional-header-data-directories-image-only) Questa stringa fornisce il nome della DLL e il nome dell'esportazione (ad esempio, "MYDLL.expfunc") o il nome della DLL e il numero ordinale dell'esportazione (ad esempio, "MYDLL. \# 27"). <br/> |



 

Un'RVA del server d'inoltro esporta una definizione da un'altra immagine, rendendola come se fosse esportata dall'immagine corrente. Di conseguenza, il simbolo viene importato ed esportato contemporaneamente.

Ad esempio, in Kernel32.dll in Windows XP, l'esportazione denominata "HeapAlloc" viene inoltrata alla stringa "NTDLL. RtlAllocateHeap." In questo modo le applicazioni possono usare Windows modulo specifico di XP Ntdll.dll senza effettivamente contenere riferimenti di importazione. La tabella di importazione dell'applicazione fa riferimento solo Kernel32.dll. Pertanto, l'applicazione non è specifica per Windows XP e può essere eseguita in qualsiasi sistema Win32.

#### <a name="export-name-pointer-table"></a>Esporta tabella puntatore nome

La tabella dei puntatori dei nomi di esportazione è una matrice di indirizzi (RVA) nella tabella dei nomi di esportazione. I puntatori sono a 32 bit ciascuno e sono relativi alla base dell'immagine. I puntatori vengono ordinati lessico per consentire ricerche binarie.

Un nome di esportazione viene definito solo se la tabella dei puntatori del nome di esportazione contiene un puntatore a esso.

#### <a name="export-ordinal-table"></a>Esporta tabella ordinale

La tabella ordinale di esportazione è una matrice di indici non imparziali a 16 bit nella tabella degli indirizzi di esportazione. Gli ordinali sono distorti dal campo Ordinal Base (Base ordinale) della tabella della directory di esportazione. In altre parole, la base ordinale deve essere sottratta dagli ordinali per ottenere indici true nella tabella degli indirizzi di esportazione.

La tabella dei puntatori del nome di esportazione e la tabella ordinale di esportazione formano due matrici parallele separate per consentire l'allineamento del campo naturale. Queste due tabelle, in effetti, funzionano come una tabella, in cui la colonna Puntatore nome esportazione punta a un nome pubblico (esportato) e la colonna Ordinale di esportazione fornisce il numero ordinale corrispondente per il nome pubblico. Un membro della tabella dei puntatori dei nomi di esportazione e un membro della tabella ordinale di esportazione sono associati dalla stessa posizione (indice) nelle rispettive matrici.

Pertanto, quando viene cercata la tabella dei puntatori del nome di esportazione e viene trovata una stringa corrispondente nella posizione i, l'algoritmo per trovare l'RVA del simbolo e l'ordinale distorto è:

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Quando si cerca un simbolo in base all'ordinale (distorto), l'algoritmo per trovare l'RVA e il nome del simbolo è:

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Tabella dei nomi di esportazione

La tabella dei nomi di esportazione contiene i dati stringa effettivi a cui punta la tabella dei puntatori dei nomi di esportazione. Le stringhe in questa tabella sono nomi pubblici che altre immagini possono usare per importare i simboli. Questi nomi di esportazione pubblici non corrispondono necessariamente ai nomi dei simboli privati presenti nel proprio file di immagine e nel codice sorgente, anche se possono esserne.

Ogni simbolo esportato ha un valore ordinale, che è solo l'indice nella tabella degli indirizzi di esportazione. L'uso dei nomi di esportazione, tuttavia, è facoltativo. Alcuni, tutti o nessuno dei simboli esportati possono avere nomi di esportazione. Per i simboli esportati che hanno nomi di esportazione, le voci corrispondenti nella tabella dei puntatori dei nomi di esportazione e nella tabella ordinale di esportazione funzionano insieme per associare ogni nome a un numero ordinale.

La struttura della tabella dei nomi di esportazione è una serie di stringhe ASCII con terminazione Null di lunghezza variabile.

### <a name="the-idata-section"></a>Sezione .idata

Tutti i file di immagine che importano simboli, inclusi praticamente tutti i file eseguibili (EXE), hanno una sezione .idata. Di seguito è riportato un layout di file tipico per le informazioni di importazione:

-   Tabella directory

    Voce di directory Null

-   DLL1 - Importa tabella di ricerca

    Null

-   DLL2 - Importa tabella di ricerca

    Null

-   DLL3 - Importa tabella di ricerca

    Null

-   Hint-Name tabella

#### <a name="import-directory-table"></a>Importa tabella directory

Le informazioni di importazione iniziano con la tabella della directory di importazione, che descrive il resto delle informazioni di importazione. La tabella della directory di importazione contiene informazioni sull'indirizzo utilizzate per risolvere i riferimenti di correzione ai punti di ingresso all'interno di un'immagine DLL. La tabella della directory di importazione è costituita da una matrice di voci di directory di importazione, una voce per ogni DLL a cui fa riferimento l'immagine. L'ultima voce di directory è vuota (con valori Null), che indica la fine della tabella di directory.

Ogni voce della directory di importazione ha il formato seguente:



| Offset         | Dimensione          | Campo                                                 | Descrizione                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Importare l'RVA della tabella di ricerca (caratteristiche) <br/> | Valore RVA della tabella di ricerca di importazione. Questa tabella contiene un nome o un numero ordinale per ogni importazione. Il nome "Characteristics" viene usato in Winnt.h, ma non descrive più questo campo. <br/> |
| 4 <br/>  | 4 <br/> | Timestamp/Data <br/>                           | Indicatore impostato su zero finché l'immagine non viene associata. Dopo l'associazione dell'immagine, questo campo viene impostato sull'indicatore di data e ora della DLL. <br/>                                          |
| 8 <br/>  | 4 <br/> | Catena di server d'inoltro <br/>                           | Indice del primo riferimento al server d'inoltro. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Assegnare un nome all'RVA <br/>                                  | Indirizzo di una stringa ASCII che contiene il nome della DLL. Questo indirizzo è relativo alla base dell'immagine. <br/>                                                                   |
| 16 <br/> | 4 <br/> | Importare l'RVA della tabella di indirizzi (tabella Thunk) <br/>    | RVA della tabella di indirizzi di importazione. Il contenuto di questa tabella è identico a quello della tabella di ricerca di importazione finché l'immagine non viene associata. <br/>                              |



 

#### <a name="import-lookup-table"></a>Importa tabella di ricerca

Una tabella di ricerca di importazione è una matrice di numeri a 32 bit per PE32 o una matrice di numeri a 64 bit per PE32+. Ogni voce usa il formato del campo di bit descritto nella tabella seguente. In questo formato, il bit 31 è il bit più significativo per PE32 e il bit 63 è il bit più significativo per PE32+. La raccolta di queste voci descrive tutte le importazioni da una DETERMINATA DLL. L'ultima voce è impostata su zero (NULL) per indicare la fine della tabella.



| Bit(s)            | Dimensione           | Campo di bit                       | Descrizione                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Flag ordinale/nome <br/>   | Se questo bit è impostato, importare in base al numero ordinale. In caso contrario, importare in base al nome. Il bit viene mascherato 0x80000000 per PE32, 0x8000000000000000 per PE32+. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Numero ordinale <br/>      | Numero ordinale a 16 bit. Questo campo viene usato solo se il campo di bit Ordinal/Name Flag è 1 (import by ordinal). I bit 30-15 o 62-15 devono essere 0. <br/>                  |
| 30-0 <br/>  | 31 <br/> | RVA tabella hint/nome <br/> | RVA a 31 bit di una voce di tabella hint/nome. Questo campo viene usato solo se il campo di bit Ordinal/Name Flag è 0 (importazione in base al nome). Per i bit PE32+ 62-31 deve essere zero. <br/> |



 

#### <a name="hintname-table"></a>Tabella hint/nome

Una tabella hint/nome è sufficiente per l'intera sezione di importazione. Ogni voce nella tabella hint/name ha il formato seguente:



| Offset         | Dimensione                 | Campo            | Descrizione                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Hint <br/> | Indice nella tabella del puntatore del nome di esportazione. Viene tentata prima una corrispondenza con questo valore. Se non riesce, viene eseguita una ricerca binaria nella tabella dei puntatori dei nomi di esportazione della DLL. <br/>            |
| 2 <br/>  | Variabile <br/> | Nome <br/> | Stringa ASCII contenente il nome da importare. Si tratta della stringa che deve essere abbinata al nome pubblico nella DLL. Questa stringa fa distinzione tra maiuscole e minuscole e termina con un byte Null. <br/> |
| \* <br/> | 0 o 1 <br/>   | Pad <br/>  | Byte finale con riempimento zero che viene visualizzato dopo il byte null finale, se necessario, per allineare la voce successiva su un limite pari. <br/>                                                        |



 

#### <a name="import-address-table"></a>Importa tabella indirizzi

La struttura e il contenuto della tabella degli indirizzi di importazione sono identici a quelli della tabella di ricerca di importazione, fino a quando il file non viene associato. Durante l'associazione, le voci nella tabella degli indirizzi di importazione vengono sovrascritte con gli indirizzi a 32 bit (per PE32) o a 64 bit (per PE32+) dei simboli importati. Questi indirizzi sono gli indirizzi di memoria effettivi dei simboli, anche se tecnicamente sono ancora chiamati "indirizzi virtuali". Il caricatore elabora in genere l'associazione.

### <a name="the-pdata-section"></a>Sezione .pdata

La sezione .pdata contiene una matrice di voci della tabella delle funzioni usate per la gestione delle eccezioni. A essa fa riferimento la voce della tabella delle eccezioni nella directory dei dati dell'immagine. Le voci devono essere ordinate in base agli indirizzi della funzione (il primo campo in ogni struttura) prima di essere generate nell'immagine finale. La piattaforma di destinazione determina quale delle tre variazioni del formato di immissione della tabella delle funzioni descritte di seguito viene usata.

Per le immagini MIPS a 32 bit, le voci della tabella delle funzioni hanno il formato seguente:



| Offset         | Dimensione          | Campo                          | Descrizione                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Indirizzo iniziale <br/>      | Valore va della funzione corrispondente. <br/>                              |
| 4 <br/>  | 4 <br/> | Indirizzo finale <br/>        | Valore va della fine della funzione. <br/>                                 |
| 8 <br/>  | 4 <br/> | Gestore eccezioni <br/>  | Puntatore al gestore eccezioni da eseguire. <br/>               |
| 12 <br/> | 4 <br/> | Dati del gestore <br/>       | Puntatore a informazioni aggiuntive da passare al gestore. <br/> |
| 16 <br/> | 4 <br/> | Prolog Indirizzo finale <br/> | Valore va della fine del prologo della funzione. <br/>                        |



 

Per le piattaforme arm, PowerPC, SH3 e SH4 Windows CE, le voci della tabella delle funzioni hanno il formato seguente:



| Offset        | Dimensione                | Campo                       | Descrizione                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | Indirizzo iniziale <br/>   | Valore va della funzione corrispondente. <br/>                                                                         |
| 4 <br/> | 8 bit <br/>  | Prolog Lunghezza <br/>   | Numero di istruzioni nel prologo della funzione. <br/>                                                          |
| 4 <br/> | 22 bit <br/> | Lunghezza funzione <br/> | Numero di istruzioni nella funzione. <br/>                                                                   |
| 4 <br/> | 1 bit <br/>   | Flag a 32 bit <br/>     | Se impostata, la funzione è costituita da istruzioni a 32 bit. Se è deselezionata, la funzione è costituita da istruzioni a 16 bit. <br/> |
| 4 <br/> | 1 bit <br/>   | Flag di eccezione <br/>  | Se impostato, esiste un gestore eccezioni per la funzione. In caso contrario, non esiste alcun gestore di eccezioni. <br/>                 |



 

Per le piattaforme x64 e Itanium, le voci della tabella delle funzioni hanno il formato seguente:



| Offset        | Dimensione          | Campo                          | Descrizione                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | Indirizzo iniziale <br/>      | Valore RVA della funzione corrispondente. <br/> |
| 4 <br/> | 4 <br/> | Indirizzo finale <br/>        | Valore RVA della fine della funzione. <br/>    |
| 8 <br/> | 4 <br/> | Informazioni di rimozione <br/> | RVA delle informazioni di rimozione. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>Sezione .reloc (solo immagine)

La tabella di rilocazione di base contiene le voci per tutte le rilocazioni di base nell'immagine. Il campo Tabella di rilocazione di base nelle directory dei dati di intestazione facoltative indica il numero di byte nella tabella di rilocazione di base. Per altre informazioni, vedere [Directory dei dati di intestazione facoltative (solo immagine).](#optional-header-data-directories-image-only) La tabella di rilocazione di base è suddivisa in blocchi. Ogni blocco rappresenta le rilocazioni di base per una pagina 4K. Ogni blocco deve iniziare su un limite a 32 bit.

Il caricatore non è necessario per elaborare le rilocazioni di base risolte dal linker, a meno che l'immagine di caricamento non possa essere caricata nella base di immagini specificata nell'intestazione PE.

#### <a name="base-relocation-block"></a>Blocco di rilocazione di base

Ogni blocco di rilocazione di base inizia con la struttura seguente:



| Offset        | Dimensione          | Campo                  | Descrizione                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Pagina RVA <br/>   | La base dell'immagine e l'RVA della pagina vengono aggiunti a ogni offset per creare l'istanza di Va in cui deve essere applicata la rilocazione di base. <br/>                         |
| 4 <br/> | 4 <br/> | Dimensione blocco <br/> | Numero totale di byte nel blocco di rilocazione di base, inclusi i campi Page RVA e Block Size e i campi Type/Offset seguenti. <br/> |



 

Il campo Dimensioni blocco è quindi seguito da un numero qualsiasi di voci di campo Tipo o Offset. Ogni voce è word (2 byte) e ha la struttura seguente:



| Offset        | Dimensione                | Campo              | Descrizione                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 bit <br/>  | Tipo <br/>   | Archiviato nei 4 bit elevati di WORD, valore che indica il tipo di rilocazione di base da applicare. Per altre informazioni, vedere [Tipi di rilocazione di base](#base-relocation-types).<br/>                         |
| 0 <br/> | 12 bit <br/> | Offset <br/> | Archiviato nei restanti 12 bit di WORD, offset dall'indirizzo iniziale specificato nel campo RVA pagina per il blocco. Questo offset specifica dove deve essere applicata la rilocazione di base. <br/> |



 

Per applicare una rilocazione di base, la differenza viene calcolata tra l'indirizzo di base preferito e la base in cui l'immagine viene effettivamente caricata. Se l'immagine viene caricata nella base preferita, la differenza è zero e pertanto non è necessario applicare le rilocazioni di base.

#### <a name="base-relocation-types"></a>Tipi di rilocazione di base



| Costante                                       | Valore          | Descrizione                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ BASED \_ ABSOLUTE <br/>        | 0 <br/>  | La rilocazione di base viene ignorata. Questo tipo può essere usato per bloccare un blocco. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ BASED \_ HIGH <br/>            | 1 <br/>  | La rilocazione di base aggiunge i 16 bit elevati della differenza al campo a 16 bit in corrispondenza dell'offset. Il campo a 16 bit rappresenta il valore massimo di una parola a 32 bit. <br/>                                                                                                                                                               |
| IMAGE \_ REL \_ BASED \_ LOW <br/>             | 2 <br/>  | La rilocazione di base aggiunge i 16 bit bassi della differenza al campo a 16 bit in corrispondenza dell'offset. Il campo a 16 bit rappresenta la metà bassa di una parola a 32 bit. <br/>                                                                                                                                                                  |
| HIGHLOW BASATO SU IMAGE \_ REL \_ \_ <br/>         | 3 <br/>  | La rilocazione di base applica tutti i 32 bit della differenza al campo a 32 bit in corrispondenza dell'offset. <br/>                                                                                                                                                                                                                              |
| \_ \_ HIGHADJ BASATO SU IMAGE REL \_ <br/>         | 4 <br/>  | La rilocazione di base aggiunge i 16 bit elevati della differenza al campo a 16 bit in corrispondenza dell'offset. Il campo a 16 bit rappresenta il valore massimo di una parola a 32 bit. I 16 bit bassi del valore a 32 bit vengono archiviati nella parola a 16 bit che segue questa rilocazione di base. Questo significa che la rilocazione di base occupa due slot. <br/> |
| \_ \_ \_ JMPADDR BASATO SU IMAGE REL \_ <br/>   | 5 <br/>  | L'interpretazione della rilocazione dipende dal tipo di computer. <br/> Quando il tipo di computer è MIPS, la rilocazione di base si applica a un'istruzione di salto MIPS. <br/>                                                                                                                                                    |
| IMAGE \_ REL \_ BASED \_ ARM \_ MOV32 <br/>      | 5 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è ARM o Thumb. La rilocazione di base applica l'indirizzo a 32 bit di un simbolo in una coppia di istruzioni MOVW/MOVT consecutiva. <br/>                                                                                                                                 |
| \_ \_ RISCV \_ \_ HIGH20 BASATO SU IMAGE REL <br/>   | 5 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è RISC-V. La rilocazione di base si applica ai 20 bit elevati di un indirizzo assoluto a 32 bit. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Riservato, deve essere zero. <br/>                                                                                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ BASED \_ THUMB \_ MOV32 <br/>    | 7 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è Thumb. La rilocazione di base applica l'indirizzo a 32 bit di un simbolo a una coppia di istruzioni MOVW/MOVT consecutiva. <br/>                                                                                                                                            |
| \_ \_ RISCV \_ \_ LOW12I BASATO SU IMAGE REL <br/>   | 7 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è RISC-V. La rilocazione di base si applica ai 12 bit bassi di un indirizzo assoluto a 32 bit formato nel formato di istruzione RISC-V di tipo I. <br/>                                                                                                                           |
| \_ \_ RISCV \_ \_ LOW12S BASATO SU IMAGE REL <br/>   | 8 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è RISC-V. La rilocazione di base si applica ai 12 bit bassi di un indirizzo assoluto a 32 bit formato nel formato di istruzione RISC-V S. <br/>                                                                                                                           |
| IMAGE \_ REL \_ BASED \_ MIPS \_ JMPADDR16 <br/> | 9 <br/>  | La rilocazione è significativa solo quando il tipo di computer è MIPS. La rilocazione di base si applica a un'istruzione di salto MIPS16. <br/>                                                                                                                                                                                            |
| DIR64 BASATO SU IMAGE \_ \_ \_ REL <br/>           | 10 <br/> | La rilocazione di base applica la differenza al campo a 64 bit in corrispondenza dell'offset. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>Sezione .tls

La sezione .tls fornisce supporto PE diretto e COFF per l'archiviazione locale di thread statici (TLS). TLS è una classe di archiviazione speciale che Windows supporta in cui un oggetto dati non è una variabile automatica (stack), ma è locale per ogni singolo thread che esegue il codice. Pertanto, ogni thread può mantenere un valore diverso per una variabile dichiarata tramite TLS.

Si noti che qualsiasi quantità di dati TLS può essere supportata tramite l'API chiama TlsAlloc, TlsFree, TlsSetValue e TlsGetValue. L'implementazione pe o COFF è un approccio alternativo all'uso dell'API e ha il vantaggio di essere più semplice dal punto di vista del programmatore di linguaggio di alto livello. Questa implementazione consente di definire e inizializzare i dati TLS in modo analogo alle normali variabili statiche in un programma. Ad esempio, in Visual C++, una variabile TLS statica può essere definita come segue, senza usare l'API Windows:

`__declspec (thread) int tlsFlag = 1;`

Per supportare questo costrutto di programmazione, la sezione PE e COFF .tls specifica le informazioni seguenti: dati di inizializzazione, routine di callback per l'inizializzazione e la terminazione per thread e l'indice TLS, illustrati nella discussione seguente.

> [!Note]
>
> Gli oggetti dati TLS dichiarati in modo statico possono essere usati solo nei file di immagine caricati in modo statico. Questo fatto rende inaffidabile l'uso di dati TLS statici in una DLL, a meno che non si sappia che la DLL o qualsiasi elemento collegato in modo statico non verrà mai caricato dinamicamente con la funzione API LoadLibrary.

 

Il codice eseguibile accede a un oggetto dati TLS statico tramite la procedura seguente:

1.  In fase di collegamento, il linker imposta il campo Indirizzo dell'indice della directory TLS. Questo campo punta a una posizione in cui il programma prevede di ricevere l'indice TLS.

    La libreria di runtime Microsoft facilita questo processo definendo un'immagine di memoria della directory TLS e fornendogli il nome speciale \_ \_ "tls \_ used" (piattaforme Intel x86) o \_ "tls \_ used" (altre piattaforme). Il linker cerca questa immagine di memoria e usa i dati per creare la directory TLS. Altri compilatori che supportano TLS e usano il linker Microsoft devono usare questa stessa tecnica.

2.  Quando viene creato un thread, il caricatore comunica l'indirizzo della matrice TLS del thread inserendo l'indirizzo del blocco di ambiente del thread (TEB) nel registro FS. Un puntatore alla matrice TLS si trova all'offset 0x2C dall'inizio di TEB. Questo comportamento è specifico di Intel x86.

3.  Il caricatore assegna il valore dell'indice TLS alla posizione indicata dal campo Indirizzo dell'indice.

4.  Il codice eseguibile recupera l'indice TLS e anche il percorso della matrice TLS.

5.  Il codice usa l'indice TLS e la posizione della matrice TLS (moltiplicando l'indice per 4 e usandolo come offset per la matrice) per ottenere l'indirizzo dell'area dati TLS per il programma e il modulo specificati. Ogni thread ha una propria area dati TLS, ma è trasparente per il programma, che non deve sapere come vengono allocati i dati per i singoli thread.

6.  Un singolo oggetto dati TLS è accessibile come offset fisso nell'area dati TLS.

La matrice TLS è una matrice di indirizzi che il sistema gestisce per ogni thread. Ogni indirizzo in questa matrice fornisce la posizione dei dati TLS per un determinato modulo (EXE o DLL) all'interno del programma. L'indice TLS indica quale membro della matrice usare. L'indice è un numero (significativo solo per il sistema) che identifica il modulo.

#### <a name="the-tls-directory"></a>The TLS Directory

Il formato della directory TLS è il seguente:



| Offset (PE32/PE32+) | Dimensioni (PE32/PE32+) | Campo                            | Descrizione                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | Avvio dati non elaborati va <br/>    | Indirizzo iniziale del modello TLS. Il modello è un blocco di dati usato per inizializzare i dati TLS. Il sistema copia tutti questi dati ogni volta che viene creato un thread, quindi non deve essere danneggiato. Si noti che questo indirizzo non è un RVA. è un indirizzo per il quale deve essere presente una rilocazione di base nella sezione .reloc. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | Dati non elaborati - Fine va <br/>      | Indirizzo dell'ultimo byte di TLS, ad eccezione del riempimento zero. Come per il campo Raw Data Start VA, si tratta di un va, non di un RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Indirizzo dell'indice <br/>     | Posizione in cui ricevere l'indice TLS assegnato dal caricatore. Questa posizione si trova in una sezione di dati ordinaria, quindi è possibile assegnare un nome simbolico accessibile al programma. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Indirizzo dei callback <br/> | Puntatore a una matrice di funzioni di callback TLS. La matrice ha terminazione Null, quindi se non è supportata alcuna funzione di callback, questo campo punta a 4 byte impostati su zero. Per informazioni sul prototipo per queste funzioni, vedere [Funzioni di callback TLS](#tls-callback-functions).<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Dimensioni del riempimento zero <br/>    | Dimensione in byte del modello, oltre ai dati inizializzati delimitati dai campi Raw Data Start VA e Raw Data End VA. Le dimensioni totali del modello devono essere le stesse delle dimensioni totali dei dati TLS nel file di immagine. Il riempimento zero è la quantità di dati che viene dopo i dati inizializzati diversi da zero. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Caratteristiche <br/>      | I quattro bit \[ 23:20 \] descrivono le informazioni di allineamento. I valori possibili sono quelli definiti come IMAGE SCN ALIGN, che vengono usati anche per descrivere \_ l'allineamento della sezione nei file \_ \_ \* oggetto. Gli altri 28 bit sono riservati per un uso futuro. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>Funzioni di callback TLS

Il programma può fornire una o più funzioni di callback TLS per supportare l'inizializzazione e la terminazione aggiuntive per gli oggetti dati TLS. Un uso tipico per una funzione di callback di questo tipo è chiamare costruttori e distruttori per gli oggetti.

Anche se in genere non sono presenti più funzioni di callback, un callback viene implementato come matrice per rendere possibile l'aggiunta di funzioni di callback aggiuntive, se lo si desidera. Se è presente più di una funzione di callback, ogni funzione viene chiamata nell'ordine in cui il relativo indirizzo viene visualizzato nella matrice. Un puntatore Null termina la matrice. È perfettamente valido avere un elenco vuoto (nessun callback supportato), nel qual caso la matrice di callback ha esattamente un membro- un puntatore Null.

Il prototipo per una funzione di callback (a cui punta un puntatore di tipo PIMAGE TLS CALLBACK) ha gli stessi parametri di una funzione del punto di ingresso \_ \_ DLL:


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



Il parametro Reserved deve essere impostato su zero. Il parametro Reason può assumere i valori seguenti:



| Impostazione                          | Valore         | Descrizione                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| DLL \_ PROCESS \_ ATTACH <br/> | 1 <br/> | È stato avviato un nuovo processo, incluso il primo thread. <br/>                                   |
| COLLEGAMENTO \_ DI THREAD \_ DLL <br/>  | 2 <br/> | È stato creato un nuovo thread. Notifica inviata per tutti i thread, ad esempio il primo. <br/>      |
| DISCONNESSIONE \_ THREAD \_ DLL <br/>  | 3 <br/> | Un thread sta per essere terminato. Notifica inviata per tutti i thread, ad esempio il primo. <br/> |
| DLL \_ PROCESS \_ DETACH <br/> | 0 <br/> | Un processo sta per terminare, incluso il thread originale. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>Struttura di configurazione del caricamento (solo immagine)

La struttura di configurazione del caricamento (IMAGE LOAD CONFIG DIRECTORY) è stata usata in precedenza in casi molto limitati nel sistema operativo Windows NT stesso per descrivere varie funzionalità troppo difficili o troppo grandi per essere descritte nell'intestazione del file o nell'intestazione facoltativa \_ dell'immagine. \_ \_ Le versioni correnti del linker Microsoft e di Windows XP e versioni successive di Windows usano una nuova versione di questa struttura per sistemi basati su x86 a 32 bit che includono la tecnologia SEH riservata. In questo modo viene fornito un elenco di gestori di eccezioni strutturate sicuri utilizzati dal sistema operativo durante l'invio delle eccezioni. Se l'indirizzo del gestore risiede nell'intervallo va di un'immagine ed è contrassegnato come riservato in grado di riconoscere SEH (ovvero IMAGE DLLCHARACTERISTICS NO SEH è chiaro nel campo \_ \_ DllCharacteristics dell'intestazione facoltativa, come descritto in precedenza), il gestore deve essere in elenco di gestori sicuri noti per tale \_ immagine. In caso contrario, il sistema operativo termina l'applicazione. Ciò consente di evitare l'exploit di hijack del gestore di eccezioni x86 usato in passato per assumere il controllo del sistema operativo.

Microsoft Linker fornisce automaticamente una struttura di configurazione del carico predefinita per includere i dati SEH riservati. Se il codice utente fornisce già una struttura di configurazione del carico, deve includere i nuovi campi SEH riservati. In caso contrario, il linker non può includere i dati SEH riservati e l'immagine non è contrassegnata come contenente SEH riservato.

#### <a name="load-configuration-directory"></a>Caricare la directory di configurazione

La voce della directory dei dati per una struttura di configurazione del carico SEH pre-riservata deve specificare una dimensione specifica della struttura di configurazione del carico perché il caricatore del sistema operativo si aspetta sempre che sia un determinato valore. A tale proposito, la dimensione è in realtà solo un controllo della versione. Per compatibilità con Windows XP e versioni precedenti di Windows, le dimensioni devono essere 64 per le immagini x86.

#### <a name="load-configuration-layout"></a>Caricare il layout di configurazione

La struttura di configurazione del carico ha il layout seguente per i file PE a 32 bit e a 64 bit:



| Offset              | Dimensione            | Campo                                      | Descrizione                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Caratteristiche <br/>                | Flag che indicano gli attributi del file, attualmente inutilizzati. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Valore del timestamp di data e ora. Il valore è rappresentato nel numero di secondi trascorsi dalla mezzanotte (00:00:00), il 1° gennaio 1970, ora UTC (Universal Coordinated Time), in base all'orologio di sistema. Il timestamp può essere stampato usando la funzione time del runtime C (CRT). <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Numero di versione principale. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Numero di versione secondario. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | GlobalFlagsClear <br/>               | Flag del caricatore globale da cancellare per questo processo quando il caricatore avvia il processo. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | GlobalFlagsSet <br/>                 | Flag del caricatore globale da impostare per questo processo quando il caricatore avvia il processo. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | CriticalSectionDefaultTimeout <br/>  | Valore di timeout predefinito da usare per le sezioni critiche del processo abbandonate. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | DeCommitFreeBlockThreshold <br/>     | Memoria che deve essere liberata prima che venga restituita al sistema, in byte. <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | DeCommitTotalFreeThreshold <br/>     | Quantità totale di memoria disponibile, in byte. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | LockPrefixTable <br/>                | \[Solo x86 Va di un elenco di indirizzi in cui viene usato il prefisso LOCK in modo che possano essere sostituiti con \] NOP nei computer a processore singolo. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | MaximumAllocationSize <br/>          | Dimensione massima di allocazione, in byte. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | VirtualMemoryThreshold <br/>         | Dimensioni massime della memoria virtuale, in byte. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | ProcessAffinityMask <br/>            | L'impostazione di questo campo su un valore diverso da zero equivale a chiamare SetProcessAffinityMask con questo valore durante l'avvio del processo (solo .exe) <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | ProcessHeapFlags <br/>               | Flag dell'heap dei processi che corrispondono al primo argomento della funzione HeapCreate. Questi flag si applicano all'heap dei processi creato durante l'avvio del processo. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | Identificatore di versione del Service Pack. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Riservato <br/>                       | Deve essere zero. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | EditList <br/>                       | Riservato per l'uso da parte del sistema. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | SecurityCookie <br/>                 | Puntatore a un cookie usato dall'implementazione Visual C++ o GS. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | SEHandlerTable <br/>                 | \[Solo x86 L'va della tabella ordinata di RVA di ogni gestore di edizione Standard \] valido nell'immagine. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | SEHandlerCount <br/>                 | \[solo x86 \] Numero di gestori univoci nella tabella. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | GuardCFCheckFunctionPointer <br/>    | Va in cui è archiviato il Flow della funzione di controllo di Control Flow Guard. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | GuardCFDispatchFunctionPointer <br/> | Va where Control Flow Guard dispatch-function pointer is stored. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | GuardCFFunctionTable <br/>           | Va della tabella ordinata di RVA di ogni controllo Flow Guard nell'immagine. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | GuardCFFunctionCount <br/>           | Numero di RVA univoci nella tabella precedente. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | GuardFlags <br/>                     | Controllare Flow flag correlati a Guard. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | CodeIntegrity <br/>                  | Informazioni sull'integrità del codice. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryTable <br/> | L'va in cui è Flow'indirizzo di Guard preso la tabella IAT. <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryCount <br/> | Numero di RVA univoci nella tabella precedente. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | GuardLongJumpTargetTable <br/>       | Va in cui è archiviata la Flow destinazione di salto lungo di Control Flow Guard. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | GuardLongJumpTargetCount <br/>       | Numero di RVA univoci nella tabella precedente. <br/>                                                                                                                                                                                                                                    |



 

Il campo GuardFlags contiene una combinazione di uno o più flag e sottocampi seguenti:

-   Il modulo esegue i controlli di integrità del flusso di controllo usando il supporto fornito dal sistema.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   Il modulo esegue controlli di integrità del flusso di controllo e scrittura.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   Il modulo contiene metadati di destinazione del flusso di controllo validi.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   Il modulo non usa il cookie di sicurezza /GS.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   Il modulo supporta l'IAT con caricamento ritardato di sola lettura.

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   Delayload della tabella di importazione nella relativa sezione .didat (senza altri elementi) che può essere riprotetto liberamente.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   Il modulo contiene informazioni sull'esportazione soppresse. Ciò deduce anche che l'indirizzo della tabella IAT è presente anche nella configurazione di caricamento.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   Il modulo consente l'eliminazione delle esportazioni.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   Il modulo contiene informazioni sulla destinazione longjmp.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   Maschera per il sottocampo che contiene lo stride delle voci della tabella della funzione Control Flow Guard , ovvero il conteggio aggiuntivo di byte per ogni voce della tabella.

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

Inoltre, l'intestazione winnt.h dell'SDK Windows definisce questa macro per la quantità di bit per spostare a destra il valore GuardFlags per giustificare a destra lo stride della tabella della funzione Control Flow Guard:

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>Sezione .rsrc

Le risorse vengono indicizzate in base a una struttura ad albero a più livelli con ordinamento binario. La progettazione generale può incorporare 2 \* \* 31 livelli. Per convenzione, tuttavia, Windows usa tre livelli:

<dl> Type  
Nome  
Linguaggio  
</dl>

Una serie di tabelle di directory delle risorse mette in relazione tutti i livelli nel modo seguente: ogni tabella di directory è seguita da una serie di voci di directory che forniscono il nome o l'identificatore (ID) per tale livello (tipo, nome o linguaggio) e un indirizzo di una descrizione dei dati o di un'altra tabella di directory. Se l'indirizzo punta a una descrizione dei dati, i dati sono una foglia nell'albero. Se l'indirizzo punta a un'altra tabella di directory, la tabella elenca le voci di directory al livello successivo verso il basso.

Gli ID tipo, nome e lingua di una foglia sono determinati dal percorso seguito dalle tabelle di directory per raggiungere la foglia. La prima tabella determina l'ID tipo, la seconda tabella (a cui punta la voce di directory nella prima tabella) determina l'ID nome e la terza tabella determina l'ID lingua.

La struttura generale della sezione .rsrc è:



| Dati                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabelle della directory delle risorse (e voci della directory delle risorse) <br/> | Una serie di tabelle, una per ogni gruppo di nodi nell'albero. Tutti i nodi di primo livello (Tipo) sono elencati nella prima tabella. Le voci di questa tabella puntano a tabelle di secondo livello. Ogni albero di secondo livello ha lo stesso ID tipo ma ID nome diversi. Gli alberi di terzo livello hanno gli stessi ID tipo e nome, ma ID di linguaggio diversi. <br/> Ogni singola tabella è immediatamente seguita da voci di directory, in cui ogni voce ha un nome o un identificatore numerico e un puntatore a una descrizione dei dati o a una tabella al livello inferiore successivo. <br/> |
| Stringhe di directory delle risorse <br/>                                 | Stringhe Unicode allineate a due byte, che fungono da dati stringa a cui puntano le voci di directory. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Descrizione dei dati delle risorse <br/>                                  | Matrice di record, a cui puntano le tabelle, che descrivono le dimensioni effettive e la posizione dei dati delle risorse. Questi record sono le foglia dell'albero resource-description. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Dati della risorsa <br/>                                              | Dati non elaborati della sezione della risorsa. Le informazioni sulle dimensioni e sulla posizione nel campo Descrizioni dei dati delle risorse delimitano le singole aree dei dati delle risorse. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Tabella della directory delle risorse

Ogni tabella di directory delle risorse ha il formato seguente. Questa struttura di dati deve essere considerata l'intestazione di una tabella perché la tabella è effettivamente costituita da voci di directory (descritte nella sezione 6.9.2, "Voci della directory delle risorse") e da questa struttura:



| Offset         | Dimensione          | Campo                              | Descrizione                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Caratteristiche <br/>        | Flag di risorsa. Questo campo è riservato per un utilizzo futuro. Attualmente è impostata su zero. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Timestamp data/ora <br/>        | Ora in cui i dati delle risorse sono stati creati dal compilatore di risorse. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Versione principale <br/>          | Numero di versione principale, impostato dall'utente. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Versione secondaria <br/>          | Numero di versione secondaria, impostato dall'utente. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Numero di voci di nome <br/> | Numero di voci di directory immediatamente dopo la tabella che usano stringhe per identificare le voci Type, Name o Language (a seconda del livello della tabella). <br/> |
| 14 <br/> | 2 <br/> | Numero di voci ID <br/>   | Numero di voci di directory immediatamente dopo le voci Name che usano ID numerici per le voci Type, Name o Language. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Voci della directory delle risorse

Le voci di directory costituiscono le righe di una tabella. Ogni voce della directory di risorse ha il formato seguente. Se la voce è una voce Name o ID è indicata dalla tabella della directory delle risorse, che indica il numero di voci Name e ID che la seguono (tenere presente che tutte le voci Name precedono tutte le voci ID per la tabella). Tutte le voci della tabella sono ordinate in ordine crescente: le voci Name in base alla stringa con distinzione tra maiuscole e minuscole e le voci ID in base al valore numerico. Gli offset sono relativi all'indirizzo in IMAGE \_ DIRECTORY \_ ENTRY RESOURCE \_ DataDirectory. Per [altre informazioni, vedere Peering inside the PE: A Tour of the Win32 Portable Executable File Format (Peering all'interno](/previous-versions/ms809762(v=msdn.10)#pe-file-resources) di PE: presentazione del formato di file eseguibile portabile Win32).



| Offset        | Dimensione          | Campo                           | Descrizione                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Offset dei nomi <br/>         | Offset di una stringa che fornisce la voce Type, Name o Language ID, a seconda del livello di tabella. <br/>     |
| 0 <br/> | 4 <br/> | ID di tipo integer <br/>          | Intero a 32 bit che identifica la voce Type, Name o Language ID. <br/>                                   |
| 4 <br/> | 4 <br/> | Offset immissione dati <br/>   | Bit alto 0. Indirizzo di una voce di dati delle risorse (foglia). <br/>                                                   |
| 4 <br/> | 4 <br/> | Offset sottodirectory <br/> | Bit alto 1. I 31 bit inferiori sono l'indirizzo di un'altra tabella di directory delle risorse (livello successivo verso il basso). <br/> |



 

#### <a name="resource-directory-string"></a>Stringa della directory delle risorse

L'area della stringa della directory delle risorse è costituita da stringhe Unicode allineate a parole. Queste stringhe vengono archiviate insieme dopo l'ultima voce della directory delle risorse e prima della prima voce di dati delle risorse. In questo modo si riduce al minimo l'impatto di queste stringhe a lunghezza variabile sull'allineamento delle voci di directory di dimensioni fisse. Ogni stringa di directory di risorse ha il formato seguente:



| Offset        | Dimensione                 | Campo                      | Descrizione                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Length <br/>         | Dimensione della stringa, senza includere il campo di lunghezza stesso. <br/> |
| 2 <br/> | Variabile <br/> | Stringa Unicode <br/> | Dati di stringa Unicode a lunghezza variabile, allineati a parole. <br/>     |



 

#### <a name="resource-data-entry"></a>Immissione di dati delle risorse

Ogni immissione di dati risorsa descrive un'unità effettiva di dati non elaborati nell'area Dati risorsa. Una voce di Dati risorsa ha il formato seguente:



| Offset         | Dimensione          | Campo                            | Descrizione                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | RVA dei dati <br/>             | Indirizzo di un'unità di dati delle risorse nell'area Dati risorsa. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Dimensione <br/>                 | Dimensione, in byte, dei dati delle risorse a cui punta il campo RVA dati. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | Tabella codici utilizzata per decodificare i valori dei punti di codice all'interno dei dati delle risorse. In genere, la tabella codici è la tabella codici Unicode. <br/> |
| 12 <br/> | 4 <br/> | Riservato, deve essere 0. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>Sezione .cormeta (solo oggetto)

I metadati CLR vengono archiviati in questa sezione. Viene usato per indicare che il file oggetto contiene codice gestito. Il formato dei metadati non è documentato, ma può essere passato alle interfacce CLR per la gestione dei metadati.

### <a name="the-sxdata-section"></a>Sezione .sxdata

I gestori di eccezioni validi di un oggetto sono elencati nella **sezione .sxdata** di tale oggetto. La sezione è contrassegnata come IMAGE \_ SCN \_ LNK \_ INFO. Contiene l'indice dei simboli COFF di ogni gestore valido, usando 4 byte per indice.

Inoltre, il compilatore contrassegna un oggetto COFF come SEH registrato emettendo il simbolo assoluto " " con l'LSB del campo del valore @feat.00 impostato su 1. Un oggetto COFF senza gestori SEH registrati avrebbe il simbolo @feat.00 " ", ma nessuna **sezione .sxdata.**

## <a name="archive-library-file-format"></a>Formato di file di archivio (libreria)

- [Firma file di archiviazione](#archive-file-signature)
- [Archiviare le intestazioni dei membri](#archive-member-headers)
- [Primo membro del linker](#first-linker-member)
- [Secondo membro del linker](#second-linker-member)
- [Membro longnames](#longnames-member)

Il formato di archivio COFF fornisce un meccanismo standard per l'archiviazione di raccolte di file oggetto. Queste raccolte sono comunemente denominate librerie nella documentazione di programmazione.

I primi 8 byte di un archivio sono costituiti dalla firma del file. Il resto dell'archivio è costituito da una serie di membri dell'archivio, come indicato di seguito:

-   Il primo e il secondo membro sono "membri del linker". Ognuno di questi membri ha il proprio formato, come descritto nella sezione [Importare il tipo di nome](#import-name-type). In genere, un linker inserisce informazioni in questi membri di archivio. I membri del linker contengono la directory dell'archivio.

-   Il terzo membro è il membro "longnames". Questo membro facoltativo è costituito da una serie di stringhe ASCII con terminazione Null in cui ogni stringa è il nome di un altro membro di archivio.

-   Il resto dell'archivio è costituito da membri standard (file oggetto). Ognuno di questi membri contiene il contenuto di un file oggetto nella sua interezza.

Un'intestazione del membro di archivio precede ogni membro. L'elenco seguente illustra la struttura generale di un archivio:

-   Firma :"! &lt; arch &gt; \\ n"
-   Intestazione

    <dl> Primo membro del linker  
    </dl>

-   Intestazione

    <dl> Secondo membro del linker  
    </dl>

-   Intestazione

    <dl> Membro longnames  
    </dl>

-   Intestazione

    <dl> Contenuto del file OBJ 1  
    (formato COFF)  
    </dl>

-   Intestazione

    <dl> Contenuto del file OBJ 2  
    (formato COFF)  
    </dl>

### <a name="archive-file-signature"></a>Firma file di archiviazione

La firma del file di archivio identifica il tipo di file. Qualsiasi utilità, ad esempio un linker, che accetta un file di archivio come input può controllare il tipo di file leggendo questa firma. La firma è costituita dai caratteri ASCII seguenti, in cui ogni carattere seguente è rappresentato letteralmente, ad eccezione del carattere di nuova riga \\ (n):

`!<arch>\n`

### <a name="archive-member-headers"></a>Archiviare le intestazioni dei membri

Ogni membro (linker, nomi lunghi o membro del file oggetto) è preceduto da un'intestazione . Un'intestazione del membro di archivio ha il formato seguente, in cui ogni campo è una stringa di testo ASCII che viene lasciata giustificata e riempita con spazi alla fine del campo. In nessuno di questi campi non è presente alcun carattere null di terminazione.

Ogni intestazione del membro inizia sul primo indirizzo pari dopo la fine del membro di archivio precedente.



| Offset         | Dimensione           | Campo                     | Descrizione                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Nome <br/>          | Nome del membro di archivio, con una barra (/) aggiunta per terminare il nome. Se il primo carattere è una barra, il nome ha un'interpretazione speciale, come descritto nella tabella seguente. <br/> |
| 16 <br/> | 12 <br/> | Data <br/>          | Data e ora di creazione del membro di archiviazione: rappresentazione decimale ASCII del numero di secondi trascorsi dall'1/1/1970 UCT. <br/>                                                    |
| 28 <br/> | 6 <br/>  | ID utente <br/>       | Rappresentazione decimale ASCII dell'ID utente. Questo campo non contiene un valore significativo nelle piattaforme Windows perché gli strumenti Microsoft generano tutti spazi vuoti. <br/>                                    |
| 34 <br/> | 6 <br/>  | ID gruppo <br/>      | Rappresentazione decimale ASCII dell'ID gruppo. Questo campo non contiene un valore significativo nelle piattaforme Windows perché gli strumenti Microsoft generano tutti spazi vuoti. <br/>                                   |
| 40 <br/> | 8 <br/>  | Mode <br/>          | Rappresentazione ottale ASCII della modalità file del membro. Si tratta del valore ST \_ MODE della funzione di run-time C \_ wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Dimensione <br/>          | Rappresentazione decimale ASCII delle dimensioni totali del membro di archivio, senza includere la dimensione dell'intestazione. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Fine dell'intestazione <br/> | I due byte nella stringa C " più \\ n" (0x60 0x0A). <br/>                                                                                                                                               |



 

Il campo Nome ha uno dei formati illustrati nella tabella seguente. Come accennato in precedenza, ognuna di queste stringhe viene giustificata a sinistra e riempita con spazi finali all'interno di un campo di 16 byte:



| Contenuto del campo Nome | Descrizione                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name/ <br/>      | Nome del membro di archiviazione. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | Il membro archive è uno dei due membri del linker. Entrambi i membri del linker hanno questo nome. <br/>                                                                                                                                                                                          |
| // <br/>         | Il membro archive è il membro longnames, costituito da una serie di stringhe ASCII con terminazione Null. Il membro longnames è il terzo membro di archivio ed è facoltativo. <br/>                                                                     |
| /n <br/>         | Il nome del membro di archiviazione si trova in corrispondenza dell'offset n all'interno del membro longnames. Il numero n è la rappresentazione decimale dell'offset. Ad esempio: "/26" indica che il nome del membro di archiviazione si trova a 26 byte oltre l'inizio del contenuto del membro longnames. <br/> |



 

### <a name="first-linker-member"></a>Primo membro del linker

Il nome del primo membro del linker è "/". Il primo membro del linker è incluso per compatibilità con le versioni precedenti. Non viene usato dai linker correnti, ma il formato deve essere corretto. Questo membro del linker fornisce una directory di nomi di simboli, così come il secondo membro del linker. Per ogni simbolo, le informazioni indicano dove trovare il membro di archivio che contiene il simbolo.

Il primo membro del linker ha il formato seguente. Queste informazioni vengono visualizzate dopo l'intestazione :



| Offset         | Dimensione               | Campo                         | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Numero di simboli <br/> | Valore long senza segno che contiene il numero di simboli indicizzati. Questo numero viene archiviato in formato big-endian. Ogni membro del file oggetto definisce in genere uno o più simboli esterni. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Offset <br/>           | Matrice di offset di file per archiviare le intestazioni dei membri, in cui n è uguale al campo Number of Symbols. Ogni numero nella matrice è un valore unsigned long archiviato in formato big-endian. Per ogni simbolo denominato nella tabella di stringhe, l'elemento corrispondente nella matrice offsets fornisce la posizione del membro di archivio che contiene il simbolo. <br/> |
| \* <br/> | \* <br/>     | Tabella delle stringhe <br/>      | Serie di stringhe con terminazione Null che denotono tutti i simboli nella directory. Ogni stringa inizia immediatamente dopo il carattere Null nella stringa precedente. Il numero di stringhe deve essere uguale al valore del campo Numero di simboli. <br/>                                                                                                       |



 

Gli elementi nella matrice offsets devono essere disposti in ordine crescente. Ciò implica che i simboli nella tabella di stringhe devono essere disposti in base all'ordine dei membri dell'archivio. Ad esempio, tutti i simboli nel primo membro del file oggetto devono essere elencati prima dei simboli nel secondo file oggetto.

### <a name="second-linker-member"></a>Secondo membro del linker

Il secondo membro del linker ha il nome "/" come il primo membro del linker. Anche se entrambi i membri del linker forniscono una directory di simboli e membri di archivio che li contengono, il secondo membro del linker viene usato in preferenza per il primo da tutti i linker correnti. Il secondo membro del linker include i nomi dei simboli in ordine lessicale, in modo da velocizzare la ricerca in base al nome.

Il secondo membro ha il formato seguente. Queste informazioni vengono visualizzate dopo l'intestazione :



| Offset         | Dimensione               | Campo                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Numero di membri <br/> | Valore long senza segno che contiene il numero di membri di archivio. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* m <br/> | Offset <br/>           | Matrice di offset di file per archiviare le intestazioni dei membri, disposti in ordine crescente. Ogni offset è un valore long senza segno. Il numero m è uguale al valore del campo Number of Members. <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Numero di simboli <br/> | Valore long senza segno che contiene il numero di simboli indicizzati. Ogni membro del file oggetto definisce in genere uno o più simboli esterni. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Indici <br/>           | Matrice di indici in base 1 (unsigned short) che esegue il mapping dei nomi dei simboli agli offset dei membri di archivio. Il numero n è uguale al campo Numero di simboli. Per ogni simbolo denominato nella tabella di stringhe, l'elemento corrispondente nella matrice Indicis fornisce un indice nella matrice offsets. La matrice offsets, a sua volta, fornisce la posizione del membro di archivio che contiene il simbolo. <br/> |
| \* <br/> | \* <br/>     | Tabella delle stringhe <br/>      | Serie di stringhe con terminazione Null che denotono tutti i simboli nella directory. Ogni stringa inizia immediatamente dopo il byte Null nella stringa precedente. Il numero di stringhe deve essere uguale al valore del campo Numero di simboli. Questa tabella elenca tutti i nomi dei simboli in ordine lessicale crescente. <br/>                                                                             |



 

### <a name="longnames-member"></a>Membro longnames

Il nome del membro longnames è "//". Il membro longnames è una serie di stringhe di nomi di membri di archivio. Un nome viene visualizzato qui solo quando lo spazio nel campo Nome non è sufficiente (16 byte). Il membro longnames è facoltativo. Può essere vuoto con solo un'intestazione oppure può essere completamente assente senza nemmeno un'intestazione.

Le stringhe hanno terminazione Null. Ogni stringa inizia immediatamente dopo il byte Null nella stringa precedente.

## <a name="import-library-format"></a>Importare il formato della libreria

- [Importa intestazione](#import-header)
- [Tipo di importazione](#import-type)

Le librerie di importazione tradizionali, ovvero le librerie che descrivono le esportazioni da un'immagine per l'uso da parte di un'altra, seguono in genere il layout descritto nella sezione 7, Formato di file di archivio [(libreria).](#archive-library-file-format) La differenza principale è che i membri della libreria di importazione contengono file pseudo-oggetto anziché file reali, in cui ogni membro include i contributi della sezione necessari per compilare le tabelle di importazione descritte nella sezione 6.4. La sezione [.idata](#the-idata-section) Il linker genera questo archivio durante la compilazione dell'applicazione di esportazione.

I contributi della sezione per un'importazione possono essere dedotto da un piccolo set di informazioni. Il linker può generare le informazioni complete e dettagliate nella libreria di importazione per ogni membro al momento della creazione della libreria o scrivere solo le informazioni canoniche nella libreria e consentire all'applicazione che la usa in un secondo momento di generare i dati necessari in tempo reale.

In una libreria di importazione con formato lungo, un singolo membro contiene le informazioni seguenti:

<dl> Archiviare l'intestazione del membro  
Intestazione del file  
Intestazioni di sezione  
Dati che corrispondono a ognuna delle intestazioni di sezione  
Tabella dei simboli COFF  
Stringhe  
  
</dl>

Al contrario, una libreria di importazione breve viene scritta come segue:

<dl> Archiviare l'intestazione del membro  
Importare l'intestazione  
Stringa del nome di importazione con terminazione Null  
Stringa del nome DLL con terminazione Null  
</dl>

Si tratta di informazioni sufficienti per ricostruire accuratamente l'intero contenuto del membro al momento dell'uso.

### <a name="import-header"></a>Importa intestazione

L'intestazione import contiene i campi e gli offset seguenti:



| Offset         | Dimensione                | Campo                       | Descrizione                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | Deve essere IMAGE \_ FILE \_ MACHINE \_ UNKNOWN. Per altre informazioni, vedere [Tipi di computer.](#machine-types) <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Deve essere 0xFFFF. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Versione <br/>         | Versione della struttura. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Computer <br/>         | Numero che identifica il tipo di computer di destinazione. Per altre informazioni, vedere [Tipi di computer.](#machine-types)<br/> |
| 8 <br/>  | 4 <br/>       | Time-Date stamp <br/> | Data e ora di creazione del file. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Dimensioni dei dati <br/>    | Dimensioni delle stringhe che seguono l'intestazione. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordinale/Hint <br/>    | Ordinale o hint per l'importazione, determinato dal valore nel campo Tipo nome. <br/>                   |
| 18 <br/> | 2 bit <br/>  | Tipo <br/>            | Tipo di importazione. Per descrizioni e valori specifici, vedere [Import Type](#import-type).<br/>                           |
|                | 3 bit <br/>  | Tipo di nome <br/>       | Tipo di nome dell'importazione. Per altre informazioni, vedere [Import Name Type](#import-name-type). <br/>                           |
|                | 11 bit <br/> | Riservato <br/>        | Riservato, deve essere 0. <br/>                                                                                             |



 

Questa struttura è seguita da due stringhe con terminazione Null che descrivono il nome del simbolo importato e la DLL da cui deriva.

### <a name="import-type"></a>Tipo di importazione

Per il campo Tipo nell'intestazione di importazione vengono definiti i valori seguenti:

| Costante                  | Valore         | Descrizione                                      |
|---------------------------|---------------|--------------------------------------------------|
| IMPORTARE \_ IL CODICE <br/>  | 0 <br/> | Codice eseguibile. <br/>                     |
| IMPORTARE \_ I DATI <br/>  | 1 <br/> | Dati. <br/>                                |
| IMPORT \_ CONST <br/> | 2 <br/> | Specificato come CONST nel file def. <br/> |

Questi valori vengono usati per determinare quali contributi di sezione devono essere generati dallo strumento che usa la libreria se deve accedere a tali dati.

### <a name="import-name-type"></a>Tipo di nome di importazione

Il nome del simbolo di importazione con terminazione Null segue immediatamente l'intestazione di importazione associata. I valori seguenti sono definiti per il campo Tipo nome nell'intestazione di importazione. Indicano come usare il nome per generare i simboli corretti che rappresentano l'importazione:

| Costante | Valore | Descrizione |
| - | - | - |
| ORDINALE \_ IMPORT | 0 | L'importazione è ordinale. Ciò indica che il valore nel campo Ordinal/Hint dell'intestazione di importazione è l'ordinale dell'importazione. Se questa costante non viene specificata, il campo Ordinal/Hint deve essere sempre interpretato come hint dell'importazione. |
| IMPORT \_ NAME | 1 | Il nome dell'importazione è identico al nome del simbolo pubblico. |
| IMPORT \_ NAME \_ NOPREFIX | 2 | Il nome dell'importazione è il nome del simbolo pubblico, ignorando il carattere ?, @o facoltativamente \_ . |
| IMPORT \_ NAME \_ UNDECORATE | 3 | Il nome dell'importazione è il nome del simbolo pubblico, ignorando il carattere ?, @o, facoltativamente, e troncando in corrispondenza \_ del primo @ . |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Appendice A: Calcolo dell'hash dell'immagine Authenticode PE

- [Che cos'è un hash di immagine PE Authenticode?](#what-is-an-authenticode-pe-image-hash)
- [Che cosa viene coperto in un hash di immagine PE Authenticode?](#what-is-covered-in-an-authenticode-pe-image-hash)

È previsto l'uso di diversi certificati di attributo per verificare l'integrità delle immagini. Tuttavia, la più comune è la firma Authenticode. Una firma Authenticode può essere usata per verificare che le sezioni pertinenti di un file di immagine PE non siano state modificate in alcun modo dal formato originale del file. Per eseguire questa attività, le firme Authenticode contengono un elemento denominato hash dell'immagine PE

### <a name="what-is-an-authenticode-pe-image-hash"></a>Che cos'è un hash di immagine PE Authenticode?

L'hash dell'immagine Authenticode PE, o hash del file, è simile a un checksum di file in quanto produce un valore ridotto correlato all'integrità di un file. Un checksum viene generato da un algoritmo semplice e viene usato principalmente per rilevare gli errori di memoria. Ciò significa che viene usato per rilevare se un blocco di memoria su disco è danneggiato e se i valori archiviati in tale blocco sono danneggiati. Un hash di file è simile a un checksum in quanto rileva anche il danneggiamento del file. Tuttavia, a differenza della maggior parte degli algoritmi di checksum, è molto difficile modificare un file in modo che abbia lo stesso hash di file del formato originale (non modificato). In altre parole, un checksum è progettato per rilevare errori di memoria semplici che causano il danneggiamento, ma è possibile usare un hash di file per rilevare modifiche intenzionali e persino leggere a un file, ad esempio quelle introdotte da virus, pirati informatici o programmi trojan horse.

In una firma Authenticode l'hash del file viene firmato digitalmente usando una chiave privata nota solo al firmatario del file. Un consumer di software può verificare l'integrità del file calcolando il valore hash del file e confrontandolo con il valore dell'hash firmato contenuto nella firma digitale Authenticode. Se gli hash dei file non corrispondono, parte del file coperto dall'hash dell'immagine PE è stata modificata.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>Che cosa viene coperto in un hash di immagine PE Authenticode?

Non è possibile o consigliabile includere tutti i dati del file di immagine nel calcolo dell'hash dell'immagine PE. A volte presenta semplicemente caratteristiche indesiderate (ad esempio, le informazioni di debug non possono essere rimosse dai file rilasciati pubblicamente); a volte è semplicemente impossibile. Ad esempio, non è possibile includere tutte le informazioni all'interno di un file di immagine in una firma Authenticode, quindi inserire la firma Authenticode che contiene l'hash dell'immagine PE nell'immagine PE e successivamente essere in grado di generare un hash di immagine PE identico includendo nuovamente tutti i dati del file di immagine nel calcolo, perché il file contiene ora la firma Authenticode che non era originariamente presente.

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Processo per la generazione dell'hash dell'immagine PE Authenticode

Questa sezione descrive come viene calcolato un hash dell'immagine PE e quali parti dell'immagine PE possono essere modificate senza invalidare la firma Authenticode.

> [!NOTE]
> L'hash dell'immagine PE per un file specifico può essere incluso in un file di catalogo separato senza includere un certificato di attributo all'interno del file con hash. Ciò è rilevante perché diventa possibile invalidare l'hash dell'immagine PE in un file di catalogo firmato con Authenticode modificando un'immagine PE che non contiene effettivamente una firma Authenticode.

Tutti i dati nelle sezioni dell'immagine PE specificati nella tabella della sezione vengono con hash nella loro interezza, ad eccezione degli intervalli di esclusione seguenti:

- **Campo CheckSum del file Windows campi specifici dell'intestazione facoltativa.** Questo checksum include l'intero file (inclusi eventuali certificati di attributo nel file). Con tutta probabilità, il checksum sarà diverso dal valore originale dopo l'inserimento della firma Authenticode.

- **Informazioni relative ai certificati degli attributi.** Le aree dell'immagine PE correlate alla firma Authenticode non sono incluse nel calcolo dell'hash dell'immagine PE perché le firme Authenticode possono essere aggiunte o rimosse da un'immagine senza influire sull'integrità complessiva dell'immagine. Questo non è un problema, perché esistono scenari utente che dipendono dalla nuova firma di immagini PE o dall'aggiunta di un timestamp. Authenticode esclude le informazioni seguenti dal calcolo hash:

  - Campo Tabella certificati delle directory dei dati di intestazione facoltative.

  - Tabella dei certificati e certificati corrispondenti a cui punta il campo Tabella certificati elencato immediatamente sopra.

  Per calcolare l'hash dell'immagine PE, Authenticode ordina le sezioni specificate nella tabella di sezione in base all'intervallo di indirizzi, quindi esegue l'hashing della sequenza di byte risultante, passando gli intervalli di esclusione.

- **Informazioni oltre la fine dell'ultima sezione.** L'area oltre l'ultima sezione (definita dall'offset più alto) non ha un hash. Questa area contiene in genere informazioni di debug. Le informazioni di debug possono in genere essere considerate advisory per i debugger. non influisce sull'integrità effettiva del programma eseguibile. È letteralmente possibile rimuovere le informazioni di debug da un'immagine dopo la consegna di un prodotto e non influire sulla funzionalità del programma. In realtà, questa operazione viene talvolta eseguita come misura di salvataggio su disco. Vale la pena notare che le informazioni di debug contenute nelle sezioni specificate dell'immagine PE non possono essere rimosse senza invalidare la firma Authenticode.

È possibile usare gli strumenti makecert e signtool disponibili in Windows Platform SDK per sperimentare la creazione e la verifica delle firme Authenticode. Per altre informazioni, vedere Le informazioni di riferimento sono riportate di seguito.

## <a name="references"></a>Riferimenti

[Download e strumenti per Windows (include Windows SDK)](https://developer.microsoft.com/windows/downloads)

[Creazione, visualizzazione e gestione dei certificati](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Procedura dettagliata per la firma del codice in modalità kernel (.doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Windows Authenticode Portable Executable Signature Format (.docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[Funzioni imageHlp](/windows/desktop/Debug/imagehlp-functions)
