---
description: Questa specifica descrive la struttura dei file eseguibili (immagine) e dei file oggetto nella famiglia di sistemi operativi Windows. Questi file sono indicati rispettivamente come file eseguibili di tipo PE (Portable Executable) e COFF (Common Object File Format).
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: Formato PE
ms.topic: article
ms.date: 03/31/2021
ms.custom: contperf-fy21q1
ms.openlocfilehash: 3cc6fd777bca831ca4424baaa81c5525a24556ec
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2021
ms.locfileid: "106334310"
---
# <a name="pe-format"></a>Formato PE

Questa specifica descrive la struttura dei file eseguibili (immagine) e dei file oggetto nella famiglia di sistemi operativi Windows. Questi file sono indicati rispettivamente come file eseguibili di tipo PE (Portable Executable) e COFF (Common Object File Format).

> [!Note]  
> Questo documento viene fornito per facilitare lo sviluppo di strumenti e applicazioni per Windows, ma non è garantita una specifica completa per tutti gli aspetti. Microsoft si riserva il diritto di modificare il documento senza preavviso.

Questa revisione del file eseguibile portabile Microsoft e della specifica del formato file oggetto comune sostituisce tutte le revisioni precedenti di questa specifica.

## <a name="general-concepts"></a>Concetti generali

Questo documento specifica la struttura dei file eseguibili (immagine) e dei file oggetto nella famiglia di sistemi operativi Microsoft Windows. Questi file sono indicati rispettivamente come file eseguibili di tipo PE (Portable Executable) e COFF (Common Object File Format). Il nome "Portable Executable" si riferisce al fatto che il formato non è specifico dell'architettura.

Nella tabella seguente vengono descritti alcuni concetti visualizzati in questa specifica:

| Nome                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| certificato attributo <br/> | Certificato utilizzato per associare le istruzioni verificabili a un'immagine. Una serie di istruzioni verificabili diverse può essere associata a un file. uno dei più utili è costituito da un'istruzione di un produttore di software che indica il digest del messaggio dell'immagine che dovrebbe essere. Un digest del messaggio è simile a un checksum, ad eccezione del fatto che è molto difficile da forgiare. Pertanto, è molto difficile modificare un file per avere lo stesso digest del messaggio del file originale. L'istruzione può essere verificata come stabilita dal produttore utilizzando schemi di crittografia a chiave pubblica o privata. In questo documento vengono descritti i dettagli relativi ai certificati di attributi diversi da per consentire l'inserimento nei file di immagine. <br/> |
| indicatore di data e ora <br/>       | Timbro utilizzato per scopi diversi in diverse posizioni in un file PE o COFF. Nella maggior parte dei casi, il formato di ogni timbro è identico a quello usato dalle funzioni temporali nella libreria di runtime del linguaggio C. Per le eccezioni, vedere il descriptor del tipo di debug dell'immagine ripetizione del tipo di debug \_ \_ \_ . [](#debug-type) Se il valore del timbro è 0 o 0xFFFFFFFF, non rappresenta un indicatore di data/ora reale o significativo. <br/>                                                                                                                                                                                                                                                                                                                                            |
| puntatore a file <br/>          | Posizione di un elemento all'interno del file stesso, prima dell'elaborazione da parte del linker (nel caso dei file oggetto) o del caricatore (nel caso di file di immagine). In altre parole, si tratta di una posizione all'interno del file archiviata su disco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| linker <br/>                | Riferimento al linker fornito con Microsoft Visual Studio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| file oggetto <br/>           | File fornito come input per il linker. Il linker produce un file di immagine, che a sua volta viene usato come input dal caricatore. Il termine "file oggetto" non implica necessariamente alcuna connessione alla programmazione orientata a oggetti. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| riservato, deve essere 0 <br/>   | Descrizione di un campo che indica che il valore del campo deve essere zero per i generatori e che i consumer devono ignorare il campo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indirizzo RVA (relativo Virtual Address) <br/>                   | In un file di immagine, questo è l'indirizzo di un elemento dopo che è stato caricato in memoria, con l'indirizzo di base del file di immagine sottratto. Il RVA di un elemento è quasi sempre diverso dalla relativa posizione all'interno del file su disco (puntatore di file). <br/> In un file oggetto, un RVA è meno significativo perché i percorsi di memoria non sono assegnati. In questo caso, un RVA è un indirizzo all'interno di una sezione (descritto più avanti in questa tabella) a cui viene applicata una rilocazione in un secondo momento durante il collegamento. Per semplicità, un compilatore deve semplicemente impostare il primo RVA in ogni sezione su zero. <br/>                                                                                                                                         |
| section <br/>               | Unità di base del codice o dei dati all'interno di un file PE o COFF. Ad esempio, tutto il codice in un file oggetto può essere combinato in un'unica sezione o (a seconda del comportamento del compilatore) ogni funzione può occupare una sezione specifica. Con più sezioni, si verifica un sovraccarico di file, ma il linker è in grado di collegarsi più selettivamente al codice. Una sezione è simile a un segmento nell'architettura Intel 8086. Tutti i dati non elaborati in una sezione devono essere caricati in modo contiguo. Inoltre, un file di immagine può contenere una serie di sezioni, ad esempio. TLS o. reloc, che hanno scopi speciali. <br/>                                                                                                                                                                      |
| Indirizzo virtuale (VA) <br/>                    | Uguale a RVA, tranne per il fatto che l'indirizzo di base del file di immagine non viene sottratto. L'indirizzo viene chiamato VA perché Windows crea uno spazio VA distinto per ogni processo, indipendentemente dalla memoria fisica. Per quasi tutti gli scopi, un VA considerato solo un indirizzo. Un VA non è come prevedibile come RVA perché il caricatore potrebbe non caricare l'immagine nel percorso preferito. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Panoramica

Nell'elenco seguente viene descritto il formato eseguibile di Microsoft PE, con la base dell'intestazione dell'immagine nella parte superiore. La sezione dell'intestazione EXE compatibile con MS-DOS 2,0 fino alla sezione non utilizzata immediatamente prima dell'intestazione PE è la sezione MS-DOS 2,0 e viene utilizzata solo per la compatibilità con MS-DOS.

-   Intestazione EXE compatibile con MS-DOS 2,0
-   unused
-   Identificatore OEM

    Informazioni OEM

    Offset nell'intestazione PE

-   Programma stub MS-DOS 2,0 e tabella di rilocazione

-   unused

-   Intestazione PE (allineata al limite di 8 byte)

-   Intestazioni di sezione
-   Pagine immagine:

    Importa informazioni

    Esporta informazioni

    rilocazioni di base

    informazioni sulle risorse

Nell'elenco seguente viene descritto il formato oggetto COFF Microsoft:

-   Intestazione COFF Microsoft
-   Intestazioni di sezione
-   Dati non elaborati:

    codice

    data

    informazioni di debug

    delocalizzazioni

## <a name="file-headers"></a>Intestazioni di file

- [Stub MS-DOS (solo immagine)](#ms-dos-stub-image-only)
- [Firma (solo immagine)](#signature-image-only)
- [Intestazione del file COFF (oggetto e immagine)](#coff-file-header-object-and-image)
  - [Tipi di computer](#machine-types)
  - [Caratteristiche](#characteristics)
- [Intestazione facoltativa (solo immagine)](#optional-header-image-only)
  - [Campi facoltativi intestazione standard (solo immagine)](#optional-header-standard-fields-image-only)
  - [Intestazione facoltativa Windows-Specific campi (solo immagine)](#optional-header-windows-specific-fields-image-only)
  - [Directory di dati intestazione facoltativa (solo immagine)](#optional-header-data-directories-image-only)

L'intestazione del file PE è costituita da uno stub Microsoft MS-DOS, dalla firma PE, dall'intestazione del file COFF e da un'intestazione facoltativa. L'intestazione di un file oggetto COFF è costituita da un'intestazione di file COFF e da un'intestazione facoltativa. In entrambi i casi, le intestazioni dei file sono seguite immediatamente dalle intestazioni di sezione.

### <a name="ms-dos-stub-image-only"></a>Stub MS-DOS (solo immagine)

Lo stub MS-DOS è un'applicazione valida che viene eseguita in MS-DOS. Viene posizionata all'inizio dell'immagine EXE. Il linker inserisce uno stub predefinito, che Visualizza il messaggio "Impossibile eseguire il programma in modalità DOS" quando l'immagine viene eseguita in MS-DOS. L'utente può specificare uno stub diverso usando l'opzione del linker/STUB.

Nel percorso 0x3C lo stub presenta l'offset del file alla firma PE. Queste informazioni consentono a Windows di eseguire correttamente il file di immagine, anche se dispone di uno stub MS-DOS. Questo offset del file si trova nel percorso 0x3C durante il collegamento.

### <a name="signature-image-only"></a>Firma (solo immagine)

Dopo lo stub MS-DOS, in corrispondenza dell'offset del file specificato in offset 0x3C, è una firma a 4 byte che identifica il file come file di immagine in formato PE. Questa firma è "PE \\ 0 \\ 0" (lettere "P" E "e" seguite da due byte null).

### <a name="coff-file-header-object-and-image"></a>Intestazione del file COFF (oggetto e immagine)

All'inizio di un file oggetto o subito dopo la firma di un file di immagine, è un'intestazione di file COFF standard nel formato seguente. Si noti che il caricatore di Windows limita il numero di sezioni a 96.

| Offset         | Dimensione          | Campo                            | Descrizione                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Computer <br/>              | Numero che identifica il tipo di computer di destinazione. Per ulteriori informazioni, vedere [tipi di computer](#machine-types). <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | NumberOfSections <br/>     | Numero di sezioni. Indica la dimensione della tabella della sezione che segue immediatamente le intestazioni. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | I 32 bit bassi del numero di secondi a partire 00:00 dal 1 ° gennaio 1970 (valore t time runtime C \_ ), che indica quando è stato creato il file. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | PointerToSymbolTable <br/> | Offset del file della tabella dei simboli COFF oppure zero se non è presente alcuna tabella dei simboli COFF. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                                                                           |
| 12 <br/> | 4 <br/> | NumberOfSymbols <br/>      | Numero di voci nella tabella dei simboli. Questi dati possono essere usati per individuare la tabella di stringhe che segue immediatamente la tabella dei simboli. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                        |
| 16 <br/> | 2 <br/> | SizeOfOptionalHeader <br/> | Dimensione dell'intestazione facoltativa, necessaria per i file eseguibili, ma non per i file oggetto. Questo valore deve essere zero per file oggetto. Per una descrizione del formato di intestazione, vedere [intestazione facoltativa (solo immagine)](#optional-header-image-only). <br/> |
| 18 <br/> | 2 <br/> | Caratteristiche <br/>      | Flag che indicano gli attributi del file. Per valori di flag specifici, vedere [caratteristiche](#characteristics). <br/>                                                                                                                               |

#### <a name="machine-types"></a>Tipi di computer

Il campo del computer ha uno dei valori seguenti, che specificano il tipo di CPU. Un file di immagine può essere eseguito solo nel computer specificato o in un sistema che emula il computer specificato.

| Costante                                    | Valore              | Descrizione                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| \_computer file di immagine \_ \_ sconosciuto <br/>   | 0x0 <br/>    | Si presuppone che il contenuto di questo campo sia applicabile a qualsiasi tipo di computer <br/> |
| FILE di immagine \_ \_ AM33 del computer \_ <br/>      | 0x1d3 <br/>  | AM33 di Matsushita <br/>                                                             |
| FILE di immagine \_ \_ amd64 del computer \_ <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| FILE di immagine del \_ \_ computer \_ ARM <br/>       | 0x1c0 <br/>  | little endian ARM <br/>                                                           |
| FILE di immagine \_ \_ arm64 del computer \_ <br/>     | 0xaa64 <br/> | little endian ARM64 <br/>                                                         |
| FILE di immagine \_ \_ ARMNT del computer \_ <br/>     | 0x1c4 <br/>  | Pollice little endian ARM-2 <br/>                                                   |
| FILE di immagine del \_ \_ computer \_ EBC <br/>       | 0xebc <br/>  | Codice byte EFI <br/>                                                               |
| FILE di immagine \_ \_ i386 del computer \_ <br/>      | 0x14c <br/>  | Processori Intel 386 o versioni successive e processori compatibili <br/>                     |
| Computer del file di immagine \_ \_ \_ ia64 <br/>      | 0x200 <br/>  | Famiglia di processori Intel Itanium <br/>                                              |
| FILE di immagine \_ \_ M32R del computer \_ <br/>      | 0x9041 <br/> | little endian Mitsubishi M32R <br/>                                               |
| FILE di immagine \_ \_ MIPS16 del computer \_ <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| FILE di immagine \_ \_ MIPSFPU del computer \_ <br/>   | 0x366 <br/>  | MIPS con FPU <br/>                                                               |
| FILE di immagine \_ \_ MIPSFPU16 del computer \_ <br/> | 0x466 <br/>  | MIPS16 con FPU <br/>                                                             |
| computer con file di immagine \_ \_ \_ PowerPC <br/>   | 0x1f0 <br/>  | little endian Power PC <br/>                                                      |
| FILE di immagine \_ \_ POWERPCFP del computer \_ <br/> | 0x1f1 <br/>  | Power PC con supporto a virgola mobile <br/>                                        |
| FILE di immagine \_ \_ R4000 del computer \_ <br/>     | 0x166 <br/>  | little endian MIPS <br/>                                                          |
| FILE di immagine \_ \_ RISCV32 del computer \_ <br/>   | 0x5032 <br/> | Spazio degli indirizzi RISC-V a 32 bit <br/>                                                 |
| FILE di immagine \_ \_ RISCV64 del computer \_ <br/>   | 0x5064 <br/> | Spazio degli indirizzi RISC-V a 64 bit <br/>                                                 |
| FILE di immagine \_ \_ RISCV128 del computer \_ <br/>  | 0x5128 <br/> | Spazio degli indirizzi RISC-V a 128 bit <br/>                                                |
| FILE di immagine \_ \_ SH3 del computer \_ <br/>       | 0x1a2 <br/>  | SH3 Hitachi <br/>                                                                 |
| FILE di immagine \_ \_ SH3DSP del computer \_ <br/>    | 0x1a3 <br/>  | Hitachi SH3 DSP <br/>                                                             |
| FILE di immagine \_ \_ SH4 del computer \_ <br/>       | 0x1a6 <br/>  | SH4 Hitachi <br/>                                                                 |
| FILE di immagine \_ \_ SH5 del computer \_ <br/>       | 0x1a8 <br/>  | SH5 Hitachi <br/>                                                                 |
| \_Thumb del \_ computer del file di immagine \_ <br/>     | 0x1c2 <br/>  | Thumb <br/>                                                                       |
| FILE di immagine \_ \_ WCEMIPSV2 del computer \_ <br/> | 0x169 <br/>  | MIPS little-endian WCE V2 <br/>                                                   |

#### <a name="characteristics"></a>Caratteristiche

Il campo caratteristiche contiene flag che indicano gli attributi dell'oggetto o del file di immagine. Sono attualmente definiti i flag seguenti:

| Flag                                                 | valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILE di immagine \_ \_ rilocazioni \_ rimosso <br/>            | 0x0001 <br/> | Solo immagine, Windows CE e Microsoft Windows NT e versioni successive. Ciò indica che il file non contiene rilocazioni di base e deve pertanto essere caricato nell'indirizzo di base preferito. Se l'indirizzo di base non è disponibile, il caricatore segnala un errore. Il comportamento predefinito del linker consiste nel rimuovere le rilocazioni di base dai file eseguibili (EXE). <br/> |
| \_ \_ immagine eseguibile del file di immagine \_ <br/>           | 0x0002 <br/> | Solo immagine. Indica che il file di immagine è valido e può essere eseguito. Se questo flag non è impostato, indica un errore del linker. <br/>                                                                                                                                                                                                                          |
| \_ \_ nums righe file \_ immagine \_ rimosse <br/>        | 0x0004 <br/> | I numeri di riga COFF sono stati rimossi. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                                                                                       |
| \_Syms locale file di immagine \_ \_ \_ rimosso <br/>       | 0x0008 <br/> | Sono state rimosse le voci della tabella dei simboli COFF per i simboli locali. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                                                             |
| FILE di immagine \_ \_ aggressivo \_ WS \_ Trim <br/>        | 0x0010 <br/> | Obsoleta. Tagliare in modo aggressivo working set. Questo flag è deprecato per Windows 2000 e versioni successive e deve essere zero. <br/>                                                                                                                                                                                                                                          |
| FILE di immagine con \_ \_ indirizzo di grandi dimensioni \_ \_ <br/>      | 0x0020 <br/> | L'applicazione può gestire > indirizzi da 2 GB. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Questo flag è riservato per un utilizzo futuro. <br/>                                                                                                                                                                                                                                                                                                                  |
| byte del file di immagine \_ \_ \_ invertito \_ lo <br/>         | 0x0080 <br/> | Little endian: il bit meno significativo (LSB) precede il bit più significativo (MSB) in memoria. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                          |
| \_Computer a \_ 32 bit del file di immagine \_ <br/>              | 0x0100 <br/> | Il computer si basa su un'architettura a 32 bit. <br/>                                                                                                                                                                                                                                                                                                        |
| DEBUG del file di immagine \_ \_ \_ rimosso <br/>             | 0x0200 <br/> | Le informazioni di debug vengono rimosse dal file di immagine. <br/>                                                                                                                                                                                                                                                                                                  |
| \_file \_ di immagine rimovibile \_ eseguito \_ dallo \_ scambio <br/> | 0x0400 <br/> | Se l'immagine si trova su un supporto rimovibile, caricarla completamente e copiarla nel file di scambio. <br/>                                                                                                                                                                                                                                                                        |
| \_file \_ di immagine NET \_ Run \_ da \_ swap <br/>        | 0x0800 <br/> | Se l'immagine si trova in un supporto di rete, caricarla completamente e copiarla nel file di scambio. <br/>                                                                                                                                                                                                                                                                          |
| \_file \_ System immagine <br/>                      | 0x1000 <br/> | Il file di immagine è un file di sistema, non un programma utente. <br/>                                                                                                                                                                                                                                                                                                   |
| \_dll file di immagine \_ <br/>                         | 0x2000 <br/> | Il file di immagine è una libreria di collegamento dinamico (DLL). Tali file sono considerati file eseguibili per quasi tutti gli scopi, sebbene non possano essere eseguiti direttamente. <br/>                                                                                                                                                                                              |
| \_solo file di immagine \_ su \_ sistema \_ <br/>            | 0x4000 <br/> | Il file deve essere eseguito solo su un computer uniprocessore. <br/>                                                                                                                                                                                                                                                                                                 |
| FILE di immagine \_ \_ byte \_ invertiti \_ <br/>         | 0x8000 <br/> | Big endian: il MSB precede il LSB in memoria. Questo flag è deprecato e deve essere zero. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>Intestazione facoltativa (solo immagine)

Ogni file di immagine ha un'intestazione facoltativa che fornisce informazioni al caricatore. Questa intestazione è facoltativa nel senso che alcuni file (in particolare i file oggetto) non lo hanno. Per i file di immagine, questa intestazione è obbligatoria. Un file oggetto può avere un'intestazione facoltativa, ma in genere questa intestazione non dispone di alcuna funzione in un file oggetto, tranne che per aumentarne le dimensioni.

Si noti che la dimensione dell'intestazione facoltativa non è fissa. Il campo **SizeOfOptionalHeader** nell'intestazione COFF deve essere usato per convalidare che un probe nel file per una particolare directory dati non vada oltre **SizeOfOptionalHeader**. Per ulteriori informazioni, vedere l' [intestazione del file COFF (oggetto e immagine)](#coff-file-header-object-and-image).

Il campo **NumberOfRvaAndSizes** dell'intestazione facoltativa deve essere usato anche per assicurarsi che nessun Probe per una voce di directory dati specifica vada oltre l'intestazione facoltativa. Inoltre, è importante convalidare il numero magico dell'intestazione facoltativa per la compatibilità del formato.

Il numero magico dell'intestazione facoltativa determina se un'immagine è un file eseguibile PE32 o PE32 +.

| Numero magico      | Formato PE         |
|-------------------|-------------------|
| 0x10b <br/> | PE32 <br/>  |
| 0x20b <br/> | PE32 + <br/> |

PE32 + images consente uno spazio degli indirizzi a 64 bit, limitando la dimensione dell'immagine a 2 gigabyte. Altre PE32 e modifiche vengono risolte nelle rispettive sezioni.

L'intestazione facoltativa ha tre parti principali.

| Offset (PE32/PE32 +) | Dimensioni (PE32/PE32 +)    | Parte intestazione                         | Descrizione                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Campi standard <br/>         | Campi definiti per tutte le implementazioni di COFF, incluso UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | Campi specifici di Windows <br/> | Campi aggiuntivi per supportare funzionalità specifiche di Windows, ad esempio i sottosistemi. <br/>                                                                              |
| 96/112 <br/>  | Variabile <br/> | Directory dati <br/>        | Coppie di indirizzi/dimensioni per tabelle speciali presenti nel file di immagine e utilizzate dal sistema operativo (ad esempio, la tabella di importazione e la tabella di esportazione). <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Campi facoltativi intestazione standard (solo immagine)

I primi otto campi dell'intestazione facoltativa sono campi standard definiti per ogni implementazione di COFF. Questi campi contengono informazioni generali utili per il caricamento e l'esecuzione di un file eseguibile. Sono invariati per il formato PE32 +.

| Offset         | Dimensione          | Campo                               | Descrizione                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Magic <br/>                   | Unsigned Integer che identifica lo stato del file di immagine. Il numero più comune è 0x10B, che lo identifica come un normale file eseguibile. 0x107 lo identifica come immagine ROM e 0x20B lo identifica come un eseguibile PE32 +. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | MajorLinkerVersion <br/>      | Numero di versione principale del linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | MinorLinkerVersion <br/>      | Numero di versione secondaria del linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | SizeOfCode <br/>              | Dimensioni della sezione del codice (testo) o della somma di tutte le sezioni di codice se sono presenti più sezioni. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | SizeOfInitializedData <br/>   | Dimensioni della sezione dei dati inizializzati o la somma di tutte le sezioni se sono presenti più sezioni di dati. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | SizeOfUninitializedData <br/> | La dimensione della sezione di dati non inizializzata (BSS) o la somma di tutte le sezioni se sono presenti più sezioni BSS. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | AddressOfEntryPoint <br/>     | Indirizzo del punto di ingresso relativo alla base dell'immagine quando il file eseguibile viene caricato in memoria. Per le immagini del programma, questo è l'indirizzo iniziale. Per i driver di dispositivo, questo è l'indirizzo della funzione di inizializzazione. Un punto di ingresso è facoltativo per le dll. Quando non è presente alcun punto di ingresso, questo campo deve essere zero. <br/> |
| 20 <br/> | 4 <br/> | BaseOfCode <br/>              | Indirizzo relativo alla base dell'immagine della sezione iniziale del codice quando viene caricato in memoria. <br/>                                                                                                                                                                                                                    |

PE32 contiene questo campo aggiuntivo, che è assente in PE32 +, che segue BaseOfCode.

| Offset         | Dimensione          | Campo                  | Descrizione                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | BaseOfData <br/> | Indirizzo relativo alla base dell'immagine della sezione di inizio dei dati quando viene caricato in memoria. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Intestazione facoltativa Windows-Specific campi (solo immagine)

I 21 campi successivi sono un'estensione del formato di intestazione facoltativo COFF. Contengono informazioni aggiuntive richieste dal linker e dal caricatore di Windows.

| Offset (PE32/PE32 +) | Dimensioni (PE32/PE32 +) | Campo                                   | Descrizione                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | ImageBase sul <br/>                   | Indirizzo preferito del primo byte di immagine quando viene caricato in memoria. deve essere un multiplo di 64 K. Il valore predefinito per le dll è 0x10000000. Il valore predefinito per Windows CE exe è 0x00010000. Il valore predefinito per Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 e Windows me è 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | Allineamento (in byte) delle sezioni quando vengono caricate in memoria. Deve essere maggiore o uguale a FileAlignment. Il valore predefinito è la dimensione della pagina per l'architettura. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | Fattore di allineamento (in byte) usato per allineare i dati non elaborati delle sezioni nel file di immagine. Il valore deve essere una potenza di 2 compresa tra 512 e 64 K, inclusi. Il valore predefinito è 512. Se il allineamento sezione è inferiore alle dimensioni di pagina dell'architettura, FileAlignment deve corrispondere a allineamento sezione. <br/> |
| 40/40 <br/>    | 2 <br/>      | MajorOperatingSystemVersion <br/> | Numero di versione principale del sistema operativo richiesto. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | MinorOperatingSystemVersion <br/> | Numero di versione secondaria del sistema operativo richiesto. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | MajorImageVersion <br/>           | Numero di versione principale dell'immagine. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | MinorImageVersion <br/>           | Numero di versione secondaria dell'immagine. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | MajorSubsystemVersion <br/>       | Numero di versione principale del sottosistema. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | MinorSubsystemVersion <br/>       | Numero di versione secondaria del sottosistema. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Riservato, deve essere zero. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | SizeOfImage <br/>                 | Dimensioni (in byte) dell'immagine, incluse tutte le intestazioni, quando l'immagine viene caricata in memoria. Deve essere un multiplo di allineamento sezione. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | SizeOfHeaders <br/>               | Dimensioni combinate di uno stub MS-DOS, un'intestazione PE e intestazioni di sezione arrotondate per eccesso a un multiplo di FileAlignment. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | CheckSum <br/>                    | Checksum del file di immagine. L'algoritmo per il calcolo del checksum viene incorporato in IMAGHELP.DLL. Di seguito viene verificata la convalida in fase di caricamento: tutti i driver, qualsiasi DLL caricata in fase di avvio e qualsiasi DLL caricata in un processo di Windows critico. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsystem <br/>                   | Sottosistema necessario per eseguire l'immagine. Per ulteriori informazioni, vedere [sottosistema Windows](#windows-subsystem). <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Per ulteriori informazioni, vedere [caratteristiche dll](#dll-characteristics) più avanti in questa specifica. <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | Dimensioni dello stack da riservare. Viene eseguito il commit solo di SizeOfStackCommit; il resto viene reso disponibile una pagina alla volta fino a quando non viene raggiunta la dimensione della riserva. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | SizeOfStackCommit <br/>           | Dimensioni dello stack di cui eseguire il commit. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | SizeOfHeapReserve <br/>           | Dimensioni dello spazio dell'heap locale da riservare. Viene eseguito il commit solo di SizeOfHeapCommit; il resto viene reso disponibile una pagina alla volta fino a quando non viene raggiunta la dimensione della riserva. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | SizeOfHeapCommit <br/>            | Dimensioni dello spazio dell'heap locale di cui eseguire il commit. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | LoaderFlags <br/>                 | Riservato, deve essere zero. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | NumberOfRvaAndSizes <br/>         | Numero di voci della directory di dati nella parte restante dell'intestazione facoltativa. Ognuna descrive una posizione e una dimensione. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Sottosistema Windows

I valori seguenti definiti per il campo del sottosistema dell'intestazione facoltativa determinano il sottosistema Windows necessario per eseguire l'immagine.

| Costante                                                  | Valore          | Descrizione                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| \_sottosistema immagine \_ sconosciuto <br/>                     | 0 <br/>  | Sottosistema sconosciuto <br/>                                 |
| IMMAGINE del \_ sottosistema \_ nativo <br/>                      | 1 <br/>  | Driver di dispositivo e processi Windows nativi <br/>          |
| \_GUI Windows sottosistema immagine \_ \_ <br/>                | 2 <br/>  | Sottosistema interfaccia utente grafica (GUI) di Windows <br/> |
| \_Windows sottosistema \_ immagine \_ <br/>                | 3 <br/>  | Sottosistema di caratteri Windows <br/>                      |
| \_Sottosistema immagine \_ OS2 \_ <br/>                    | 5 <br/>  | Sottosistema operativo/2 caratteri <br/>                         |
| sottosistema di immagini \_ \_ POSIX \_ <br/>                  | 7 <br/>  | Sottosistema di caratteri POSIX <br/>                        |
| \_finestre native del sottosistema immagini \_ \_ <br/>             | 8 <br/>  | Driver Win9x nativo <br/>                                  |
| IMMAGINE del \_ sottosistema immagini-GUI di \_ Windows \_ CE \_ <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| \_applicazione EFI del sottosistema immagine \_ \_ <br/>            | 10 <br/> | Applicazione Extensible Firmware Interface (EFI) <br/>   |
| \_driver del \_ \_ servizio di avvio \_ EFI \_ del sottosistema immagine <br/> | 11 <br/> | Un driver EFI con servizi di avvio <br/>                     |
| \_ \_ driver di runtime EFI del sottosistema di immagini \_ \_ <br/>       | 12 <br/> | Un driver EFI con servizi di runtime <br/>                 |
| \_ROM EFI del sottosistema immagine \_ \_ <br/>                    | 13 <br/> | Un'immagine EFI ROM <br/>                                     |
| \_Xbox sottosistema \_ immagine <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| applicazione di avvio di Windows per il \_ sottosistema immagine \_ \_ \_ <br/>  | 16 <br/> | Applicazione di avvio di Windows. <br/>                            |

##### <a name="dll-characteristics"></a>Caratteristiche DLL

I valori seguenti vengono definiti per il campo DllCharacteristics dell'intestazione facoltativa.

| Costante                                                             | Valore              | Descrizione                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Riservato, deve essere zero. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Riservato, deve essere zero. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Riservato, deve essere zero. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Riservato, deve essere zero. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ High \_ entropia \_ va <br/>             | 0x0020 <br/> | L'immagine può gestire uno spazio degli indirizzi virtuali a 64 bit a entropia elevata. <br/>                               |
| \_DLLCHARACTERISTICS immagine\_ <br/> \_base dinamica <br/>    | 0x0040 <br/> | La DLL può essere rilocata in fase di caricamento. <br/>                                                          |
| \_DLLCHARACTERISTICS immagine\_ <br/> FORZA \_ integrità <br/> | 0x0080 <br/> | Vengono applicati i controlli di integrità del codice. <br/>                                                         |
| \_DLLCHARACTERISTICS immagine\_ <br/> \_compatibilità NX <br/>       | 0x0100 <br/> | Image è compatibile con NX. <br/>                                                                     |
| \_DLLCHARACTERISTICS immagine \_ senza \_ isolamento <br/>                | 0x0200 <br/> | L'isolamento è compatibile, ma non isolare l'immagine. <br/>                                              |
| \_DLLCHARACTERISTICS immagine \_ senza \_ SEH <br/>                      | 0x0400 <br/> | Non usa la gestione delle eccezioni strutturate (SE). In questa immagine non può essere chiamato alcun gestore SE. <br/> |
| \_DLLCHARACTERISTICS immagine \_ senza \_ binding <br/>                     | 0x0800 <br/> | Non associare l'immagine. <br/>                                                                      |
| IMAGE \_ DLLCHARACTERISTICS \_ appcontainer <br/>                  | 0x1000 <br/> | L'immagine deve essere eseguita in un AppContainer. <br/>                                                      |
| \_ \_ driver WDM Image \_ DLLCHARACTERISTICS <br/>                  | 0x2000 <br/> | Driver WDM. <br/>                                                                               |
| IMAGE \_ DLLCHARACTERISTICS \_ Guard \_ CF <br/>                     | 0x4000 <br/> | Image supporta la protezione del flusso di controllo. <br/>                                                          |
| IMAGE \_ DLLCHARACTERISTICS \_ Terminal \_ server \_ Aware <br/>      | 0x8000 <br/> | Terminal Server in grado di riconoscere. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Directory di dati intestazione facoltativa (solo immagine)

Ogni directory dati fornisce l'indirizzo e le dimensioni di una tabella o di una stringa utilizzata da Windows. Queste voci di directory dati vengono caricate in memoria in modo che possano essere utilizzate dal sistema in fase di esecuzione. Una directory di dati è un campo a 8 byte con la dichiarazione seguente:

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

Il primo campo, VirtualAddress, è in realtà l'RVA della tabella. RVA è l'indirizzo della tabella relativa all'indirizzo di base dell'immagine quando viene caricata la tabella. Il secondo campo restituisce le dimensioni in byte. Nella tabella seguente sono elencate le directory dei dati, che costituiscono l'ultima parte dell'intestazione facoltativa.

Si noti che il numero di directory non è fisso. Prima di cercare una directory specifica, controllare il campo NumberOfRvaAndSizes nell'intestazione facoltativa.

Inoltre, non presupporre che i RVA in questa tabella puntino all'inizio di una sezione o che le sezioni che contengono tabelle specifiche abbiano nomi specifici.

| Offset (PE/PE32 +)   | Dimensione          | Campo                               | Descrizione                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Esporta tabella <br/>            | Indirizzo e dimensioni della tabella di esportazione. Per ulteriori informazioni, vedere la [sezione. edata (solo immagine)](#the-edata-section-image-only). <br/>                                                |
| 104/120 <br/> | 8 <br/> | Importa tabella <br/>            | Indirizzo della tabella di importazione e dimensioni. Per ulteriori informazioni, vedere [la sezione. idata](#the-idata-section).<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Tabella delle risorse <br/>          | Indirizzo e dimensioni della tabella delle risorse. Per ulteriori informazioni, vedere [la sezione. rsrc](#the-rsrc-section).<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Tabella delle eccezioni <br/>         | Indirizzo e dimensioni della tabella delle eccezioni. Per ulteriori informazioni, vedere [la sezione. pData](#the-pdata-section). <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Tabella certificati <br/>       | Indirizzo e dimensioni della tabella del certificato dell'attributo. Per ulteriori informazioni, vedere [la tabella certificate Attribute (solo immagine)](#the-attribute-certificate-table-image-only). <br/> |
| 136/152 <br/> | 8 <br/> | Tabella di rilocazione di base <br/>   | Indirizzo e dimensioni della tabella di rilocazione di base. Per ulteriori informazioni, vedere [la sezione. reloc (solo immagine)](#the-reloc-section-image-only).<br/>                                   |
| 144/160 <br/> | 8 <br/> | Debug <br/>                   | Indirizzo e dimensioni iniziali dei dati di debug. Per ulteriori informazioni, vedere [la sezione. debug](#the-debug-section).<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Architettura <br/>            | Riservato, deve essere 0 <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | PTR globale <br/>              | RVA del valore da archiviare nel registro del puntatore globale. Il membro size della struttura deve essere impostato su zero. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | Tabella TLS <br/>               | Indirizzo e dimensioni della tabella di archiviazione locale di thread (TLS). Per ulteriori informazioni, [la sezione. TLS](#the-tls-section).<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Caricare la tabella di configurazione <br/>       | Indirizzo e dimensioni della tabella di configurazione di caricamento. Per ulteriori informazioni, [la struttura di configurazione Load (solo immagine)](#the-load-configuration-structure-image-only).<br/>       |
| 184/200 <br/> | 8 <br/> | Importazione associata <br/>            | Indirizzo e dimensioni della tabella di importazione associata. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | IAT <br/>                     | Indirizzo e dimensioni della tabella di indirizzi di importazione. Per altre informazioni, vedere [importare la tabella degli indirizzi](#import-address-table).<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Descrittore di importazione ritardata <br/> | Indirizzo e dimensioni del descrittore dell'importazione ritardata. Per altre informazioni, vedere [tabelle di importazione a caricamento ritardato (solo immagine)](#delay-load-import-tables-image-only).<br/>                    |
| 208/224 <br/> | 8 <br/> | Intestazione runtime CLR <br/>      | Indirizzo e dimensioni dell'intestazione del runtime CLR. Per ulteriori informazioni, vedere [la sezione. cormeta (solo oggetto)](#the-cormeta-section-object-only).<br/>                                |
| 216/232 <br/> | 8 <br/> | Riservato, deve essere zero <br/>  |                                                                                                                                                                                      |

La voce della tabella dei certificati punta a una tabella di certificati di attributo. Questi certificati non vengono caricati in memoria come parte dell'immagine. Il primo campo di questa voce, che è in genere un RVA, è invece un puntatore del file.

## <a name="section-table-section-headers"></a>Tabella delle sezioni (intestazioni di sezione)

- [Flag di sezione](#section-flags)
- [Sezioni raggruppate (solo oggetto)](#grouped-sections-object-only)

Ogni riga della tabella della sezione è, in effetti, un'intestazione di sezione. Questa tabella segue immediatamente l'intestazione facoltativa, se disponibile. Questo posizionamento è necessario perché l'intestazione del file non contiene un puntatore diretto alla tabella della sezione. Il percorso della tabella della sezione viene invece determinato calcolando la posizione del primo byte dopo le intestazioni. Assicurarsi di usare le dimensioni dell'intestazione facoltativa come specificato nell'intestazione del file.

Il numero di voci nella tabella della sezione viene fornito dal campo NumberOfSections nell'intestazione del file. Le voci nella tabella della sezione sono numerate a partire da uno (1). Le voci della sezione relativa alla memoria del codice e dei dati sono nell'ordine scelto dal linker.

In un file di immagine, il VAs per le sezioni deve essere assegnato dal linker in modo che sia in ordine crescente e adiacente e che sia un multiplo del valore allineamento sezione nell'intestazione facoltativa.

Ogni intestazione di sezione (voce della tabella della sezione) ha il formato seguente, per un totale di 40 byte per voce.



| Offset         | Dimensione          | Campo                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nome <br/>                 | Stringa con codifica UTF-8 con riempimento null a 8 byte. Se la stringa è esattamente di 8 caratteri, non è presente alcun carattere di terminazione null. Per i nomi più lunghi, questo campo contiene una barra (/) seguita da una rappresentazione ASCII di un numero decimale che è un offset nella tabella di stringhe. Le immagini eseguibili non utilizzano una tabella di stringhe e non supportano i nomi di sezione di lunghezza superiore a 8 caratteri. I nomi lunghi nei file oggetto vengono troncati se vengono emessi in un file eseguibile. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | Dimensione totale della sezione quando viene caricata in memoria. Se questo valore è maggiore di SizeOfRawData, la sezione viene riempita con zero. Questo campo è valido solo per le immagini eseguibili e deve essere impostato su zero per i file oggetto. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | Per le immagini eseguibili, l'indirizzo del primo byte della sezione relativa alla base dell'immagine quando la sezione viene caricata in memoria. Per i file oggetto, questo campo è l'indirizzo del primo byte prima dell'applicazione della rilocazione; per semplicità, i compilatori devono impostare questo valore su zero. In caso contrario, si tratta di un valore arbitrario che viene sottratto dagli offset durante la rilocazione. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | SizeOfRawData <br/>        | Dimensioni della sezione (per i file oggetto) o dimensione dei dati inizializzati su disco (per i file di immagine). Per le immagini eseguibili, deve essere un multiplo di FileAlignment dall'intestazione facoltativa. Se è minore di VirtualSize, il resto della sezione viene riempito con zero. Poiché il campo SizeOfRawData è arrotondato ma il campo VirtualSize non è, è possibile che SizeOfRawData sia maggiore di VirtualSize. Quando una sezione contiene solo dati non inizializzati, questo campo deve essere zero. <br/> |
| 20 <br/> | 4 <br/> | PointerToRawData <br/>     | Puntatore di file alla prima pagina della sezione all'interno del file COFF. Per le immagini eseguibili, deve essere un multiplo di FileAlignment dall'intestazione facoltativa. Per i file oggetto, il valore deve essere allineato a un limite di 4 byte per ottenere prestazioni ottimali. Quando una sezione contiene solo dati non inizializzati, questo campo deve essere zero. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | PointerToRelocations <br/> | Puntatore di file all'inizio delle voci di rilocazione per la sezione. Viene impostato su zero per le immagini eseguibili o se non sono presenti rilocazioni. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | PointerToLinenumbers <br/> | Puntatore di file all'inizio delle voci del numero di riga per la sezione. Questa impostazione è impostata su zero se non sono presenti numeri di riga COFF. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | NumberOfRelocations <br/>  | Numero di voci di rilocazione per la sezione. Questa impostazione è impostata su zero per le immagini eseguibili. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | NumberOfLinenumbers <br/>  | Numero di voci di numeri di riga per la sezione. Questo valore deve essere zero per un'immagine perché le informazioni di debug COFF sono deprecate. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Caratteristiche <br/>      | Flag che descrivono le caratteristiche della sezione. Per altre informazioni, vedere [flag di sezione](#section-flags).<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Flag di sezione

I flag di sezione nel campo caratteristiche dell'intestazione della sezione indicano le caratteristiche della sezione.



| Flag                                              | valore                  | Descrizione                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| \_tipo di SCN immagine \_ \_ senza \_ riempimento <br/>             | 0x00000008 <br/> | La sezione non deve essere riempita al limite successivo. Questo flag è obsoleto e viene sostituito da IMAGE \_ SCN \_ align \_ 1BYTES. Questa operazione è valida solo per i file oggetto. <br/> |
|                                                   | 0x00000010 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ ( \_ codice CNT) <br/>                 | 0x00000020 <br/> | La sezione contiene codice eseguibile. <br/>                                                                                                                           |
| \_ \_ \_ dati inizializzati SCN CNT immagine \_ <br/>    | 0x00000040 <br/> | La sezione contiene dati inizializzati. <br/>                                                                                                                          |
| \_dati non \_ \_ inizializzati in SCN dell'immagine \_ <br/> | 0x00000080 <br/> | La sezione contiene dati non inizializzati. <br/>                                                                                                                        |
| IMAGE \_ SCN \_ lnk \_ other <br/>                | 0x00000100 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ lnk \_ info <br/>                 | 0x00000200 <br/> | La sezione contiene commenti o altre informazioni. Questo tipo è presente nella sezione. drectve. Questa operazione è valida solo per i file oggetto. <br/>                                    |
|                                                   | 0x00000400 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ lnk \_ Remove <br/>               | 0x00000800 <br/> | La sezione non diventerà parte dell'immagine. Questa operazione è valida solo per i file oggetto. <br/>                                                                             |
| IMAGE \_ SCN \_ lnk \_ COMDAT <br/>               | 0x00001000 <br/> | La sezione contiene dati COMDAT. Per ulteriori informazioni, vedere [COMDAT Sections (solo oggetto)](#comdat-sections-object-only). Questa operazione è valida solo per i file oggetto. <br/> |
| IMAGE \_ SCN \_ GPREL <br/>                     | 0x00008000 <br/> | La sezione contiene i dati a cui si fa riferimento tramite il puntatore globale (GP). <br/>                                                                                           |
| IMAGE \_ SCN \_ mem \_ PURGEABLE <br/>            | 0x00020000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMMAGINE di bit della memoria di \_ SCN \_ \_ <br/>                | 0x00020000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| memoria di \_ SCN immagine \_ \_ bloccata <br/>               | 0x00040000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| \_ \_ precaricamento MEM di Image SCN \_ <br/>              | 0x00080000 <br/> | Riservato per utilizzi futuri. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ align \_ 1BYTES <br/>             | 0x00100000 <br/> | Allineare i dati in un limite di 1 byte. Valido solo per i file oggetto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 2BYTES <br/>             | 0x00200000 <br/> | Allinea i dati in un limite di 2 byte. Valido solo per i file oggetto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 4BYTES <br/>             | 0x00300000 <br/> | Allinea i dati in un limite di 4 byte. Valido solo per i file oggetto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ align \_ 8BYTES <br/>             | 0x00400000 <br/> | Allinea i dati in un limite di 8 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 16BYTES <br/>            | 0x00500000 <br/> | Allinea i dati in un limite di 16 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 32BYTES <br/>            | 0x00600000 <br/> | Allinea i dati in un limite di 32 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 64BYTES <br/>            | 0x00700000 <br/> | Allinea i dati in un limite di 64 byte. Valido solo per i file oggetto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ align \_ 128BYTES <br/>           | 0x00800000 <br/> | Allinea i dati in un limite di 128 byte. Valido solo per i file oggetto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 256 byte <br/>           | 0x00900000 <br/> | Allinea i dati in un limite di 256 byte. Valido solo per i file oggetto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 512BYTES <br/>           | 0x00A00000 <br/> | Allinea i dati in un limite di 512 byte. Valido solo per i file oggetto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ align \_ 1024BYTES <br/>          | 0x00B00000 <br/> | Allinea i dati in un limite di 1024 byte. Valido solo per i file oggetto. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 2048BYTES <br/>          | 0x00C00000 <br/> | Allinea i dati in un limite di 2048 byte. Valido solo per i file oggetto. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 4096BYTES <br/>          | 0x00D00000 <br/> | Allinea i dati in un limite di 4096 byte. Valido solo per i file oggetto. <br/>                                                                                                |
| IMAGE \_ SCN \_ align \_ 8192BYTES <br/>          | 0x00E00000 <br/> | Allinea i dati in un limite di 8192 byte. Valido solo per i file oggetto. <br/>                                                                                               |
| IMAGE \_ SCN \_ lnk \_ NRELOC \_ OVFL <br/>         | 0x01000000 <br/> | La sezione contiene rilocazioni estese. <br/>                                                                                                                      |
| IMAGE \_ SCN \_ mem \_ scartabile <br/>          | 0x02000000 <br/> | La sezione può essere eliminata in base alle esigenze. <br/>                                                                                                                         |
| memoria \_ SCN dell'immagine \_ \_ non \_ memorizzata nella cache <br/>          | 0x04000000 <br/> | La sezione non può essere memorizzata nella cache. <br/>                                                                                                                                   |
| il paging della MEM dell'immagine non è stato \_ \_ \_ \_ sottopaginato <br/>           | 0x08000000 <br/> | La sezione non è paginabile. <br/>                                                                                                                                    |
| memoria di \_ SCN immagine \_ \_ condivisa <br/>               | 0x10000000 <br/> | La sezione può essere condivisa in memoria. <br/>                                                                                                                            |
| esecuzione della memoria di \_ SCN immagine \_ \_ <br/>              | 0x20000000 <br/> | La sezione può essere eseguita come codice. <br/>                                                                                                                            |
| \_ \_ lettura mem di Image SCN \_ <br/>                 | 0x40000000 <br/> | È possibile leggere la sezione. <br/>                                                                                                                                        |
| scrittura memoria di \_ SCN immagine \_ \_ <br/>                | 0x80000000 <br/> | È possibile scrivere nella sezione. <br/>                                                                                                                                  |



 

IMAGE \_ SCN \_ lnk \_ NRELOC \_ OVFL indica che il numero di rilocazioni per la sezione supera i 16 bit riservati nell'intestazione della sezione. Se il bit è impostato e il campo NumberOfRelocations nell'intestazione della sezione è 0xFFFF, il numero effettivo di rilocazioni viene archiviato nel campo VirtualAddress a 32 bit della prima rilocazione. Si verifica un errore se si \_ imposta Image SCN \_ lnk \_ NRELOC \_ OVFL e sono presenti meno di 0xFFFF rilocazioni nella sezione.

### <a name="grouped-sections-object-only"></a>Sezioni raggruppate (solo oggetto)

"$"? il carattere (simbolo del dollaro) ha un'interpretazione speciale nei nomi di sezione nei file oggetto.

Quando si determina la sezione dell'immagine che conterrà il contenuto di una sezione oggetto, il linker Elimina "$"? e tutti i caratteri che lo seguono. Quindi, una sezione di oggetto denominata. il **testo $ X** contribuisce effettivamente alla sezione **. Text** nell'immagine.

Tuttavia, i caratteri che seguono "$"? determinare l'ordine dei contributi alla sezione Image. Tutti i contributi con lo stesso nome della sezione di oggetti vengono allocati in modo contiguo nell'immagine e i blocchi di contributi sono ordinati in base al nome lessicale per sezione oggetto. Pertanto, tutti i file oggetto con il nome della sezione **. il testo $ X** termina insieme, dopo il **testo $ W** contributi e prima del **. testo $ Y** contributi.

Il nome della sezione in un file di immagine non contiene mai una "$"? .

## <a name="other-contents-of-the-file"></a>Altro contenuto del file

- [Dati della sezione](#section-data)
- [Rilocazioni COFF (solo oggetto)](#coff-relocations-object-only)
  - [Indicatori di tipo](#type-indicators)
- [Numeri di riga COFF (deprecato)](#coff-line-numbers-deprecated)
- [Tabella di simboli COFF](#coff-symbol-table)
  - [Rappresentazione del nome del simbolo](#symbol-name-representation)
  - [Valori numero di sezione](#section-number-values)
  - [Rappresentazione del tipo](#type-representation)
  - [Classe di archiviazione](#storage-class)
- [Record di simboli ausiliari](#auxiliary-symbol-records)
  - [Formato ausiliario 1: definizioni di funzione](#auxiliary-format-1-function-definitions)
  - [Formato ausiliario 2: simboli. BF e. EF](#auxiliary-format-2-bf-and-ef-symbols)
  - [Formato ausiliario 3: External vulnerabili](#auxiliary-format-3-weak-externals)
  - [Formato ausiliario 4: file](#auxiliary-format-4-files)
  - [Formato ausiliario 5: definizioni di sezione](#auxiliary-format-5-section-definitions)
  - [Sezioni COMDAT (solo oggetto)](#comdat-sections-object-only)
  - [Definizione del token CLR (solo oggetto)](#clr-token-definition-object-only)
- [Tabella di stringhe COFF](#coff-string-table)
- [Tabella dei certificati degli attributi (solo immagine)](#the-attribute-certificate-table-image-only)
  - [Dati del certificato](#certificate-data)
- [Tabelle di importazione a caricamento ritardato (solo immagine)](#delay-load-import-tables-image-only)
  - [Tabella di Delay-Load directory](#the-delay-load-directory-table)
  - [Attributes (Attributi)](#attributes)
  - [Nome](#name)
  - [Handle del modulo](#module-handle)
  - [Tabella degli indirizzi di importazione ritardata](#delay-import-address-table)
  - [Tabella nome importazione ritardata](#delay-import-name-table)
  - [Tabella degli indirizzi di importazione con associazione ritardata e timestamp](#delay-bound-import-address-table-and-time-stamp)
  - [Tabella degli indirizzi di importazione dello scaricamento ritardato](#delay-unload-import-address-table)

Le strutture di dati descritte finora, fino a includere l'intestazione facoltativa, si trovano tutte in corrispondenza di un offset fisso dall'inizio del file (o dall'intestazione PE se il file è un'immagine che contiene uno stub MS-DOS).

Il resto di un oggetto COFF o di un file di immagine contiene blocchi di dati che non sono necessariamente in corrispondenza di un offset di file specifico. Al contrario, i percorsi vengono definiti dai puntatori nell'intestazione facoltativa o in un'intestazione di sezione.

Un'eccezione è destinata alle immagini con un valore allineamento sezione inferiore alle dimensioni di pagina dell'architettura (4 K per Intel x86 e per MIPS e 8 K per Itanium). Per una descrizione di allineamento sezione, vedere [intestazione facoltativa (solo immagine)](#optional-header-image-only). In questo caso, sono presenti vincoli sull'offset del file dei dati della sezione, come descritto nella sezione 5,1, "dati della sezione". Un'altra eccezione è che il certificato dell'attributo e le informazioni di debug devono essere posizionati alla fine di un file di immagine, con la tabella dei certificati dell'attributo immediatamente prima della sezione debug, perché il caricatore non esegue il mapping di questi in memoria. Tuttavia, la regola sul certificato dell'attributo e le informazioni di debug non si applicano ai file oggetto.

### <a name="section-data"></a>Dati della sezione

I dati inizializzati per una sezione sono costituiti da blocchi di byte semplici. Tuttavia, per le sezioni che contengono tutti zeri, non è necessario includere i dati della sezione.

I dati per ogni sezione si trovano in corrispondenza dell'offset del file specificato dal campo PointerToRawData nell'intestazione della sezione. Le dimensioni dei dati nel file sono indicate dal campo SizeOfRawData. Se SizeOfRawData è minore di VirtualSize, il resto viene riempito con zeri.

In un file di immagine, i dati della sezione devono essere allineati su un limite come specificato dal campo FileAlignment nell'intestazione facoltativa. I dati della sezione devono essere visualizzati in ordine dei valori RVA per le sezioni corrispondenti (come le singole intestazioni di sezione nella tabella della sezione).

Se il valore allineamento sezione nell'intestazione facoltativa è inferiore alle dimensioni della pagina dell'architettura, esistono restrizioni aggiuntive nei file di immagine. Per tali file, il percorso dei dati della sezione nel file deve corrispondere alla relativa posizione in memoria quando viene caricata l'immagine, in modo che l'offset fisico per i dati della sezione sia uguale a RVA.

### <a name="coff-relocations-object-only"></a>Rilocazioni COFF (solo oggetto)

I file oggetto contengono rilocazioni COFF, che specificano il modo in cui i dati della sezione devono essere modificati quando vengono inseriti nel file di immagine e successivamente caricati in memoria.

I file di immagine non contengono rilocazioni COFF, perché a tutti i simboli a cui viene fatto riferimento sono già stati assegnati indirizzi in uno spazio degli indirizzi flat. Un'immagine contiene le informazioni di rilocazione sotto forma di rilocazioni di base nella sezione. reloc (a meno che l'immagine non abbia il file di immagine rilocazioni di cui è stato \_ \_ rimosso l' \_ attributo). Per ulteriori informazioni, vedere [la sezione. reloc (solo immagine)](#the-reloc-section-image-only).

Per ogni sezione in un file oggetto, una matrice di record a lunghezza fissa include le rilocazioni COFF della sezione. La posizione e la lunghezza della matrice sono specificate nell'intestazione della sezione. Ogni elemento della matrice ha il formato seguente.



| Offset        | Dimensione          | Campo                        | Descrizione                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Indirizzo dell'elemento a cui viene applicata la rilocazione. Si tratta dell'offset dall'inizio della sezione, più il valore del campo RVA/offset della sezione. Vedere la [sezione tabella (intestazioni di sezione)](#section-table-section-headers). Se, ad esempio, il primo byte della sezione ha un indirizzo di 0x10, il terzo byte avrà un indirizzo di 0x12. <br/> |
| 4 <br/> | 4 <br/> | SymbolTableIndex <br/> | Indice in base zero nella tabella dei simboli. Questo simbolo fornisce l'indirizzo da utilizzare per la rilocazione. Se il simbolo specificato ha una classe di archiviazione della sezione, l'indirizzo del simbolo è l'indirizzo con la prima sezione con lo stesso nome. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | Tipo <br/>             | Valore che indica il tipo di rilocazione da eseguire. I tipi di rilocazione validi dipendono dal tipo di computer. Vedere [indicatori di tipo](#type-indicators). <br/>                                                                                                                                                                                     |



 

Se il simbolo a cui fa riferimento il campo SymbolTableIndex ha la \_ sezione classe di archiviazione sym \_ Class \_ , l'indirizzo del simbolo è l'inizio della sezione. La sezione si trova in genere nello stesso file, tranne quando il file oggetto fa parte di un archivio (libreria). In tal caso, è possibile trovare la sezione in qualsiasi altro file oggetto nell'archivio con lo stesso nome di membro di archivio del file oggetto corrente. La relazione con il nome del membro Archive viene utilizzata nel collegamento delle tabelle di importazione, ovvero la sezione. idata.

#### <a name="type-indicators"></a>Indicatori di tipo

Il campo tipo del record di rilocazione indica il tipo di rilocazione da eseguire. Per ogni tipo di computer vengono definiti tipi di rilocazione diversi.

##### <a name="x64-processors"></a>Processori x64

Per i processori x64 e compatibili sono definiti i seguenti indicatori di tipo di rilocazione.



| Costante                                | Valore              | Descrizione                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMMAGINE \_ rel \_ amd64 \_ Absolute <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                        |
| IMAGE \_ rel \_ amd64 \_ ADDR64 <br/>   | 0x0001 <br/> | Il VA a 64 bit della destinazione di rilocazione. <br/>                                                                                                           |
| IMAGE \_ rel \_ amd64 \_ ADDR32 <br/>   | 0x0002 <br/> | Il VA a 32 bit della destinazione di rilocazione. <br/>                                                                                                           |
| IMAGE \_ rel \_ amd64 \_ ADDR32NB <br/> | 0x0003 <br/> | Indirizzo a 32 bit senza un RVA (Image base). <br/>                                                                                                   |
| IMAGE \_ rel \_ amd64 \_ REL32 <br/>    | 0x0004 <br/> | Indirizzo relativo a 32 bit dal byte che segue la rilocazione. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | Indirizzo a 32 bit relativo alla distanza di byte 1 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | Indirizzo a 32 bit relativo alla distanza di byte 2 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | Indirizzo a 32 bit relativo alla distanza di byte 3 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | Indirizzo a 32 bit relativo alla distanza di byte 4 dalla rilocazione. <br/>                                                                               |
| IMAGE \_ rel \_ amd64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | Indirizzo a 32 bit relativo alla distanza di byte 5 dalla rilocazione. <br/>                                                                               |
| \_Sezione Image rel \_ amd64 \_ <br/>  | 0x000A <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                  |
| IMAGE \_ rel \_ amd64 \_ SECREL <br/>   | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/> |
| IMAGE \_ rel \_ amd64 \_ SECREL7 <br/>  | 0x000C <br/> | Offset senza segno a 7 bit dalla base della sezione che contiene la destinazione. <br/>                                                                    |
| IMMAGINE \_ del \_ token amd64 rel \_ <br/>    | 0x000D <br/> | Token CLR. <br/>                                                                                                                                       |
| IMAGE \_ rel \_ amd64 \_ SREL32 <br/>   | 0x000E <br/> | Valore dipendente dall'intervallo con segno a 32 bit emesso nell'oggetto. <br/>                                                                                     |
| IMAGE \_ rel \_ amd64 \_ Pair <br/>     | 0x000F <br/> | Coppia che deve seguire immediatamente ogni valore dipendente dall'intervallo. <br/>                                                                                   |
| IMAGE \_ rel \_ amd64 \_ SSPAN32 <br/>  | 0x0010 <br/> | Valore dipendente dall'intervallo con segno a 32 bit applicato in fase di collegamento. <br/>                                                                                |



 

##### <a name="arm-processors"></a>Processori ARM

Per i processori ARM sono definiti gli indicatori di tipo rilocazione seguenti.



| Costante                                | Valore              | Descrizione                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ ARM \_ Absolute <br/>   | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ ARM \_ ADDR32 <br/>     | 0x0001 <br/> | Il VA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ rel \_ ARM \_ ADDR32NB <br/>   | 0x0002 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ rel \_ ARM \_ BRANCH24 <br/>   | 0x0003 <br/> | Spostamento relativo a 24 bit nella destinazione. <br/>                                                                                                                                                                                                            |
| IMAGE \_ rel \_ ARM \_ BRANCH11 <br/>   | 0x0004 <br/> | Riferimento a una chiamata subroutine. Il riferimento è costituito da istruzioni a 2 16 bit con offset a 11 bit. <br/>                                                                                                                                                 |
| IMAGE \_ rel \_ ARM \_ REL32 <br/>      | 0x000A <br/> | Indirizzo relativo a 32 bit dal byte che segue la rilocazione. <br/>                                                                                                                                                                                        |
| \_sezione Image rel \_ ARM \_ <br/>    | 0x000E <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                                                                                                                           |
| IMAGE \_ rel \_ ARM \_ SECREL <br/>     | 0x000F <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                          |
| IMAGE \_ rel \_ ARM \_ MOV32 <br/>      | 0x0010 <br/> | Il VA a 32 bit della destinazione. Questa rilocazione viene applicata usando un'istruzione MOVW per i 16 bit bassi seguiti da un MOVT per i 16 bit alti. <br/>                                                                                                              |
| IMMAGINE \_ \_ MOV32 pollice \_ rel <br/>    | 0x0011 <br/> | Il VA a 32 bit della destinazione. Questa rilocazione viene applicata usando un'istruzione MOVW per i 16 bit bassi seguiti da un MOVT per i 16 bit alti. <br/>                                                                                                              |
| IMMAGINE \_ \_ BRANCH20 pollice \_ rel <br/> | 0x0012 <br/> | L'istruzione è fissata con lo spostamento relativo a 21 bit alla destinazione allineata a 2 byte. Il bit meno significativo dello spostamento è sempre zero e non viene archiviato. Questa rilocazione corrisponde a un'istruzione B condizionale Thumb-2 32-bit. <br/> |
| Non utilizzato <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| IMMAGINE \_ \_ BRANCH24 pollice \_ rel <br/> | 0x0014 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 2 byte. Il bit meno significativo dello spostamento è zero e non viene archiviato. Questa rilocazione corrisponde a un'istruzione Thumb-2 B. <br/>                            |
| IMMAGINE \_ \_ BLX23 pollice \_ rel <br/>    | 0x0015 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 4 byte. I 2 bit inferiori dello spostamento sono pari a zero e non vengono archiviati. <br/> Questa rilocazione corrisponde a un'istruzione BLX Thumb-2. <br/>                      |
| IMAGE \_ rel \_ ARM \_ Pair <br/>       | 0x0016 <br/> | La rilocazione è valida solo quando segue immediatamente un REFHI ARM \_ REFHI o Thumb \_ . Il SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>Processori ARM64

Per i processori ARM64 sono definiti gli indicatori di tipo rilocazione seguenti.



| Costante                                       | Valore              | Descrizione                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ arm64 \_ Absolute <br/>        | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                        |
| IMAGE \_ rel \_ arm64 \_ ADDR32 <br/>          | 0x0001 <br/> | Il VA a 32 bit della destinazione. <br/>                                                                                                                      |
| IMAGE \_ rel \_ arm64 \_ ADDR32NB <br/>        | 0x0002 <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                     |
| IMAGE \_ rel \_ arm64 \_ BRANCH26 <br/>        | 0x0003 <br/> | Spostamento relativo a 26 bit per la destinazione, per le istruzioni B e BL. <br/>                                                                        |
| IMAGE \_ rel \_ arm64 \_ PAGEBASE \_ REL21 <br/> | 0x0004 <br/> | La base della pagina della destinazione, per l'istruzione ADRP. <br/>                                                                                                |
| IMAGE \_ rel \_ arm64 \_ REL21 <br/>           | 0x0005 <br/> | Spostamento relativo a 12 bit nella destinazione, per l'istruzione ADR <br/>                                                                               |
| IMAGE \_ rel \_ arm64 \_ PAGEOFFSET \_ 12A <br/> | 0x0006 <br/> | Offset di pagina a 12 bit della destinazione, per le istruzioni ADD/aggiunge (immediate) con lo spostamento zero. <br/>                                                      |
| IMAGE \_ rel \_ arm64 \_ PAGEOFFSET \_ 12L <br/> | 0x0007 <br/> | Offset di pagina a 12 bit della destinazione, per l'istruzione LDR (indicizzato, unsigned immediate). <br/>                                                          |
| IMAGE \_ rel \_ arm64 \_ SECREL <br/>          | 0x0008 <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/> |
| IMAGE \_ rel \_ arm64 \_ SECREL \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 dell'offset della sezione della destinazione, per le istruzioni ADD/aggiunge (immediate) con lo spostamento zero. <br/>                                                  |
| IMAGE \_ rel \_ arm64 \_ SECREL \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 dell'offset della sezione della destinazione, per le istruzioni ADD/aggiunge (immediate) con lo spostamento zero. <br/>                                                 |
| IMAGE \_ rel \_ arm64 \_ SECREL \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 dell'offset della sezione della destinazione, per l'istruzione LDR (indicizzato, unsigned immediate). <br/>                                                      |
| IMMAGINE \_ del \_ token arm64 rel \_ <br/>           | 0x000C <br/> | Token CLR. <br/>                                                                                                                                        |
| \_Sezione Image rel \_ arm64 \_ <br/>         | 0x000D <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                  |
| IMAGE \_ rel \_ arm64 \_ ADDR64 <br/>          | 0x000E <br/> | Il VA a 64 bit della destinazione di rilocazione. <br/>                                                                                                           |
| IMAGE \_ rel \_ arm64 \_ BRANCH19 <br/>        | 0x000F <br/> | Offset a 19 bit per la destinazione di rilocazione, per l'istruzione B condizionale. <br/>                                                                        |
| IMAGE \_ rel \_ arm64 \_ BRANCH14 <br/>        | 0x0010 <br/> | Offset a 14 bit per la destinazione di rilocazione, per le istruzioni TBZ e TBNZ. <br/>                                                                        |
| IMAGE \_ rel \_ arm64 \_ REL32 <br/>           | 0x0011 <br/> | Indirizzo relativo a 32 bit dal byte che segue la rilocazione. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>Processori Hitachi SuperH

I seguenti indicatori di tipo di rilocazione sono definiti per i processori SH3 e SH4. Le rilocazioni specifiche di SH5 sono indicate come SHM (SH Media).



| Costante                                      | Valore              | Descrizione                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ SH3 \_ Absolute <br/>         | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                     |
| IMAGE \_ rel \_ SH3 \_ DIRECT16 <br/>         | 0x0001 <br/> | Riferimento alla posizione a 16 bit che contiene l'oggetto VA del simbolo di destinazione. <br/>                                                                                                                                  |
| IMAGE \_ rel \_ SH3 \_ DIRECT32 <br/>         | 0x0002 <br/> | VA a 32 bit del simbolo di destinazione. <br/>                                                                                                                                                                            |
| IMAGE \_ rel \_ SH3 \_ DIRECT8 <br/>          | 0x0003 <br/> | Riferimento alla posizione a 8 bit che contiene l'oggetto VA del simbolo di destinazione. <br/>                                                                                                                                   |
| IMAGE \_ rel \_ SH3 \_ DIRECT8 \_ Word <br/>    | 0x0004 <br/> | Riferimento all'istruzione a 8 bit che contiene l'effettivo a 16 bit del simbolo di destinazione. <br/>                                                                                                               |
| IMAGE \_ rel \_ SH3 \_ DIRECT8 \_ Long <br/>    | 0x0005 <br/> | Riferimento all'istruzione a 8 bit che contiene il valore di VA a 32 bit effettivo del simbolo di destinazione. <br/>                                                                                                               |
| IMAGE \_ rel \_ SH3 \_ DIRECT4 <br/>          | 0x0006 <br/> | Riferimento alla posizione a 8 bit i cui 4 bit inferiori contengono la VA del simbolo di destinazione. <br/>                                                                                                                        |
| IMAGE \_ rel \_ SH3 \_ DIRECT4 \_ Word <br/>    | 0x0007 <br/> | Riferimento all'istruzione a 8 bit i cui 4 bit inferiori contengono l'efficacia a 16 bit del simbolo di destinazione. <br/>                                                                                                    |
| IMAGE \_ rel \_ SH3 \_ DIRECT4 \_ Long <br/>    | 0x0008 <br/> | Riferimento all'istruzione a 8 bit i cui 4 bit inferiori contengono l'effettivo VA a 32 bit del simbolo di destinazione. <br/>                                                                                                    |
| IMAGE \_ rel \_ SH3 \_ PCREL8 \_ Word <br/>     | 0x0009 <br/> | Riferimento all'istruzione a 8 bit che contiene l'offset relativo effettivo a 16 bit del simbolo di destinazione. <br/>                                                                                                  |
| IMAGE \_ rel \_ SH3 \_ PCREL8 \_ Long <br/>     | 0x000A <br/> | Riferimento all'istruzione a 8 bit che contiene l'offset relativo effettivo a 32 bit del simbolo di destinazione. <br/>                                                                                                  |
| IMAGE \_ rel \_ SH3 \_ PCREL12 \_ Word <br/>    | 0x000B <br/> | Riferimento all'istruzione a 16 bit i cui 12 bit inferiori contengono l'offset relativo effettivo a 16 bit del simbolo di destinazione. <br/>                                                                                     |
| \_Sezione Image rel \_ SH3 \_ inizio \_ <br/> | 0x000C <br/> | Riferimento a una posizione a 32 bit che corrisponde al VA della sezione che contiene il simbolo di destinazione. <br/>                                                                                                                |
| \_Sezione Image rel \_ SH3 \_ sizeof \_ <br/>  | 0x000D <br/> | Riferimento alla posizione a 32 bit che corrisponde alla dimensione della sezione che contiene il simbolo di destinazione. <br/>                                                                                                            |
| \_Sezione Image rel \_ SH3 \_ <br/>          | 0x000E <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                                                                               |
| IMAGE \_ rel \_ SH3 \_ SECREL <br/>           | 0x000F <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                              |
| IMAGE \_ rel \_ SH3 \_ DIRECT32 \_ NB <br/>     | 0x0010 <br/> | RVA a 32 bit del simbolo di destinazione. <br/>                                                                                                                                                                           |
| IMAGE \_ rel \_ SH3 \_ GPREL4 \_ Long <br/>     | 0x0011 <br/> | Relativo al GP. <br/>                                                                                                                                                                                                   |
| IMMAGINE \_ del \_ token SH3 rel \_ <br/>            | 0x0012 <br/> | Token CLR. <br/>                                                                                                                                                                                                     |
| IMAGE \_ rel \_ SHM \_ PCRELPT <br/>          | 0x0013 <br/> | Offset dall'istruzione corrente in longwords. Se il bit NoMode non è impostato, inserire l'inverso del bit basso a bit 32 per selezionare PTA o PTB. <br/>                                                          |
| IMAGE \_ rel \_ SHM \_ REFLO <br/>            | 0x0014 <br/> | I 16 bit bassi dell'indirizzo a 32 bit. <br/>                                                                                                                                                                         |
| IMAGE \_ rel \_ SHM \_ REFHALF <br/>          | 0x0015 <br/> | 16 bit alti dell'indirizzo a 32 bit. <br/>                                                                                                                                                                        |
| IMAGE \_ rel \_ SHM \_ rello <br/>            | 0x0016 <br/> | I 16 bit bassi dell'indirizzo relativo. <br/>                                                                                                                                                                       |
| IMAGE \_ rel \_ SHM \_ RELHALF <br/>          | 0x0017 <br/> | 16 bit alti dell'indirizzo relativo. <br/>                                                                                                                                                                      |
| IMAGE \_ rel \_ SHM \_ Pair <br/>             | 0x0018 <br/> | La rilocazione è valida solo quando segue immediatamente una rilocazione REFHALF, RELHALF o RELLO. Il campo SymbolTableIndex della rilocazione contiene uno spostamento e non un indice nella tabella dei simboli. <br/> |
| IMAGE \_ rel \_ SHM \_ NoMode <br/>           | 0x8000 <br/> | La modalità di rilocazione ignora la sezione. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>Processori PowerPC IBM

I seguenti indicatori di tipo di rilocazione sono definiti per i processori PowerPC.



| Costante                              | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMMAGINE \_ rel \_ PPC \_ Absolute <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMMAGINE \_ rel \_ PPC \_ ADDR64 <br/>   | 0x0001 <br/> | Il VA a 64 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMMAGINE \_ rel \_ PPC \_ ADDR32 <br/>   | 0x0002 <br/> | Il VA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMMAGINE \_ rel \_ PPC \_ ADDR24 <br/>   | 0x0003 <br/> | I 24 bit bassi del VA della destinazione. Questa proprietà è valida solo quando il simbolo di destinazione è assoluto e può essere esteso con segno al valore originale. <br/>                                                                                                                                                                                                                          |
| IMMAGINE \_ rel \_ PPC \_ ADDR16 <br/>   | 0x0004 <br/> | I 16 bit bassi dell'oggetto VA della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMMAGINE \_ rel \_ PPC \_ ADDR14 <br/>   | 0x0005 <br/> | I 14 bit bassi dell'oggetto VA della destinazione. Questa proprietà è valida solo quando il simbolo di destinazione è assoluto e può essere esteso con segno al valore originale. <br/>                                                                                                                                                                                                                               |
| IMMAGINE \_ rel \_ PPC \_ REL24 <br/>    | 0x0006 <br/> | Offset relativo al PC a 24 bit nella posizione del simbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMMAGINE \_ rel \_ PPC \_ REL14 <br/>    | 0x0007 <br/> | Offset relativo al PC a 14 bit per la posizione del simbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMMAGINE \_ rel \_ PPC \_ ADDR32NB <br/> | 0x000A <br/> | RVA a 32 bit della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                           |
| IMMAGINE \_ rel \_ PPC \_ SECREL <br/>   | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                       |
| \_sezione Image rel \_ PPC \_ <br/>  | 0x000C <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                                                        |
| IMMAGINE \_ rel \_ PPC \_ SECREL16 <br/> | 0x000F <br/> | Offset a 16 bit della destinazione dall'inizio della relativa sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                       |
| IMMAGINE \_ rel \_ PPC \_ REFHI <br/>    | 0x0010 <br/> | I 16 bit alti della destinazione a 32 bit di destinazione. Viene utilizzato per la prima istruzione in una sequenza a due istruzioni che carica un indirizzo completo. Questa rilocazione deve essere seguita immediatamente da una rilocazione di coppie il cui SymbolTableIndex contiene uno spostamento con segno a 16 bit che viene aggiunto ai 16 bit superiori ricavati dalla posizione in cui si trova. <br/> |
| IMMAGINE \_ rel \_ PPC \_ REFLO <br/>    | 0x0011 <br/> | I 16 bit bassi dell'oggetto VA della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ rel \_ PPC \_ Pair <br/>     | 0x0012 <br/> | Rilocazione valida solo quando segue immediatamente una rilocazione REFHI o SECRELHI. Il SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                                                                                                                        |
| IMMAGINE \_ rel \_ PPC \_ SECRELLO <br/> | 0x0013 <br/> | I 16 bit bassi dell'offset a 32 bit della destinazione dall'inizio della relativa sezione. <br/>                                                                                                                                                                                                                                                                                   |
| IMMAGINE \_ rel \_ PPC \_ GPREL <br/>    | 0x0015 <br/> | Spostamento con segno a 16 bit della destinazione rispetto al registro GP. <br/>                                                                                                                                                                                                                                                                                               |
| IMMAGINE \_ del \_ token PPC rel \_ <br/>    | 0x0016 <br/> | Token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Processori Intel 386

Gli indicatori di tipo di rilocazione seguenti sono definiti per i processori Intel 386 e compatibili.



| Costante                               | Valore              | Descrizione                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMMAGINE \_ rel \_ i386 \_ Absolute <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                        |
| IMMAGINE \_ rel \_ \_ DIR16 <br/>    | 0x0001 <br/> | Non supportata. <br/>                                                                                                                                    |
| IMMAGINE \_ rel \_ \_ REL16 <br/>    | 0x0002 <br/> | Non supportata. <br/>                                                                                                                                    |
| IMMAGINE \_ rel \_ \_ DIR32 <br/>    | 0x0006 <br/> | Il VA a 32 bit di destinazione. <br/>                                                                                                                           |
| IMMAGINE \_ rel \_ \_ DIR32NB <br/>  | 0x0007 <br/> | RVA a 32 bit di destinazione. <br/>                                                                                                                          |
| IMMAGINE \_ rel \_ \_ SEG12 <br/>    | 0x0009 <br/> | Non supportata. <br/>                                                                                                                                    |
| \_Sezione Image rel \_ i386 \_ <br/>  | 0x000A <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                  |
| IMMAGINE \_ rel \_ \_ SECREL <br/>   | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/> |
| IMMAGINE \_ del \_ token i386 rel \_ <br/>    | 0x000C <br/> | Token CLR. <br/>                                                                                                                                    |
| IMMAGINE \_ rel \_ \_ SECREL7 <br/>  | 0x000D <br/> | Offset a 7 bit dalla base della sezione che contiene la destinazione. <br/>                                                                             |
| IMMAGINE \_ rel \_ \_ REL32 <br/>    | 0x0014 <br/> | Spostamento relativo a 32 bit nella destinazione. Supporta il ramo relativo x86 e le istruzioni di chiamata. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Famiglia di processori Intel Itanium (IPF)

Gli indicatori di tipo di rilocazione seguenti sono definiti per la famiglia di processori Intel Itanium e i processori compatibili. Si noti che le rilocazioni sulle istruzioni usano l'offset e il numero di slot del bundle per l'offset di rilocazione.



| Costante                                 | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMMAGINE \_ rel \_ ia64 \_ Absolute <br/>   | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ rel \_ \_ IMM14 ia64 <br/>      | 0x0001 <br/> | La rilocazione dell'istruzione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione prima di essere inserito nello slot specificato nel bundle IMM14. La destinazione della rilocazione deve essere assoluta o l'immagine deve essere fissa. <br/>                                                                                 |
| IMAGE \_ rel \_ \_ IMM22 ia64 <br/>      | 0x0002 <br/> | La rilocazione dell'istruzione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione prima di essere inserito nello slot specificato nel bundle IMM22. La destinazione della rilocazione deve essere assoluta o l'immagine deve essere fissa. <br/>                                                                                 |
| IMAGE \_ rel \_ \_ IMM64 ia64 <br/>      | 0x0003 <br/> | Il numero di slot di questa rilocazione deve essere uno (1). La rilocazione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione prima di essere archiviato in tutti e tre gli slot del bundle IMM64. <br/>                                                                                                                   |
| IMAGE \_ rel \_ \_ DIR32 ia64 <br/>      | 0x0004 <br/> | Il VA a 32 bit di destinazione. Questa operazione è supportata solo per/LARGEADDRESSAWARE: NO images. <br/>                                                                                                                                                                                                                                                    |
| IMAGE \_ rel \_ \_ DIR64 ia64 <br/>      | 0x0005 <br/> | Il VA a 64 bit di destinazione. <br/>                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ rel \_ \_ PCREL21B ia64 <br/>   | 0x0006 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 16 bit. I 4 bit inferiori dello spostamento sono pari a zero e non vengono archiviati. <br/>                                                                                                                                                                     |
| IMAGE \_ rel \_ \_ PCREL21M ia64 <br/>   | 0x0007 <br/> | L'istruzione è fissata con lo spostamento relativo a 25 bit alla destinazione allineata a 16 bit. I 4 bit inferiori dello spostamento, che sono zero, non vengono archiviati. <br/>                                                                                                                                                                 |
| IMAGE \_ rel \_ \_ PCREL21F ia64 <br/>   | 0x0008 <br/> | Il LSB dell'offset della rilocazione deve contenere il numero di slot mentre il resto è l'indirizzo del bundle. Il bundle è stato risolto con lo spostamento relativo a 25 bit per la destinazione allineata a 16 bit. I 4 bit inferiori dello spostamento sono pari a zero e non vengono archiviati. <br/>                                                                |
| IMAGE \_ rel \_ \_ GPREL22 ia64 <br/>    | 0x0009 <br/> | La rilocazione dell'istruzione può essere seguita da una rilocazione ADDEND il cui valore viene aggiunto all'indirizzo di destinazione e quindi da un offset relativo a GP a 22 bit che viene calcolato e applicato al bundle GPREL22. <br/>                                                                                                                            |
| IMAGE \_ rel \_ \_ LTOFF22 ia64 <br/>    | 0x000A <br/> | L'istruzione è fissata con l'offset relativo al GP a 22 bit alla voce della tabella letterale del simbolo di destinazione. Il linker crea questa voce di tabella letterale in base a questa rilocazione e alla rilocazione ADDEND che potrebbe seguire. <br/>                                                                                                        |
| \_Sezione Image rel \_ ia64 \_ <br/>    | 0x000B <br/> | L'indice della sezione a 16 bit della sezione contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                         |
| IMAGE \_ rel \_ \_ SECREL22 ia64 <br/>   | 0x000C <br/> | L'istruzione è fissata con l'offset a 22 bit della destinazione dall'inizio della sezione. Questa rilocazione può essere seguita immediatamente da una rilocazione ADDEND, il cui campo valore contiene l'offset senza segno a 32 bit della destinazione dall'inizio della sezione. <br/>                                                     |
| IMAGE \_ rel \_ \_ SECREL64I ia64 <br/>  | 0x000D <br/> | Il numero di slot per questa rilocazione deve essere uno (1). L'istruzione è fissata con l'offset a 64 bit della destinazione dall'inizio della sezione. Questa rilocazione può essere seguita immediatamente da una rilocazione ADDEND il cui campo valore contiene l'offset senza segno a 32 bit della destinazione dall'inizio della sezione. <br/> |
| IMAGE \_ rel \_ \_ SECREL32 ia64 <br/>   | 0x000E <br/> | Indirizzo dei dati da correggere con l'offset a 32 bit della destinazione dall'inizio della relativa sezione. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ rel \_ \_ DIR32NB ia64 <br/>    | 0x0010 <br/> | RVA a 32 bit di destinazione. <br/>                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ rel \_ \_ SREL14 ia64 <br/>     | 0x0011 <br/> | Viene applicato a un controllo immediato a 14 bit con segno che contiene la differenza tra due destinazioni Relocatable. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già emesso questo valore. <br/>                                                                                                              |
| IMAGE \_ rel \_ \_ SREL22 ia64 <br/>     | 0x0012 <br/> | Questa operazione viene applicata a un controllo immediato a 22 bit con segno che contiene la differenza tra due destinazioni Relocatable. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già emesso questo valore. <br/>                                                                                                              |
| IMAGE \_ rel \_ \_ SREL32 ia64 <br/>     | 0x0013 <br/> | Viene applicato a un controllo immediato a 32 bit con segno che contiene la differenza tra due valori Relocatable. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già emesso questo valore. <br/>                                                                                                               |
| IMAGE \_ rel \_ \_ UREL32 ia64 <br/>     | 0x0014 <br/> | Questa operazione viene applicata a un controllo immediato a 32 bit senza segno che contiene la differenza tra due valori Relocatable. Si tratta di un campo dichiarativo per il linker che indica che il compilatore ha già emesso questo valore. <br/>                                                                                                            |
| IMAGE \_ rel \_ \_ PCREL60X ia64 <br/>   | 0x0015 <br/> | Correzione relativa al PC a 60 bit che rimane sempre come istruzione BRL di un bundle MLX. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ \_ PCREL60B ia64 <br/>   | 0x0016 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione si inserisce in un campo con segno a 25 bit, convertire l'intero Bundle in un bundle MBB con NOP. B nello slot 1 e un'istruzione BR a 25 bit (con i 4 bit più bassi tutti zero ed eliminati) nello slot 2. <br/>                                                                                          |
| IMAGE \_ rel \_ \_ PCREL60F ia64 <br/>   | 0x0017 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione si inserisce in un campo con segno a 25 bit, convertire l'intero Bundle in un bundle MFB con NOP. F nello slot 1 e a 25 bit (4 bit più bassi tutti zero ed eliminati) istruzione BR nello slot 2. <br/>                                                                                                   |
| IMAGE \_ rel \_ \_ PCREL60I ia64 <br/>   | 0x0018 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione si inserisce in un campo con segno a 25 bit, convertire l'intero Bundle in un bundle MIB con NOP. I in slot 1 e a 25 bit (4 bit più bassi tutti zero ed eliminati) istruzione BR nello slot 2. <br/>                                                                                                   |
| IMAGE \_ rel \_ \_ PCREL60M ia64 <br/>   | 0x0019 <br/> | Correzione relativa al PC a 60 bit. Se lo spostamento di destinazione si inserisce in un campo con segno a 25 bit, convertire l'intero Bundle in un bundle MMB con NOP. M nello slot 1 e a 25 bit (4 bit più bassi tutti zero ed eliminati) istruzione BR nello slot 2. <br/>                                                                                                   |
| IMAGE \_ rel \_ \_ IMMGPREL64 ia64 <br/> | 0x001a <br/> | Correzione relativa A GP a 64 bit. <br/>                                                                                                                                                                                                                                                                                                         |
| IMMAGINE \_ del \_ token rel ia64 \_ <br/>      | 0x001b <br/> | Token CLR. <br/>                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ rel \_ \_ GPREL32 ia64 <br/>    | 0x001c <br/> | Correzione relativa A GP a 32 bit. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ rel \_ \_ Addend ia64 <br/>     | 0x001F <br/> | La rilocazione è valida solo quando segue immediatamente una delle seguenti rilocazioni: IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I o SECREL32. Il valore contiene Addend da applicare alle istruzioni all'interno di un bundle, non per i dati. <br/>                                                                  |



 

##### <a name="mips-processors"></a>Processori MIPS

Per i processori MIPS sono definiti i seguenti indicatori di tipo di rilocazione.



| Costante                                | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ MIPS \_ Absolute <br/>  | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ rel \_ \_ REFHALF <br/>   | 0x0001 <br/> | I 16 bit alti della destinazione a 32 bit di destinazione. <br/>                                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ rel \_ \_ REFWORD <br/>   | 0x0002 <br/> | Il VA a 32 bit di destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ \_ JMPADDR <br/>   | 0x0003 <br/> | I 26 bit bassi della destinazione VA. Sono supportate le istruzioni MIPS J e JAL. <br/>                                                                                                                                                                                                                                                                                      |
| IMAGE \_ rel \_ \_ REFHI <br/>     | 0x0004 <br/> | I 16 bit alti della destinazione a 32 bit di destinazione. Viene utilizzato per la prima istruzione in una sequenza a due istruzioni che carica un indirizzo completo. Questa rilocazione deve essere seguita immediatamente da una rilocazione di coppie il cui SymbolTableIndex contiene uno spostamento con segno a 16 bit che viene aggiunto ai 16 bit superiori che vengono ricavati dalla posizione in cui si trova. <br/> |
| IMAGE \_ rel \_ \_ REFLO <br/>     | 0x0005 <br/> | I 16 bit bassi dell'oggetto VA della destinazione. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ rel \_ \_ GPREL <br/>     | 0x0006 <br/> | Spostamento con segno a 16 bit della destinazione rispetto al registro GP. <br/>                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ MIPS \_ valore letterale <br/>   | 0x0007 <br/> | Equivale a IMAGE \_ rel \_ \_ GPREL. <br/>                                                                                                                                                                                                                                                                                                                                    |
| \_sezione Image rel \_ MIPS \_ <br/>   | 0x000A <br/> | L'indice della sezione a 16 bit della sezione contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                                                             |
| IMAGE \_ rel \_ \_ SECREL <br/>    | 0x000B <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ rel \_ \_ SECRELLO <br/>  | 0x000C <br/> | I 16 bit bassi dell'offset a 32 bit della destinazione dall'inizio della relativa sezione. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ rel \_ \_ SECRELHI <br/>  | 0x000D <br/> | 16 bit alti dell'offset a 32 bit della destinazione dall'inizio della sezione. È necessario che la rilocazione di una coppia di immagini \_ rel \_ MIPS \_ sia immediatamente successiva. Il SymbolTableIndex della rilocazione della coppia contiene uno spostamento con segno a 16 bit che viene aggiunto ai 16 bit superiori che vengono ricavati dalla posizione in cui viene rilocata. <br/>                            |
| IMAGE \_ rel \_ \_ JMPADDR16 <br/> | 0x0010 <br/> | I 26 bit bassi della destinazione VA. Supporta l'istruzione MIPS16 JAL. <br/>                                                                                                                                                                                                                                                                                           |
| IMAGE \_ rel \_ \_ REFWORDNB <br/> | 0x0022 <br/> | RVA a 32 bit di destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                |
| IMMAGINE \_ della \_ coppia rel MIPS \_ <br/>      | 0x0025 <br/> | La rilocazione è valida solo quando segue immediatamente una rilocazione REFHI o SECRELHI. Il SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>Mitsubishi M32R

Per i processori Mitsubishi M32R sono definiti gli indicatori di tipo rilocazione seguenti.



| Costante                               | Valore              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ rel \_ M32R \_ Absolute <br/> | 0x0000 <br/> | La rilocazione viene ignorata. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ rel \_ M32R \_ ADDR32 <br/>   | 0x0001 <br/> | Il VA a 32 bit di destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ rel \_ M32R \_ ADDR32NB <br/> | 0x0002 <br/> | RVA a 32 bit di destinazione. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ rel \_ M32R \_ ADDR24 <br/>   | 0x0003 <br/> | La destinazione a 24 bit VA. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ rel \_ M32R \_ GPREL16 <br/>  | 0x0004 <br/> | Offset a 16 bit della destinazione dal registro GP. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ rel \_ M32R \_ PCREL24 <br/>  | 0x0005 <br/> | Offset a 24 bit della destinazione dal contatore del programma (PC), spostato a sinistra di 2 bit ed esteso con segno <br/>                                                                                                                                                                                                                                                                                                |
| IMAGE \_ rel \_ M32R \_ PCREL16 <br/>  | 0x0006 <br/> | Offset a 16 bit della destinazione dal PC, spostato a sinistra di 2 bit ed esteso con segno <br/>                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ rel \_ M32R \_ PCREL8 <br/>   | 0x0007 <br/> | Offset a 8 bit della destinazione dal PC, spostato a sinistra di 2 bit ed esteso con segno <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ rel \_ M32R \_ REFHALF <br/>  | 0x0008 <br/> | 16 MSBs della destinazione VA. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ rel \_ M32R \_ REFHI <br/>    | 0x0009 <br/> | 16 MSBs della destinazione VA, adattati per l'estensione del segno LSB. Viene utilizzato per la prima istruzione in una sequenza a due istruzioni che carica un indirizzo completo a 32 bit. Questa rilocazione deve essere seguita immediatamente da una rilocazione di coppie il cui SymbolTableIndex contiene uno spostamento con segno a 16 bit che viene aggiunto ai 16 bit superiori che vengono ricavati dalla posizione in cui si trova. <br/> |
| IMAGE \_ rel \_ M32R \_ REFLO <br/>    | 0x000A <br/> | 16 LSB della destinazione VA. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ rel \_ M32R \_ Pair <br/>     | 0x000B <br/> | La rilocazione deve seguire la rilocazione di REFHI. Il SymbolTableIndex contiene uno spostamento e non un indice nella tabella dei simboli. <br/>                                                                                                                                                                                                                                                             |
| \_Sezione Image rel \_ M32R \_ <br/>  | 0x000C <br/> | Indice della sezione a 16 bit della sezione che contiene la destinazione. Questa operazione viene utilizzata per supportare le informazioni di debug. <br/>                                                                                                                                                                                                                                                                                  |
| IMAGE \_ rel \_ M32R \_ SECREL <br/>   | 0x000D <br/> | Offset a 32 bit della destinazione dall'inizio della sezione. Viene usato per supportare le informazioni di debug e l'archiviazione locale di thread statici. <br/>                                                                                                                                                                                                                                                 |
| IMMAGINE \_ del \_ token M32R rel \_ <br/>    | 0x000E <br/> | Token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>Numeri di riga COFF (deprecato)

I numeri di riga COFF non vengono più prodotti e, in futuro, non verranno utilizzati.

I numeri di riga COFF indicano la relazione tra il codice e i numeri di riga nei file di origine. Il formato Microsoft per i numeri di riga COFF è simile a COFF standard, ma è stato esteso per consentire a una singola sezione di fare riferimento ai numeri di riga in più file di origine.

I numeri di riga COFF sono costituiti da una matrice di record a lunghezza fissa. La posizione (offset del file) e le dimensioni della matrice vengono specificate nell'intestazione della sezione. Ogni record di numeri di riga ha il formato seguente.



| Offset        | Dimensione          | Campo                  | Descrizione                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Tipo ( \* ) <br/>  | Si tratta di un'Unione di due campi: SymbolTableIndex e VirtualAddress. Il fatto che SymbolTableIndex o RVA venga utilizzato dipende dal valore di LineNumber. <br/> |
| 4 <br/> | 2 <br/> | LineNumber <br/> | Quando è diverso da zero, questo campo specifica un numero di riga in base 1. Se è zero, il campo tipo viene interpretato come indice della tabella dei simboli per una funzione. <br/>    |



 

Il campo tipo è un'Unione di campi a 2 4 byte: SymbolTableIndex e VirtualAddress.



| Offset        | Dimensione          | Campo                        | Descrizione                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | SymbolTableIndex <br/> | Utilizzato quando LineNumber è zero: indice della voce della tabella dei simboli per una funzione. Questo formato viene usato per indicare la funzione a cui fa riferimento un gruppo di record di numeri di riga. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Utilizzato quando LineNumber è diverso da zero: l'RVA del codice eseguibile che corrisponde alla riga di origine indicata. In un file oggetto, contiene il VA all'interno della sezione. <br/> |



 

Un record di numeri di riga può impostare il campo LineNumber su zero e puntare a una definizione di funzione nella tabella dei simboli oppure può funzionare come voce di un numero di riga standard assegnando un numero intero positivo (numero di riga) e l'indirizzo corrispondente nel codice dell'oggetto.

Un gruppo di voci di numeri di riga inizia sempre con il primo formato, ovvero l'indice di un simbolo di funzione. Se si tratta del primo record di numeri di riga nella sezione, sarà anche il nome del simbolo COMDAT per la funzione se è impostato il flag COMDAT della sezione. Vedere le [sezioni COMDAT (solo oggetto)](#comdat-sections-object-only). Il record ausiliario della funzione nella tabella dei simboli presenta un puntatore al campo LineNumber che punta allo stesso record di numeri di riga.

Un record che identifica una funzione è seguito da un numero qualsiasi di voci di numeri di riga che forniscono informazioni effettive sul numero di riga, ovvero voci con LineNumber maggiore di zero. Queste voci sono basate su uno, relativo all'inizio della funzione e rappresentano ogni riga di origine nella funzione ad eccezione della prima riga.

Il primo record di numeri di riga per l'esempio seguente, ad esempio, specifica la funzione ReverseSign (SymbolTableIndex di ReverseSign e LineNumber impostati su zero). Vengono quindi registrati i record con i valori LineNumber 1, 2 e 3, corrispondenti alle righe di origine, come indicato di seguito:


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>Tabella di simboli COFF

La tabella dei simboli in questa sezione viene ereditata dal formato COFF tradizionale. È diverso da Microsoft Visual C++ informazioni di debug. Un file può contenere sia una tabella dei simboli COFF che Visual C++ informazioni di debug e le due sono mantenute separate. Alcuni strumenti Microsoft usano la tabella dei simboli per scopi limitati ma importanti, ad esempio per la comunicazione di informazioni COMDAT al linker. I nomi di sezione e i nomi di file, nonché i simboli di codice e di dati, sono elencati nella tabella dei simboli.

Il percorso della tabella dei simboli è indicato nell'intestazione COFF.

La tabella dei simboli è una matrice di record, ogni 18 byte di lunghezza. Ogni record è un record di tabella di simboli standard o ausiliario. Un record standard definisce un simbolo o un nome e ha il formato seguente.



| Offset         | Dimensione          | Campo                          | Descrizione                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nome ( \* ) <br/>          | Nome del simbolo, rappresentato da un'Unione di tre strutture. Viene utilizzata una matrice di 8 byte se la lunghezza del nome non supera gli 8 byte. Per altre informazioni, vedere [rappresentazione del nome del simbolo](https://www.bing.com/search?q=Symbol+Name+Representation). <br/> |
| 8 <br/>  | 4 <br/> | Valore <br/>              | Valore associato al simbolo. L'interpretazione di questo campo dipende da SectionNumber e StorageClass. Un significato tipico è l'indirizzo Relocatable. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | Intero con segno che identifica la sezione, usando un indice in base uno nella tabella della sezione. Alcuni valori hanno un significato speciale, come definito nella sezione 5.4.2, "valori numero di sezione". <br/>                                         |
| 14 <br/> | 2 <br/> | Tipo <br/>               | Numero che rappresenta il tipo. Microsoft Tools imposta questo campo su 0x20 (Function) o 0x0 (non una funzione). Per ulteriori informazioni, vedere [rappresentazione del tipo](#type-representation). <br/>                                                |
| 16 <br/> | 1 <br/> | StorageClass <br/>       | Valore enumerato che rappresenta la classe di archiviazione. Per altre informazioni, vedere [classe di archiviazione](#storage-class). <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | NumberOfAuxSymbols <br/> | Numero di voci della tabella dei simboli ausiliari che seguono questo record. <br/>                                                                                                                                                           |



 

Zero o più record della tabella di simboli ausiliari seguono immediatamente ogni record della tabella di simboli standard. Tuttavia, in genere non più di un record di tabella di simboli ausiliario segue un record di tabella dei simboli standard, ad eccezione dei record. file con nomi di file lunghi. Ogni record ausiliario ha le stesse dimensioni di un record di tabella dei simboli standard (18 byte), ma anziché definire un nuovo simbolo, il record ausiliario fornisce informazioni aggiuntive sull'ultimo simbolo definito. La scelta tra diversi formati da usare dipende dal campo StorageClass. I formati attualmente definiti per i record della tabella dei simboli ausiliari sono riportati nella sezione 5,5, "record dei simboli ausiliari".

Gli strumenti che leggono le tabelle di simboli COFF devono ignorare i record di simboli ausiliari la cui interpretazione è sconosciuta. In questo modo è possibile estendere il formato della tabella dei simboli per aggiungere nuovi record ausiliari, senza compromettere gli strumenti esistenti.

#### <a name="symbol-name-representation"></a>Rappresentazione del nome del simbolo

Il campo ShortName in una tabella dei simboli è costituito da 8 byte che contengono il nome stesso, se non ha una lunghezza superiore a 8 byte oppure il campo ShortName restituisce un offset nella tabella di stringhe. Per determinare se viene specificato il nome stesso o un offset, verificare i primi 4 byte per verificarne l'uguaglianza su zero.

Per convenzione, i nomi vengono considerati come stringhe con codifica UTF-8 con terminazione zero.



| Offset        | Dimensione          | Campo                 | Descrizione                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | ShortName <br/> | Matrice di 8 byte. Questa matrice viene riempita con valori null a destra se la lunghezza del nome è inferiore a 8 byte. <br/> |
| 0 <br/> | 4 <br/> | Zeri <br/>    | Campo impostato su tutti zeri se il nome supera i 8 byte. <br/>                                     |
| 4 <br/> | 4 <br/> | Offset <br/>    | Offset nella tabella di stringhe. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Valori numero di sezione

In genere, il campo del valore della sezione in una voce della tabella dei simboli è un indice in base uno nella tabella della sezione. Tuttavia, questo campo è un intero con segno e può assumere valori negativi. I valori seguenti, minori di uno, hanno significati speciali.



| Costante                          | Valore          | Descrizione                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMMAGINE \_ sym non \_ definita <br/> | 0 <br/>  | Al record di simboli non è ancora stata assegnata una sezione. Un valore pari a zero indica che un riferimento a un simbolo esterno è definito altrove. Un valore diverso da zero è un simbolo comune con una dimensione specificata dal valore. <br/> |
| IMAGE \_ sym \_ Absolute <br/>  | -1 <br/> | Il simbolo ha un valore assoluto (non-relocatable) e non è un indirizzo. <br/>                                                                                                                                                  |
| IMAGE \_ sym \_ debug <br/>     | -2 <br/> | Il simbolo fornisce informazioni generali sul tipo o sul debug, ma non corrisponde a una sezione. Gli strumenti Microsoft usano questa impostazione insieme ai record. file (FILE di classe di archiviazione). <br/>                                            |



 

#### <a name="type-representation"></a>Rappresentazione del tipo

Il campo tipo di una voce della tabella dei simboli contiene 2 byte, dove ogni byte rappresenta le informazioni sul tipo. LSB rappresenta il tipo di dati semplice (base) e MSB rappresenta il tipo complesso, se presente:



| MSB                                                       | LSB                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Tipo complesso: None, POINTER, Function, array. <br/> | Tipo di base: Integer, a virgola mobile e così via. <br/> |



 

I valori seguenti sono definiti per il tipo di base, anche se gli strumenti Microsoft non utilizzano in genere questo campo e impostano LSB su 0. Al contrario, Visual C++ informazioni di debug vengono utilizzate per indicare i tipi. Tuttavia, i valori COFF possibili sono elencati qui per completezza.



| Costante                             | Valore          | Descrizione                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| IMMAGINE \_ di \_ tipo sym \_ null <br/>   | 0 <br/>  | Nessuna informazione sul tipo o tipo di base sconosciuto. Usa questa impostazione per Microsoft Tools <br/> |
| IMMAGINE \_ di \_ tipo sym \_ void <br/>   | 1 <br/>  | Nessun tipo valido; utilizzato con puntatori e funzioni void <br/>                       |
| IMMAGINE \_ sym \_ tipo \_ Char <br/>   | 2 <br/>  | Un carattere (byte con segno) <br/>                                                  |
| tipo di immagine \_ sym \_ \_ short <br/>  | 3 <br/>  | Intero con segno A 2 byte <br/>                                                    |
| IMMAGINE \_ \_ tipo sym \_ int <br/>    | 4 <br/>  | Tipo Integer naturale (normalmente di 4 byte in Windows) <br/>                       |
| \_ \_ lunghezza tipo sym \_ immagine <br/>   | 5 <br/>  | Intero con segno a 4 byte <br/>                                                    |
| IMMAGINE \_ di \_ tipo sym \_ float <br/>  | 6 <br/>  | Numero a virgola mobile a 4 byte <br/>                                             |
| IMMAGINE \_ di \_ tipo sym \_ Double <br/> | 7 <br/>  | Numero a virgola mobile a 8 byte <br/>                                            |
| \_ \_ struct tipo di immagine sym \_ <br/> | 8 <br/>  | Struttura <br/>                                                                |
| \_ \_ Unione tipo di immagine sym \_ <br/>  | 9 <br/>  | Unione <br/>                                                                    |
| \_ \_ enum tipo di immagine sym \_ <br/>   | 10 <br/> | Tipo enumerato <br/>                                                         |
| IMMAGINE \_ sym \_ tipo \_ Moe <br/>    | 11 <br/> | Membro dell'enumerazione (un valore specifico) <br/>                                 |
| IMAGE \_ sym \_ tipo \_ byte <br/>   | 12 <br/> | Byte; intero senza segno a 1 byte <br/>                                            |
| IMMAGINE \_ di \_ tipo SYM ( \_ Word) <br/>   | 13 <br/> | Una parola; intero senza segno a 2 byte <br/>                                            |
| IMAGE \_ sym \_ digitare \_ uint <br/>   | 14 <br/> | Un Unsigned Integer di dimensioni naturali (normalmente 4 byte) <br/>                    |
| IMMAGINE \_ di \_ tipo sym. \_ DWORD <br/>  | 15 <br/> | Intero senza segno a 4 byte <br/>                                                 |



 

Il byte più significativo specifica se il simbolo è un puntatore a, una funzione che restituisce o una matrice del tipo di base specificato in LSB. Gli strumenti Microsoft usano questo campo solo per indicare se il simbolo è una funzione, in modo che gli unici due valori risultanti siano 0x0 e 0x20 per il campo tipo. Tuttavia, altri strumenti possono utilizzare questo campo per comunicare altre informazioni.

È molto importante specificare correttamente l'attributo della funzione. Queste informazioni sono necessarie per il corretto funzionamento del collegamento incrementale. Per alcune architetture, le informazioni potrebbero essere necessarie per altri scopi.



| Costante                                | Valore         | Descrizione                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| IMAGE \_ sym \_ DTYPE \_ null <br/>     | 0 <br/> | Nessun tipo derivato; il simbolo è una variabile scalare semplice. <br/> |
| \_ \_ puntatore DTYPE immagine \_ sym <br/>  | 1 <br/> | Il simbolo è un puntatore al tipo di base. <br/>                    |
| IMAGE \_ sym \_ DTYPE \_ Function <br/> | 2 <br/> | Il simbolo è una funzione che restituisce un tipo di base. <br/>       |
| IMAGE \_ sym \_ DTYPE \_ Array <br/>    | 3 <br/> | Il simbolo è una matrice di tipo base. <br/>                     |



 

#### <a name="storage-class"></a>Classe di archiviazione

Il campo StorageClass della tabella dei simboli indica il tipo di definizione rappresentata da un simbolo. Nella tabella seguente sono riportati i valori possibili. Si noti che il campo StorageClass è un numero intero senza segno a 1 byte. Il valore speciale-1 deve pertanto essere considerato come il relativo equivalente senza segno, 0xFF.

Sebbene il formato COFF tradizionale usi molti valori della classe di archiviazione, gli strumenti Microsoft si basano su Visual C++ formato di debug per la maggior parte delle informazioni sui simboli e in genere usano solo quattro valori della classe di archiviazione: EXTERNAL (2), STATIC (3), FUNCTION (101) e FILE (103). Ad eccezione della seconda intestazione di colonna riportata di seguito, "value" deve essere usato per indicare il campo del valore del record di simboli (la cui interpretazione dipende dal numero trovato come classe di archiviazione).



| Costante                                          | Valore                 | Descrizione/interpretazione del campo del valore                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ fine \_ della funzione della classe \_ Image sym <br/>  | -1 (0xFF) <br/> | Simbolo speciale che rappresenta la fine della funzione, a scopo di debug. <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ sym \_ Class \_ null <br/>               | 0 <br/>         | Nessuna classe di archiviazione assegnata. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ sym \_ Class \_ automatico <br/>          | 1 <br/>         | Variabile automatica (stack). Il campo valore specifica l'offset del stack frame. <br/>                                                                                                                                                                                                                                              |
| IMAGE \_ sym \_ Class \_ External <br/>           | 2 <br/>         | Valore utilizzato dagli strumenti Microsoft per i simboli esterni. Il campo valore indica la dimensione se il numero di sezione è IMAGE \_ sym \_ undefined (0). Se il numero di sezione è diverso da zero, il campo del valore specifica l'offset nella sezione. <br/>                                                                                 |
| IMAGE \_ sym \_ Class \_ static <br/>             | 3 <br/>         | Offset del simbolo all'interno della sezione. Se il campo del valore è zero, il simbolo rappresenta il nome di una sezione. <br/>                                                                                                                                                                                                            |
| \_ \_ Registro classi sym \_ immagine <br/>           | 4 <br/>         | Variabile Register. Il campo valore specifica il numero di registro. <br/>                                                                                                                                                                                                                                                            |
| IMAGE \_ sym \_ Class \_ External \_ def <br/>      | 5 <br/>         | Simbolo definito esternamente. <br/>                                                                                                                                                                                                                                                                                           |
| \_ \_ etichetta classe sym \_ immagine <br/>              | 6 <br/>         | Etichetta del codice definita all'interno del modulo. Il campo valore specifica l'offset del simbolo all'interno della sezione. <br/>                                                                                                                                                                                                         |
| etichetta non definita dell'immagine \_ sym \_ Class \_ \_ <br/>   | 7 <br/>         | Riferimento a un'etichetta di codice non definita. <br/>                                                                                                                                                                                                                                                                               |
| IMAGE \_ sym \_ - \_ membro \_ della classe di \_ struct <br/> | 8 <br/>         | Membro della struttura. Il campo valore specifica il membro n. <br/>                                                                                                                                                                                                                                                               |
| \_argomento della \_ classe Image sym \_ <br/>           | 9 <br/>         | Argomento formale (parametro) di una funzione. Il campo valore specifica l'argomento n. <br/>                                                                                                                                                                                                                                      |
| \_ \_ tag struct della classe Image sym \_ \_ <br/>        | 10 <br/>        | Voce del nome del tag della struttura. <br/>                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ sym \_ classe \_ membro \_ di \_ Union <br/>  | 11 <br/>        | Membro di Unione. Il campo valore specifica il membro n. <br/>                                                                                                                                                                                                                                                                     |
| IMAGE \_ sym \_ tag di classe \_ Union \_ <br/>         | 12 <br/>        | Voce del nome del tag di Unione. <br/>                                                                                                                                                                                                                                                                                                      |
| \_definizione del \_ tipo di classe Image sym \_ \_ <br/>   | 13 <br/>        | Una voce typedef. <br/>                                                                                                                                                                                                                                                                                                               |
| IMAGE \_ sym \_ Class \_ undefined \_ static <br/>  | 14 <br/>        | Dichiarazione di dati statici. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ sym \_ - \_ tag enum class \_ <br/>          | 15 <br/>        | Una voce TagName di tipo enumerata. <br/>                                                                                                                                                                                                                                                                                              |
| IMAGE \_ sym \_ classe \_ membro \_ di \_ enum <br/>   | 16 <br/>        | Membro di un'enumerazione. Il campo valore specifica il membro n. <br/>                                                                                                                                                                                                                                                         |
| IMAGE \_ sym \_ classe \_ Register \_ param <br/>    | 17 <br/>        | Parametro register. <br/>                                                                                                                                                                                                                                                                                                          |
| \_campo di \_ bit della classe Image sym \_ \_ <br/>         | 18 <br/>        | Riferimento a un campo di bit. Il campo valore specifica il bit n nel campo di bit. <br/>                                                                                                                                                                                                                                                |
| IMMAGINE \_ del \_ blocco di classe sym \_ <br/>              | 100 <br/>       | Un record. BB (inizio del blocco) o EB (fine del blocco). Il campo del valore è l'indirizzo Relocatable della posizione del codice. <br/>                                                                                                                                                                                                      |
| funzione della classe di immagine \_ sym \_ \_ <br/>           | 101 <br/>       | Valore utilizzato dagli strumenti Microsoft per i record di simboli che definiscono l'ambito di una funzione: Begin function (. BF), End Function (. EF) e Lines nella funzione (. LF). Per i record. LF, il campo valore indica il numero di righe di origine nella funzione. Per i record. EF, il campo valore indica le dimensioni del codice della funzione. <br/> |
| \_ \_ \_ fine della classe dell'immagine sym \_ della classe \_ struct <br/>    | 102 <br/>       | Una voce di fine della struttura. <br/>                                                                                                                                                                                                                                                                                                     |
| IMMAGINE \_ del \_ file di classe sym \_ <br/>               | 103 <br/>       | Valore usato da Microsoft Tools, nonché dal formato COFF tradizionale, per il record di simboli del file di origine. Il simbolo è seguito da record ausiliari che denominano il file. <br/>                                                                                                                                                       |
| \_sezione della \_ classe Image sym \_ <br/>            | 104 <br/>       | Una definizione di una sezione (gli strumenti Microsoft usano invece la classe di archiviazione statica). <br/>                                                                                                                                                                                                                                                  |
| IMMAGINE \_ sym \_ classe \_ vulnerabile \_ esterna <br/>     | 105 <br/>       | Un oggetto esterno vulnerabile. Per ulteriori informazioni, vedere il [formato ausiliario 3: External vulnerabili](#auxiliary-format-3-weak-externals). <br/>                                                                                                                                                                                                           |
| IMAGE \_ sym \_ Class \_ - \_ token CLR <br/>         | 107 <br/>       | Simbolo del token CLR. Il nome è una stringa ASCII costituita dal valore esadecimale del token. Per ulteriori informazioni, vedere [definizione del token CLR (solo oggetto)](#clr-token-definition-object-only). <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Record di simboli ausiliari

I record della tabella di simboli ausiliari seguono sempre e si applicano a, alcuni record della tabella dei simboli standard. Un record ausiliario può avere qualsiasi formato riconoscibile dagli strumenti, ma è necessario allocare 18 byte in modo che la tabella dei simboli venga mantenuta come una matrice di dimensioni regolari. Attualmente, gli strumenti Microsoft riconoscono i formati ausiliari per i seguenti tipi di record: definizioni di funzione, simboli di inizio e fine delle funzioni (. BF ed. EF), External vulnerabili, nomi file e definizioni di sezione.

La progettazione COFF tradizionale include anche formati di record ausiliari per matrici e strutture. Gli strumenti Microsoft non li usano, ma inseriscono queste informazioni simboliche in Visual C++ formato di debug nelle sezioni debug.

#### <a name="auxiliary-format-1-function-definitions"></a>Formato ausiliario 1: definizioni di funzione

Un record di tabella dei simboli contrassegna l'inizio di una definizione di funzione se presenta tutti gli elementi seguenti: una classe di archiviazione di EXTERNAL (2), un valore di tipo che indica che si tratta di una funzione (0x20) e un numero di sezione maggiore di zero. Si noti che un record della tabella dei simboli con un numero di sezione non definito (0) non definisce la funzione e non dispone di un record ausiliario. I record dei simboli di definizione di funzione sono seguiti da un record ausiliario nel formato descritto di seguito:



| Offset         | Dimensione          | Campo                             | Descrizione                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | TagIndex <br/>              | Indice della tabella dei simboli del record di simboli. BF (Begin Function) corrispondente. <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | Dimensioni del codice eseguibile per la funzione stessa. Se la funzione si trova in una sezione specifica, SizeOfRawData nell'intestazione della sezione è maggiore o uguale a questo campo, a seconda delle considerazioni di allineamento. <br/> |
| 8 <br/>  | 4 <br/> | PointerToLinenumber <br/>   | Offset del file della prima voce di numero di riga COFF per la funzione oppure zero se non ne esiste alcuno. Per ulteriori informazioni, vedere la pagina relativa ai [numeri di riga COFF (deprecata)](#coff-line-numbers-deprecated). <br/>                          |
| 12 <br/> | 4 <br/> | PointerToNextFunction <br/> | Indice della tabella dei simboli del record per la funzione successiva. Se la funzione è l'ultima nella tabella dei simboli, questo campo è impostato su zero. <br/>                                                                           |
| 16 <br/> | 2 <br/> | Non utilizzato <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Formato ausiliario 2: simboli. BF e. EF

Per ogni definizione di funzione nella tabella dei simboli, tre elementi descrivono l'inizio, la fine e il numero di righe. Ognuno di questi simboli ha una funzione di classe di archiviazione (101):

Un record di simboli denominato. BF (Begin Function). Il campo del valore non è utilizzato.

Un record di simboli denominato. LF (righe nella funzione). Il campo valore indica il numero di righe nella funzione.

Un record di simboli denominato. EF (fine della funzione). Il campo del valore ha lo stesso numero del campo dimensione totale nel record dei simboli di definizione della funzione.

I record dei simboli. BF e. EF (ma non i record. LF) sono seguiti da un record ausiliario con il formato seguente:



| Offset         | Dimensione          | Campo                                         | Descrizione                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Non utilizzato <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | LineNumber <br/>                        | Numero di riga ordinale effettivo (1, 2, 3 e così via) all'interno del file di origine, corrispondente al record. BF o. EF. <br/>                                               |
| 6 <br/>  | 6 <br/> | Non utilizzato <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | PointerToNextFunction (solo. BF) <br/> | Indice della tabella dei simboli del record di simboli. BF successivo. Se la funzione è l'ultima nella tabella dei simboli, questo campo è impostato su zero. Non viene usato per i record. EF. <br/> |
| 16 <br/> | 2 <br/> | Non utilizzato <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Formato ausiliario 3: External vulnerabili

"External vulnerabili" è un meccanismo per i file oggetto che consente la flessibilità in fase di collegamento. Un modulo può contenere un simbolo esterno non risolto (SYM1), ma può includere anche un record ausiliario che indica che se SYM1 non è presente al momento del collegamento, per risolvere i riferimenti viene usato un altro simbolo esterno (sym2).

Se una definizione di SYM1 è collegata, viene risolto normalmente un riferimento esterno al simbolo. Se una definizione di SYM1 non è collegata, tutti i riferimenti all'oggetto esterno vulnerabile per SYM1 si riferiscono invece a sym2. Il simbolo esterno, sym2, deve essere sempre collegato; in genere, viene definito nel modulo che contiene il riferimento debole a SYM1.

Gli External vulnerabili sono rappresentati da un record della tabella dei simboli con una classe di archiviazione esterna, un numero di sezione UNDEF e un valore pari a zero. Il record di simboli esterno vulnerabile è seguito da un record ausiliario con il formato seguente:



| Offset        | Dimensione           | Campo                       | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | TagIndex <br/>        | Indice della tabella dei simboli di sym2, il simbolo da collegare se SYM1 non viene trovato. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Caratteristiche <br/> | Un valore di IMAGE \_ \_ \_ \_ unlibrary debole Search nolibrary indica che non deve essere eseguita alcuna ricerca di libreria per SYM1. <br/> Un valore di IMAGE \_ la \_ libreria di ricerca extern vulnerabile \_ \_ indica che deve essere eseguita una ricerca di libreria per SYM1. <br/> Un valore di IMAGE \_ \_ alias di \_ ricerca extern vulnerabile \_ indica che SYM1 è un alias di sym2. <br/> |
| 8 <br/> | 10 <br/> | Non utilizzato <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Si noti che il campo caratteristiche non è definito in WINNT. H viene invece utilizzato il campo dimensione totale.

#### <a name="auxiliary-format-4-files"></a>Formato ausiliario 4: file

Questo formato segue un record della tabella dei simboli con FILE di classe di archiviazione (103). Il nome del simbolo deve essere. file e il record ausiliario che segue fornisce il nome di un file di codice sorgente.



| Offset        | Dimensione           | Campo                 | Descrizione                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | File Name <br/> | Stringa ANSI che fornisce il nome del file di origine. Questa operazione viene riempita con valori null se è minore della lunghezza massima. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Formato ausiliario 5: definizioni di sezione

Questo formato segue un record della tabella di simboli che definisce una sezione. Un record di questo tipo ha un nome di simbolo che corrisponde al nome di una sezione, ad esempio. Text o. drectve, e ha una classe di archiviazione statica (3). Il record ausiliario fornisce informazioni sulla sezione a cui fa riferimento. Quindi, duplica alcune delle informazioni nell'intestazione della sezione.



| Offset         | Dimensione          | Campo                           | Descrizione                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Length <br/>              | Dimensione dei dati della sezione; uguale a SizeOfRawData nell'intestazione della sezione. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | NumberOfRelocations <br/> | Numero di voci di rilocazione per la sezione. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | NumberOfLinenumbers <br/> | Numero di voci di numeri di riga per la sezione. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | CheckSum <br/>            | Checksum per i dati comuni. È applicabile se il \_ \_ \_ flag COMDAT di Image SCN lnk è impostato nell'intestazione della sezione. Per ulteriori informazioni, vedere [COMDAT Sections (solo oggetto)](#comdat-sections-object-only). <br/> |
| 12 <br/> | 2 <br/> | Number <br/>              | Indice in base uno nella tabella della sezione per la sezione associata. Viene usato quando l'impostazione di selezione COMDAT è 5. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Selezione <br/>           | Numero di selezione COMDAT. Questa operazione è applicabile se la sezione è una sezione COMDAT. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | Non utilizzato <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>Sezioni COMDAT (solo oggetto)

Il campo di selezione del formato ausiliario per la definizione della sezione è applicabile se la sezione è una sezione COMDAT. Una sezione COMDAT è una sezione che può essere definita da più di un file oggetto. (Immagine \_ del flag \_ \_ Il campo SCN lnk COMDAT è impostato nel campo flag della sezione dell'intestazione della sezione. Il campo di selezione determina il modo in cui il linker risolve le più definizioni delle sezioni COMDAT.

Il primo simbolo che ha il valore della sezione COMDAT deve essere il simbolo della sezione. Questo simbolo ha il nome della sezione, il campo del valore uguale a zero, il numero di sezione della sezione COMDAT in questione, il campo tipo uguale a IMAGE \_ sym \_ Type \_ null, il campo della classe uguale a Image \_ sym \_ Class \_ static e un record ausiliario. Il secondo simbolo è denominato "simbolo COMDAT" e viene usato dal linker insieme al campo di selezione.

Di seguito sono riportati i valori per il campo di selezione.



| Costante                                        | Valore         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ COMDAT \_ Select \_ noduplicates <br/> | 1 <br/> | Se questo simbolo è già definito, il linker genera un errore di "simbolo di moltiplicazione definito". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ COMDAT \_ Select \_ any <br/>          | 2 <br/> | È possibile collegare qualsiasi sezione che definisce lo stesso simbolo COMDAT. i Rest vengono rimossi. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ selezionare le \_ stesse \_ dimensioni <br/>   | 3 <br/> | Il linker sceglie una sezione arbitraria tra le definizioni per questo simbolo. Se tutte le definizioni non hanno la stessa dimensione, viene generato un errore di "simbolo di moltiplicazione definito". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_COMDAT immagine \_ selezionare \_ \_ corrispondenza esatta <br/> | 4 <br/> | Il linker sceglie una sezione arbitraria tra le definizioni per questo simbolo. Se tutte le definizioni non corrispondono esattamente, viene generato un errore di "simbolo di moltiplicazione definito". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ selezionare \_ associativo <br/>  | 5 <br/> | La sezione è collegata se è collegata una certa altra sezione COMDAT. Questa altra sezione è indicata dal campo numerico del record dei simboli ausiliari per la definizione della sezione. Questa impostazione è utile per le definizioni che includono componenti in più sezioni, ad esempio il codice in uno e i dati di un'altra, ma in cui tutti devono essere collegati o eliminati come un set. L'altra sezione a cui è associata questa sezione deve essere una sezione COMDAT, che può essere un'altra sezione COMDAT associativa. Una catena di associazioni della sezione COMDAT associativa non può formare un ciclo. Alla fine, la catena di associazioni della sezione deve passare a una sezione COMDAT che non dispone dell'immagine \_ COMDAT \_ selezionare \_ set associativo. <br/> |
| IMMAGINE \_ COMDAT \_ selezionare \_ più grande <br/>      | 6 <br/> | Il linker sceglie la definizione più grande tra tutte le definizioni per questo simbolo. Se queste dimensioni sono più definizioni, la scelta tra di esse è arbitraria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>Definizione del token CLR (solo oggetto)

Questo simbolo ausiliario segue in genere \_ il \_ token CLR della classe Image sym \_ \_ . Viene usato per associare un token allo spazio dei nomi della tabella dei simboli COFF.



| Offset        | Dimensione           | Campo                        | Descrizione                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bAuxType <br/>         | Deve essere IMAGE \_ aux \_ Symbol \_ Type \_ token \_ def (1). <br/>                              |
| 1 <br/> | 1 <br/>  | bReserved <br/>        | Riservato, deve essere zero. <br/>                                                        |
| 2 <br/> | 4 <br/>  | SymbolTableIndex <br/> | Indice del simbolo del COFF a cui si riferisce la definizione del token CLR. <br/> |
| 6 <br/> | 12 <br/> |                              | Riservato, deve essere zero. <br/>                                                        |



 

### <a name="coff-string-table"></a>Tabella di stringhe COFF

Immediatamente dopo la tabella dei simboli COFF si trova la tabella di stringhe COFF. La posizione di questa tabella viene trovata prendendo l'indirizzo della tabella dei simboli nell'intestazione COFF e aggiungendo il numero di simboli moltiplicato per la dimensione di un simbolo.

All'inizio della tabella di stringhe COFF sono presenti 4 byte che contengono la dimensione totale (in byte) del resto della tabella di stringhe. Questa dimensione include il campo dimensioni stesso, in modo che il valore in questa posizione sia 4 se non sono presenti stringhe.

Le dimensioni seguenti sono stringhe con terminazione null a cui puntano i simboli della tabella dei simboli COFF.

### <a name="the-attribute-certificate-table-image-only"></a>Tabella dei certificati degli attributi (solo immagine)

È possibile associare i certificati di attributo a un'immagine aggiungendo una tabella dei certificati dell'attributo. La tabella dei certificati dell'attributo è costituita da un set di voci di certificato di attributo contigue e allineate a quadrupla. Per ottenere questo allineamento, viene inserita la spaziatura interna zero tra la fine originale del file e l'inizio della tabella dei certificati dell'attributo. Ogni voce di certificato di attributo contiene i campi seguenti.



| Offset       | Dimensione                         | Campo                       | Descrizione                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Specifica la lunghezza della voce del certificato dell'attributo. <br/>                                       |
| 4<br/> | 2<br/>                 | wRevision<br/>        | Contiene il numero di versione del certificato. Per informazioni dettagliate, vedere il testo seguente.<br/>                   |
| 6<br/> | 2<br/>                 | wCertificateType<br/> | Specifica il tipo di contenuto in bCertificate. Per informazioni dettagliate, vedere il testo seguente.<br/>             |
| 8<br/> | Vedere quanto segue<br/> | bCertificate<br/>     | Contiene un certificato, ad esempio una firma Authenticode. Per informazioni dettagliate, vedere il testo seguente.<br/> |



 

Il valore dell'indirizzo virtuale dalla voce della tabella del certificato nella directory dei dati di intestazione facoltativa è un offset del file alla prima voce del certificato dell'attributo. È possibile accedere alle voci successive avanzando i byte dwLength della voce, arrotondati per eccesso a un multiplo di 8 byte, dall'inizio della voce del certificato dell'attributo corrente. Questa operazione continua fino a quando la somma dei valori dwLength arrotondati è uguale al valore della dimensione della voce della tabella Certificates nella directory dei dati di intestazione facoltativa. Se la somma dei valori dwLength arrotondati non è uguale al valore di dimensione, la tabella del certificato dell'attributo o il campo delle dimensioni è danneggiato.

Ad esempio, se la voce della tabella di certificati della directory dei dati dell'intestazione facoltativa contiene:


```C++
virtual address = 0x5000
size = 0x1000
```



Il primo certificato inizia in corrispondenza dell'offset 0x5000 dall'inizio del file su disco. Per avanzare tra tutte le voci del certificato dell'attributo:

1.  Aggiungere il valore dwLength del primo certificato dell'attributo all'offset iniziale.
2.  Arrotondare il valore del passaggio 1 fino al multiplo più vicino a 8 byte per trovare l'offset della seconda voce del certificato dell'attributo.
3.  Aggiungere il valore di offset dal passaggio 2 al valore dwLength della seconda voce del certificato dell'attributo e arrotondare per eccesso al multiplo a 8 byte più vicino per determinare l'offset della terza voce del certificato dell'attributo.
4.  Ripetere il passaggio 3 per ogni certificato successivo fino a quando l'offset calcolato è uguale a 0x6000 (0x5000 Start + 0x1000 Total Size), che indica che è stata avviata l'intera tabella.

In alternativa, è possibile enumerare le voci del certificato chiamando la funzione **ImageEnumerateCertificates** di Win32 in un ciclo. Per un collegamento alla pagina di riferimento della funzione, vedere [riferimenti](#references).

Le voci della tabella dei certificati attributo possono contenere qualsiasi tipo di certificato, purché la voce abbia il valore dwLength corretto, un valore wRevision univoco e un valore wCertificateType univoco. Il tipo più comune di immissione della tabella dei certificati è una \_ struttura del certificato Win, documentata in wintrust. h, descritta nella parte restante di questa sezione.

Di seguito sono riportate le opzioni per il \_ membro Win certificate **wRevision** .



| Valore             | Nome                                 | Note                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | WIN \_ CERT \_ Revision \_ 1 \_ 0<br/> | Versione 1, versione legacy della struttura Win \_ Certificate. È supportato solo ai fini della verifica delle firme Authenticode legacy<br/> |
| 0x0200<br/> | WIN \_ CERT \_ Revision \_ 2 \_ 0<br/> | La versione 2 è la versione corrente della \_ struttura Win certificate. <br/>                                                                       |



 

Le opzioni per il \_ membro Win certificate **wCertificateType** includono, a titolo esemplificativo, gli elementi nella tabella seguente. Si noti che alcuni valori non sono attualmente supportati.



| Valore             | Nome                                           | Note                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | \_Tipo di certificato Win \_ \_ X509 <br/>              | bCertificate contiene un certificato X. 509 <br/> Non supportato<br/>         |
| 0x0002<br/> | \_dati con \_ \_ firma PKCS \_ di tipo certificato Win \_<br/> | bCertificate contiene una \# struttura SIGNEDDATA PKCS 7<br/>                         |
| 0x0003<br/> | \_Tipo di certificato Win \_ \_ riservato \_ 1<br/>        | Riservato <br/>                                                                    |
| 0x0004<br/> | \_ \_ \_ \_ firma dello stack TS del tipo di certificato Win \_<br/>  | Firma del certificato dello stack del protocollo Terminal Server <br/> Non supportato<br/> |



 

Il \_ membro **bCertificate** della struttura del certificato Win contiene una matrice di byte a lunghezza variabile con il tipo di contenuto specificato da **wCertificateType**. Il tipo supportato da Authenticode è il \_ \_ tipo di certificato Win \_ dati con \_ firma PKCS \_ , una \# struttura PKCS 7 **SignedData** . Per informazioni dettagliate sul formato di firma digitale Authenticode, vedere il [formato di firma eseguibile di Windows Authenticode Portable](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Se il contenuto di **bCertificate** non termina con un limite di Quadrupla, la voce del certificato dell'attributo viene riempita con zeri, dalla fine di **bCertificate** al limite di quadrupla successivo.

Il valore **dwLength** è la lunghezza della struttura del certificato Win finalizzato \_ e viene calcolato come:

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Questa lunghezza deve includere le dimensioni di qualsiasi riempimento utilizzato per soddisfare il requisito che ogni \_ struttura del certificato Win sia allineata quadrupla:

` dwLength += (8 - (dwLength & 7)) & 7;`

La **dimensione della tabella del certificato** specificata nella voce della **tabella Certificates** nelle [directory dei dati di intestazione facoltativa (solo immagine)](#optional-header-data-directories-image-only)include la spaziatura interna.

Per altre informazioni sull'uso dell'API ImageHlp per enumerare, aggiungere e rimuovere certificati da file PE, vedere [funzioni Imagehlp](imagehlp-functions.md).

#### <a name="certificate-data"></a>Dati del certificato

Come indicato nella sezione precedente, i certificati nella tabella certificati attributo possono contenere qualsiasi tipo di certificato. I certificati che assicurano l'integrità di un file PE possono includere un hash dell'immagine PE.

Un hash dell'immagine PE (o hash file) è simile al checksum di un file in quanto l'algoritmo hash produce un digest del messaggio correlato all'integrità di un file. Tuttavia, un checksum è prodotto da un algoritmo semplice e viene usato principalmente per rilevare se un blocco di memoria su disco è peggiorato e i valori archiviati sono diventati danneggiati. Un hash di file è simile a un checksum in quanto rileva anche il danneggiamento del file. Tuttavia, a differenza della maggior parte degli algoritmi di checksum, è molto difficile modificare un file senza modificare l'hash del file dal valore originale non modificato. Un hash di file può quindi essere usato per rilevare modifiche intenzionali e persino minime a un file, ad esempio quelle introdotte da virus, pirati informatici o programmi Trojan Horse.

Quando è incluso in un certificato, il digest dell'immagine deve escludere determinati campi nell'immagine PE, ad esempio la voce relativa al checksum e alla tabella dei certificati in directory di dati di intestazione facoltative. Questo perché l'azione di aggiunta di un certificato modifica questi campi e determina il calcolo di un valore hash diverso.

La funzione Win32 **ImageGetDigestStream** fornisce un flusso di dati da un file PE di destinazione con cui eseguire le funzioni hash. Questo flusso di dati resta coerente quando vengono aggiunti o rimossi certificati da un file PE. In base ai parametri passati a **ImageGetDigestStream**, altri dati dell'immagine PE possono essere omessi dal calcolo hash. Per un collegamento alla pagina di riferimento della funzione, vedere [riferimenti](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load importare tabelle (solo immagine)

Queste tabelle sono state aggiunte all'immagine per supportare un meccanismo uniforme che consente alle applicazioni di ritardare il caricamento di una DLL fino alla prima chiamata a tale DLL. Il layout delle tabelle corrisponde a quello delle tabelle di importazione tradizionali descritte nella sezione 6,4, [la sezione. idata](#the-idata-section)". Qui sono illustrati solo alcuni dettagli.

#### <a name="the-delay-load-directory-table"></a>Tabella di Delay-Load directory

La tabella directory di caricamento ritardato è la controparte della tabella di importazione directory. Può essere recuperato tramite la voce del descrittore di importazione ritardata nell'elenco directory dei dati intestazione facoltativa (offset 200). La tabella viene disposta nel modo seguente:



| Offset         | Dimensione          | Campo                                  | Descrizione                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Attributi <br/>                 | Deve essere zero. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Nome <br/>                       | RVA del nome della DLL da caricare. Il nome risiede nella sezione di dati di sola lettura dell'immagine. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Handle del modulo <br/>              | RVA dell'handle del modulo (nella sezione dati dell'immagine) della DLL da caricare in modo ritardato. Viene usato per l'archiviazione dalla routine fornita per gestire il caricamento ritardato. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Tabella degli indirizzi di importazione ritardata <br/> | RVA della tabella degli indirizzi di importazione a caricamento ritardato. Per ulteriori informazioni, vedere [tabella degli indirizzi di importazione ritardata (IAT)](#delay-import-address-table). <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Tabella nome importazione ritardata <br/>    | RVA della tabella dei nomi di caricamento ritardato, che contiene i nomi delle importazioni che potrebbero dover essere caricate. Corrisponde al layout della tabella dei nomi di importazione. Per ulteriori informazioni, vedere la [tabella hint/Name](#hintname-table).<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Tabella di importazione ritardata associata <br/>   | RVA della tabella dell'indirizzo di caricamento ritardato associato, se esistente. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Scarica tabella di importazione ritardata <br/>  | RVA della tabella di indirizzi di caricamento ritardato di scaricamento, se esistente. Si tratta di una copia esatta della tabella degli indirizzi di importazione ritardata. Se il chiamante Scarica la DLL, questa tabella deve essere copiata di nuovo sulla tabella degli indirizzi di importazione ritardata in modo che le successive chiamate alla DLL continuino a usare correttamente il meccanismo di thunk. <br/> |
| 28 <br/> | 4 <br/> | Timestamp <br/>                 | Timestamp della DLL a cui è stata associata questa immagine. <br/>                                                                                                                                                                                                                                                     |



 

Le tabelle a cui viene fatto riferimento in questa struttura di dati sono organizzate e ordinate esattamente come le rispettive controparti per le importazioni tradizionali. Per informazioni dettagliate, vedere [la sezione. idata](#the-idata-section).

#### <a name="attributes"></a>Attributi

Non è ancora stato definito alcun flag di attributo. Il linker imposta questo campo su zero nell'immagine. Questo campo può essere usato per estendere il record indicando la presenza di nuovi campi o può essere usato per indicare comportamenti per le funzioni di supporto delay o Unload.

#### <a name="name"></a>Nome

Il nome della DLL da caricare in modo ritardato risiede nella sezione di dati di sola lettura dell'immagine. Viene fatto riferimento tramite il campo szName.

#### <a name="module-handle"></a>Handle del modulo

L'handle della DLL da caricare in modo ritardato si trova nella sezione dati dell'immagine. Il campo phmod punta all'handle. L'helper di caricamento ritardato fornito usa questo percorso per archiviare l'handle per la DLL caricata.

#### <a name="delay-import-address-table"></a>Tabella degli indirizzi di importazione ritardata

Viene fatto riferimento alla tabella di indirizzi di importazione ritardata (IAT) dal descrittore dell'importazione ritardata tramite il campo pIAT. L'helper per il caricamento ritardato aggiorna questi puntatori con i punti di ingresso reali, in modo che i thunk non siano più nel ciclo chiamante. Per accedere ai puntatori a funzione, utilizzare l'espressione `pINT->u1.Function` .

#### <a name="delay-import-name-table"></a>Tabella nome importazione ritardata

La tabella dei nomi dell'importazione ritardata (INT) contiene i nomi delle importazioni che potrebbero richiedere il caricamento. Sono ordinati in modo analogo ai puntatori a funzione nella tabella IAT. Sono costituite dalle stesse strutture dell'INT standard e a cui si accede tramite l'espressione `pINT->u1.AddressOfData->Name[0]` .

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Tabella degli indirizzi di importazione con associazione ritardata e timestamp

La tabella di indirizzi di importazione con binding ritardato (BIAT) è una tabella facoltativa di elementi di dati di IMAGE \_ thunk \_ utilizzata insieme al campo timestamp della tabella di directory per il caricamento ritardato da parte di una fase di associazione post-elaborazione.

#### <a name="delay-unload-import-address-table"></a>Tabella degli indirizzi di importazione dello scaricamento ritardato

La tabella di indirizzi di importazione UIAT è una tabella facoltativa di elementi di \_ dati del thunk di immagine \_ utilizzata dal codice di scaricamento per gestire una richiesta di scaricamento esplicita. È costituito da dati inizializzati nella sezione di sola lettura che è una copia esatta della IAT originale che ha fatto riferimento al codice per i thunk di caricamento ritardato. Nella richiesta di scaricamento la libreria può essere liberata, \* phmod deselezionata e il Uiat scritto sulla tabella IAT per ripristinare tutto lo stato di precaricamento.

## <a name="special-sections"></a>Sezioni speciali

- [Sezione. debug](#the-debug-section)
  - [Directory di debug (solo immagine)](#debug-directory-image-only)
  - [Tipo di debug](#debug-type)
  - [. debug $ F (solo oggetto)](#debugf-object-only)
  - [. debug $ S (solo oggetto)](#debugs-object-only)
  - [. debug $ P (solo oggetto)](#debugp-object-only)
  - [. debug $ T (solo oggetto)](#debugt-object-only)
  - [Supporto del linker per le informazioni di debug Microsoft](#linker-support-for-microsoft-debug-information)
- [Sezione. drectve (solo oggetto)](#the-drectve-section-object-only)
- [Sezione. edata (solo immagine)](#the-edata-section-image-only)
  - [Esporta tabella directory](#export-directory-table)
  - [Esporta tabella indirizzi](#export-address-table)
  - [Esporta tabella puntatore al nome](#export-name-pointer-table)
  - [Esporta tabella ordinale](#export-ordinal-table)
  - [Esporta tabella nome](#export-name-table)
- [Sezione. idata](#the-idata-section)
  - [Importa tabella directory](#import-directory-table)
  - [Importa tabella di ricerca](#import-lookup-table)
  - [Tabella di hint/nomi](#hintname-table)
  - [Importa tabella indirizzi](#delay-import-address-table)
- [Sezione. pData](#the-pdata-section)
- [Sezione. reloc (solo immagine)](#the-reloc-section-image-only)
  - [Blocco di rilocazione di base](#base-relocation-block)
  - [Tipi di rilocazione di base](#base-relocation-types)
- [Sezione. TLS](#the-tls-section)
  - [Directory TLS](#the-tls-directory)
  - [Funzioni di callback TLS](#tls-callback-functions)
- [Struttura di configurazione di caricamento (solo immagine)](#the-load-configuration-structure-image-only)
  - [Carica directory di configurazione](#load-configuration-directory)
  - [Carica layout di configurazione](#load-configuration-layout)
- [Sezione. rsrc](#the-rsrc-section)
  - [Tabella directory delle risorse](#resource-directory-table)
  - [Voci della directory delle risorse](#resource-directory-entries)
  - [Stringa di directory delle risorse](#resource-directory-string)
  - [Immissione dati risorsa](#resource-data-entry)
- [Sezione. cormeta (solo oggetto)](#the-cormeta-section-object-only)
- [Sezione. sxdata](#the-sxdata-section)

Le sezioni COFF tipiche contengono il codice o i dati che i linker e i caricatori di Microsoft Win32 elaborano senza una conoscenza particolare del contenuto della sezione. Il contenuto è pertinente solo per l'applicazione collegata o eseguita.

Tuttavia, alcune sezioni COFF hanno significati speciali quando vengono rilevati nei file oggetto o nei file di immagine. Gli strumenti e i caricatori riconoscono queste sezioni perché hanno flag speciali impostati nell'intestazione della sezione, perché i percorsi speciali nell'intestazione facoltativa image puntano a essi, oppure perché il nome della sezione stessa indica una funzione speciale della sezione. (Anche se il nome della sezione non indica una funzione speciale della sezione, il nome della sezione è determinato dalla convenzione, quindi gli autori di questa specifica possono fare riferimento a un nome di sezione in tutti i casi).

Le sezioni riservate e i relativi attributi sono descritti nella tabella seguente, seguita da descrizioni dettagliate per i tipi di sezione che vengono salvati in modo permanente in eseguibili e i tipi di sezione che contengono metadati per le estensioni.



| Nome della sezione          | Content                                                                                                                                                                  | Caratteristiche                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| . bss <br/>      | Dati non inizializzati (formato libero) <br/>                                                                                                                             | IMAGE \_ SCN \_ CNT immagine dei dati non inizializzata immagine di SCN memoria memoria immagine \_ \_ \| \_ \_ \_ \| \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                               |
| .cormeta <br/>  | Metadati CLR che indicano che il file oggetto contiene codice gestito <br/>                                                                                       | IMAGE \_ SCN \_ lnk \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . Data <br/>     | Dati inizializzati (formato libero) <br/>                                                                                                                               | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| immagine SCN \_ \_ mem \_ lettura \| immagine \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . debug $ F <br/>  | Informazioni di debug Polinesia generate (solo oggetto, solo architettura x86 e ora obsolete) <br/>                                                                       | IMAGE \_ SCN \_ CNT immagine \_ dei dati inizializzati SCN immagine \_ \| \_ \_ \_ lettura \| immagine \_ \_ memoria SCN mem \_ <br/>                                                                                                                                                                                                                                                                                           |
| . debug $ P <br/>  | Tipi di debug precompilati (solo oggetto) <br/>                                                                                                                        | IMAGE \_ SCN \_ CNT immagine \_ dei dati inizializzati SCN immagine \_ \| \_ \_ \_ lettura \| immagine \_ \_ memoria SCN mem \_ <br/>                                                                                                                                                                                                                                                                                           |
| . debug $ S <br/>  | Simboli di debug (solo oggetto) <br/>                                                                                                                                  | IMAGE \_ SCN \_ CNT immagine \_ dei dati inizializzati SCN immagine \_ \| \_ \_ \_ lettura \| immagine \_ \_ memoria SCN mem \_ <br/>                                                                                                                                                                                                                                                                                           |
| . debug $ T <br/>  | Tipi di debug (solo oggetto) <br/>                                                                                                                                    | IMAGE \_ SCN \_ CNT immagine \_ dei dati inizializzati SCN immagine \_ \| \_ \_ \_ lettura \| immagine \_ \_ memoria SCN mem \_ <br/>                                                                                                                                                                                                                                                                                           |
| .drective <br/> | Opzioni del linker <br/>                                                                                                                                               | IMAGE \_ SCN \_ lnk \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .edata <br/>    | Esporta tabelle <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| \_ SCN \_ \_ lettura mem <br/>                                                                                                                                                                                                                                                                                                                           |
| . idata <br/>    | Importa tabelle <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| immagine SCN \_ \_ mem \_ lettura \| immagine \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . idlsym <br/>   | Include SEH (solo immagine) registrato per supportare gli attributi IDL. Per informazioni, vedere "attributi IDL" nei [riferimenti](#references) alla fine di questo argomento. <br/> | IMAGE \_ SCN \_ lnk \_ info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . pData <br/>    | Informazioni sulle eccezioni <br/>                                                                                                                                        | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| \_ SCN \_ \_ lettura mem <br/>                                                                                                                                                                                                                                                                                                                           |
| . rdata <br/>    | Dati inizializzati di sola lettura <br/>                                                                                                                                   | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| \_ SCN \_ \_ lettura mem <br/>                                                                                                                                                                                                                                                                                                                           |
| . reloc <br/>    | Rilocazioni di immagini <br/>                                                                                                                                            | IMAGE \_ SCN \_ CNT immagine \_ dei dati inizializzati SCN immagine \_ \| \_ \_ \_ lettura \| immagine \_ \_ memoria SCN mem \_ <br/>                                                                                                                                                                                                                                                                                           |
| . rsrc <br/>     | Directory delle risorse <br/>                                                                                                                                           | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| \_ SCN \_ \_ lettura mem <br/>                                                                                                                                                                                                                                                                                                                           |
| . sbss <br/>     | GP-dati non inizializzati relativi (formato libero) <br/>                                                                                                                 | IMAGE \_ SCN \_ CNT immagine \_ dei dati non inizializzati SCN memoria immagine memoria SCN mem \_ \| Write Image \_ \_ \_ \| \_ \_ \_ \| \_ SCN \_ GPREL the image \_ SCN \_ GPREL flag deve essere impostato solo per le architetture ia64; questo flag non è valido per altre architetture. Il \_ \_ flag GPREL SCN image è solo per i file oggetto. quando questo tipo di sezione viene visualizzato in un file di immagine, il flag GPREL per l'immagine \_ SCN \_ non deve essere impostato. <br/> |
| . sdata <br/>    | GP-dati inizializzati relativi (formato libero) <br/>                                                                                                                   | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzata \| immagine SCN \_ \_ mem \_ Read \| Image \_ SCN \_ mem \_ Write \| Image \_ SCN \_ GPREL the image \_ SCN \_ GPREL flag deve essere impostato solo per le architetture ia64; questo flag non è valido per altre architetture. Il \_ \_ flag GPREL SCN image è solo per i file oggetto. quando questo tipo di sezione viene visualizzato in un file di immagine, il flag GPREL per l'immagine \_ SCN \_ non deve essere impostato. <br/>   |
| .srdata <br/>   | Dati di sola lettura relativi al GP (formato libero) <br/>                                                                                                                     | IMAGE \_ SCN \_ CNT \_ inizializzazione \_ dei dati \| immagine SCN \_ \_ mem \_ Read \| Image \_ SCN \_ GPREL the image \_ SCN \_ GPREL flag deve essere impostato solo per le architetture ia64; questo flag non è valido per altre architetture. Il \_ \_ flag GPREL SCN image è solo per i file oggetto. quando questo tipo di sezione viene visualizzato in un file di immagine, il flag GPREL per l'immagine \_ SCN \_ non deve essere impostato. <br/>                             |
| . sxdata <br/>   | Dati del gestore eccezioni registrati (formato libero e solo x86/oggetto) <br/>                                                                                          | IMAGE \_ SCN \_ lnk \_ info contiene l'indice dei simboli di ognuno dei gestori di eccezioni a cui fa riferimento il codice nel file oggetto. Il simbolo può essere per un simbolo UNDEF o uno definito in tale modulo. <br/>                                                                                                                                                                     |
| text <br/>     | Codice eseguibile (formato libero) <br/>                                                                                                                                | IMAGE \_ SCN \_ CNT \_ codice \| Image \_ SCN \_ mem \_ Execute \| IIMAGE \_ SCN \_ mem \_ Read <br/>                                                                                                                                                                                                                                                                                                           |
| . TLS <br/>      | Archiviazione locale di thread (solo oggetto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| immagine SCN \_ \_ mem \_ lettura \| immagine \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . TLS $ <br/>     | Archiviazione locale di thread (solo oggetto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| immagine SCN \_ \_ mem \_ lettura \| immagine \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . vsdata <br/>   | GP-dati inizializzati relativi (formato libero e per le architetture ARM, SH4 e Thumb) <br/>                                                                    | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| immagine SCN \_ \_ mem \_ lettura \| immagine \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . XData <br/>    | Informazioni sull'eccezione (formato libero) <br/>                                                                                                                          | IMAGE \_ SCN \_ CNT \_ immagine \_ dei dati inizializzati \| \_ SCN \_ \_ lettura mem <br/>                                                                                                                                                                                                                                                                                                                           |



 

Alcune delle sezioni elencate di seguito sono contrassegnate come "solo oggetto" o "solo immagine" per indicare che la semantica speciale è pertinente solo per i file oggetto o i file di immagine, rispettivamente. Una sezione contrassegnata come "solo immagine" potrebbe essere ancora visualizzata in un file oggetto come modo per accedere al file di immagine, ma la sezione non ha un significato speciale per il linker, solo per il caricatore di file di immagine.

### <a name="the-debug-section"></a>Sezione. debug

La sezione. debug viene utilizzata nei file oggetto per contenere informazioni di debug generate dal compilatore e nei file di immagine per contenere tutte le informazioni di debug generate. In questa sezione viene descritta la creazione di pacchetti di informazioni di debug in file di immagine e di oggetto.

Nella sezione successiva viene descritto il formato della directory di debug, che può trovarsi in qualsiasi punto dell'immagine. Nelle sezioni successive vengono descritti i "gruppi" nei file oggetto contenenti informazioni di debug.

Il valore predefinito per il linker è che le informazioni di debug non sono mappate nello spazio degli indirizzi dell'immagine. Una sezione. debug esiste solo quando viene eseguito il mapping delle informazioni di debug nello spazio degli indirizzi.

#### <a name="debug-directory-image-only"></a>Directory di debug (solo immagine)

I file di immagine contengono una directory di debug facoltativa che indica il tipo di informazioni di debug presenti e la posizione in cui si trova. Questa directory è costituita da una matrice di voci della directory di debug la cui posizione e dimensione sono indicate nell'intestazione facoltativa image.

La directory di debug può trovarsi in una sezione. debug (se esistente), oppure può essere inclusa in qualsiasi altra sezione del file di immagine oppure non trovarsi in una sezione.

Ogni voce della directory di debug identifica la posizione e le dimensioni di un blocco di informazioni di debug. L'RVA specificato può essere zero se le informazioni di debug non sono coperte da un'intestazione di sezione, ovvero si trova nel file di immagine e non è mappato nello spazio degli indirizzi di run-time. Se viene mappato, RVA è il relativo indirizzo.

Una voce di directory di debug ha il formato seguente:



| Offset         | Dimensione          | Campo                        | Descrizione                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Caratteristiche <br/>  | Riservato, deve essere zero. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | Data e ora di creazione dei dati di debug. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | Numero di versione principale del formato dati di debug. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | Numero di versione secondario del formato dati di debug. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | Tipo <br/>             | Formato delle informazioni di debug. Questo campo consente il supporto di più debugger. Per ulteriori informazioni, vedere [tipo di debug](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | SizeOfData <br/>       | Dimensione dei dati di debug (esclusa la directory di debug). <br/>                                                                     |
| 20 <br/> | 4 <br/> | AddressOfRawData <br/> | Indirizzo dei dati di debug quando vengono caricati, relativi alla base dell'immagine. <br/>                                                                     |
| 24 <br/> | 4 <br/> | PointerToRawData <br/> | Puntatore di file ai dati di debug. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Tipo di debug

Per il campo tipo della voce della directory di debug vengono definiti i valori seguenti:



| Costante                                        | Valore          | Descrizione                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo di debug immagine \_ \_ sconosciuto <br/>         | 0 <br/>  | Valore sconosciuto ignorato da tutti gli strumenti. <br/>                                                                                                                                                       |
| \_tipo di debug immagine \_ \_ COFF <br/>            | 1 <br/>  | Informazioni di debug COFF (numeri di riga, tabella dei simboli e tabella di stringhe). Questo tipo di informazioni di debug è indicato anche dai campi nelle intestazioni dei file. <br/>                                          |
| \_tipo di debug immagine \_ \_ CodeView <br/>        | 2 <br/>  | Visual C++ informazioni di debug. <br/>                                                                                                                                                                    |
| \_tipo di debug immagine \_ \_ Polinesia <br/>             | 3 <br/>  | Informazioni sull'omissione dei puntatori ai frame (Polinesia). Queste informazioni indicano al debugger come interpretare stack frame non standard, che usano il registro EBP per uno scopo diverso da un puntatore a frame. <br/> |
| \_tipo di debug Image \_ \_ varie <br/>            | 4 <br/>  | Percorso del file DBG. <br/>                                                                                                                                                                            |
| \_ \_ eccezione tipo di debug immagine \_ <br/>       | 5 <br/>  | Una copia della sezione pData. <br/>                                                                                                                                                                            |
| \_ \_ correzione tipo di debug immagine \_ <br/>           | 6 <br/>  | Riservato. <br/>                                                                                                                                                                                            |
| IMAGE \_ debug \_ Type \_ OMAP \_ to \_ src <br/>   | 7 <br/>  | Mapping da un RVA nell'immagine a un RVA nell'immagine di origine. <br/>                                                                                                                                          |
| IMAGE \_ debug \_ Type \_ OMAP \_ da \_ src <br/> | 8 <br/>  | Mapping da un RVA nell'immagine di origine a un RVA nell'immagine. <br/>                                                                                                                                          |
| \_tipo di debug immagine \_ \_ Borland <br/>         | 9 <br/>  | Riservato per Borland. <br/>                                                                                                                                                                                |
| \_Tipo di debug immagine \_ \_ RESERVED10 <br/>      | 10 <br/> | Riservato. <br/>                                                                                                                                                                                            |
| \_tipo di debug immagine \_ \_ CLSID <br/>           | 11 <br/> | Riservato. <br/>                                                                                                                                                                                            |
| \_ripetizione del \_ tipo di debug immagine \_ <br/>           | 16 <br/> | Determinismo o riproducibilità PE. <br/>                                                                                                                                                                   |
| \_tipo di debug immagine \_ \_ ex \_ DLLCHARACTERISTICS | 20 | Caratteristiche DLL estese bit. |



 

Se il campo tipo è impostato su IMAGE \_ debug \_ Type \_ polinesias, i dati non elaborati di debug sono una matrice in cui ogni membro descrive la stack frame di una funzione. Non tutte le funzioni nel file di immagine devono contenere informazioni per la Polinesia, anche se il tipo di debug è la Polinesia. Si presuppone che le funzioni che non dispongono di informazioni sulla Polinesia siano di stack frame normali. Il formato per le informazioni sulla Polinesia è il seguente:


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



La presenza di una voce di tipo immagine \_ debug \_ tipo \_ di riproduzione indica che il file PE è stato compilato in modo da ottenere il determinismo o la riproducibilità. Se l'input non viene modificato, il file PE di output sarà sicuramente di bit per bit identico, indipendentemente dal momento in cui viene generato il PE. Vari campi di data/ora nel file PE sono compilati con parte o tutti i bit di un valore hash calcolato che utilizza il contenuto del file PE come input e pertanto non rappresentano più la data e l'ora effettive in cui viene prodotto un file PE o dati specifici correlati all'interno del PE. I dati non elaborati di questa voce di debug possono essere vuoti oppure possono contenere un valore hash calcolato preceduto da un valore a quattro byte che rappresenta la lunghezza del valore hash.

Se il campo tipo è impostato su IMAGE \_ debug \_ Type \_ es \_ DLLCHARACTERISTICS, i dati non elaborati di debug contengono bit di caratteristiche dll estese, in aggiunta a quelli che possono essere impostati nell'intestazione facoltativa dell'immagine. Vedere le [caratteristiche della dll](#dll-characteristics) nella sezione [intestazione facoltativa Windows-Specific campi (solo immagine)](#optional-header-windows-specific-fields-image-only).

##### <a name="extended-dll-characteristics"></a>Caratteristiche DLL estese

I valori seguenti sono definiti per le caratteristiche DLL estese bit.

| Costante | Valore | Descrizione |
|-|-|-|
| IMMAGINE \_ DLLCHARACTERISTICS \_ ex \_ CET \_ compat | 0x0001 | Image è compatibile con CET. |

#### <a name="debugf-object-only"></a>. debug $ F (solo oggetto)

I dati in questa sezione sono stati sostituiti in Visual C++ versione 7,0 e versioni successive da un set più ampio di dati che viene emesso in una sottosezione **. debug $ S** .

I file oggetto possono contenere le sezioni. debug $ F il cui contenuto è uno o più \_ record di dati Polinesia (informazioni sull'omissione dei puntatori ai frame). Vedere l'argomento \_ relativo \_ \_ al tipo di debug delle immagini per la Polinesia nel tipo di [debug](#debug-type).

Il linker riconosce questi record **. debug $ F** . Se è in corso la generazione di informazioni di debug, il linker Ordina i \_ record di dati polinesiani per procedura RVA e genera una voce di directory di debug.

Il compilatore non deve generare record POLINESIAli per le procedure con formato frame standard.

#### <a name="debugs-object-only"></a>. debug $ S (solo oggetto)

Questa sezione contiene Visual C++ informazioni di debug (informazioni simboliche).

#### <a name="debugp-object-only"></a>. debug $ P (solo oggetto)

Questa sezione contiene Visual C++ informazioni di debug (informazioni precompilate). Si tratta di tipi condivisi tra tutti gli oggetti compilati utilizzando l'intestazione precompilata generata con questo oggetto.

#### <a name="debugt-object-only"></a>. debug $ T (solo oggetto)

Questa sezione contiene Visual C++ informazioni di debug (informazioni sul tipo).

#### <a name="linker-support-for-microsoft-debug-information"></a>Supporto del linker per le informazioni di debug Microsoft

Per supportare le informazioni di debug, il linker:

-   Raccoglie tutti i dati di debug pertinenti dalle sezioni **. debug $ F**, **debug $ S**, **. debug $ P** e **. debug $ T** .

-   Elabora i dati insieme alle informazioni di debug generate dal linker nel file PDB e crea una voce di directory di debug per farvi riferimento.

### <a name="the-drectve-section-object-only"></a>Sezione. drectve (solo oggetto)

Una sezione è una sezione di direttiva se dispone del \_ \_ \_ flag di info di SCN lnk impostato nell'intestazione della sezione e ha il nome della sezione **. drectve** . Il linker rimuove una sezione **. drectve** dopo l'elaborazione delle informazioni, quindi la sezione non viene visualizzata nel file di immagine che viene collegato.

Una sezione **. drectve** è costituita da una stringa di testo che può essere codificata come ANSI o UTF-8. Se il marcatore dell'ordine dei byte UTF-8 (BOM, un prefisso a tre byte costituito da 0xEF, 0xBB e 0xBF) non è presente, la stringa di direttiva viene interpretata come ANSI. La stringa di direttiva è una serie di opzioni del linker separate da spazi. Ogni opzione contiene un trattino, il nome dell'opzione e qualsiasi attributo appropriato. Se un'opzione contiene spazi, l'opzione deve essere racchiusa tra virgolette. La sezione **. drectve** non deve avere rilocazioni o numeri di riga.

### <a name="the-edata-section-image-only"></a>Sezione. edata (solo immagine)

La sezione Export data, denominata. edata, contiene informazioni sui simboli a cui altre immagini possono accedere tramite il collegamento dinamico. I simboli esportati si trovano in genere nelle DLL, ma le dll possono anche importare simboli.

Di seguito è riportata una panoramica della struttura generale della sezione Export. Le tabelle descritte sono in genere contigue nel file nell'ordine indicato (anche se non è obbligatorio). Per esportare i simboli come ordinali sono necessarie solo la tabella di esportazione della tabella e dell'indirizzo di esportazione. Un ordinale è un'esportazione a cui si accede direttamente dall'indice della tabella degli indirizzi di esportazione. Per supportare l'utilizzo dei nomi di esportazione, sono disponibili la tabella del puntatore dei nomi, la tabella ordinale e il nome di esportazione.



| Nome tabella                         | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esporta tabella directory <br/> | Tabella con una sola riga (a differenza della directory di debug). Questa tabella indica le posizioni e le dimensioni delle altre tabelle di esportazione. <br/>                                                                                                                                                                                                               |
| Esporta tabella indirizzi <br/>   | Matrice di RVA di simboli esportati. Questi sono gli indirizzi effettivi delle funzioni e dei dati esportati nel codice eseguibile e nelle sezioni di dati. Altri file di immagine possono importare un simbolo usando un indice in questa tabella (un numero ordinale) o, facoltativamente, usando il nome pubblico che corrisponde al numero ordinale se è definito un nome pubblico. <br/> |
| Tabella puntatore al nome <br/>     | Matrice di puntatori ai nomi di esportazione pubblici, ordinati in ordine crescente. <br/>                                                                                                                                                                                                                                                                    |
| Tabella ordinale <br/>          | Matrice di ordinali corrispondenti ai membri della tabella del puntatore del nome. La corrispondenza è in base alla posizione; Pertanto, la tabella del puntatore del nome e la tabella ordinale devono avere lo stesso numero di membri. Ogni ordinale è un indice nella tabella degli indirizzi di esportazione. <br/>                                                                        |
| Esporta tabella nome <br/>      | Serie di stringhe ASCII con terminazione null. I membri della tabella del puntatore del nome puntano a questa area. Questi nomi sono i nomi pubblici tramite i quali vengono importati ed esportati i simboli. non sono necessariamente uguali ai nomi privati utilizzati all'interno del file di immagine. <br/>                                                           |



 

Quando un altro file di immagine importa un simbolo in base al nome, il caricatore Win32 cerca una stringa corrispondente nella tabella del puntatore del nome. Se viene trovata una stringa corrispondente, l'ordinale associato viene identificato cercando il membro corrispondente nella tabella ordinale, ovvero il membro della tabella ordinale con lo stesso indice del puntatore di stringa trovato nella tabella del puntatore del nome. L'ordinale risultante è un indice nella tabella degli indirizzi di esportazione che fornisce la posizione effettiva del simbolo desiderato. È possibile accedere a ogni simbolo di esportazione tramite un ordinale.

Quando un altro file di immagine importa un simbolo in base al numero ordinale, non è necessario cercare una stringa corrispondente nella tabella del puntatore del nome. L'uso diretto di un ordinale è pertanto più efficiente. Tuttavia, un nome di esportazione è più semplice da ricordare e non richiede che l'utente conosca l'indice della tabella per il simbolo.

#### <a name="export-directory-table"></a>Esporta tabella directory

Le informazioni sui simboli di esportazione iniziano con la tabella export directory, che descrive il resto delle informazioni sui simboli di esportazione. La tabella directory di esportazione contiene informazioni sull'indirizzo utilizzate per risolvere le importazioni nei punti di ingresso all'interno dell'immagine.



| Offset         | Dimensione          | Campo                                | Descrizione                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Esporta flag <br/>             | Riservato, deve essere 0. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Indicatore di data e ora <br/>          | Data e ora di creazione dei dati di esportazione. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Versione principale <br/>            | Numero di versione principale. I numeri di versione principale e secondaria possono essere impostati dall'utente. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Versione secondaria <br/>            | Numero di versione secondario. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nome RVA <br/>                 | Indirizzo della stringa ASCII che contiene il nome della DLL. Questo indirizzo è relativo alla base dell'immagine. <br/>                                                |
| 16 <br/> | 4 <br/> | Base ordinale <br/>             | Numero ordinale iniziale per le esportazioni in questa immagine. Questo campo specifica il numero ordinale iniziale per la tabella degli indirizzi di esportazione. Viene in genere impostato su 1. <br/> |
| 20 <br/> | 4 <br/> | Voci della tabella di indirizzi <br/>    | Numero di voci nella tabella degli indirizzi di esportazione. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Numero di puntatori al nome <br/>  | Numero di voci nella tabella del puntatore del nome. Questo è anche il numero di voci nella tabella ordinale. <br/>                                                     |
| 28 <br/> | 4 <br/> | Esporta tabella indirizzi RVA <br/> | Indirizzo della tabella degli indirizzi di esportazione rispetto alla base dell'immagine. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | Puntatore al nome RVA <br/>         | Indirizzo della tabella dei puntatori del nome di esportazione rispetto alla base dell'immagine. Le dimensioni della tabella sono fornite dal campo numero di puntatori a nome. <br/>                       |
| 36 <br/> | 4 <br/> | RVA tabella ordinale <br/>        | Indirizzo della tabella ordinale, relativo alla base dell'immagine. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Esporta tabella indirizzi

La tabella degli indirizzi di esportazione contiene l'indirizzo dei punti di ingresso esportati e i dati esportati e gli assoluti. Un numero ordinale viene utilizzato come indice nella tabella degli indirizzi di esportazione.

Ogni voce nella tabella degli indirizzi di esportazione è un campo che usa uno dei due formati riportati nella tabella seguente. Se l'indirizzo specificato non si trova all'interno della sezione Export (come definito dall'indirizzo e dalla lunghezza indicati nell'intestazione facoltativa), il campo è un RVA di esportazione, ovvero un indirizzo effettivo nel codice o nei dati. In caso contrario, il campo è un RVA di server d'avanzamento, che assegna un nome a un simbolo in un'altra DLL.



| Offset        | Dimensione          | Campo                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Esporta RVA <br/>    | Indirizzo del simbolo esportato quando viene caricato in memoria rispetto alla base dell'immagine. Ad esempio, l'indirizzo di una funzione esportata. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | RVA server d'avanzamento <br/> | Puntatore a una stringa ASCII con terminazione null nella sezione Export. Questa stringa deve essere compresa nell'intervallo specificato dalla voce Esporta directory dati della tabella. Vedere [directory di dati intestazione facoltativa (solo immagine)](#optional-header-data-directories-image-only). Questa stringa restituisce il nome della DLL e il nome dell'esportazione (ad esempio, "MYDLL. expfunc") o il nome della DLL e il numero ordinale dell'esportazione, ad esempio "MYDLL. \# 27 "). <br/> |



 

Un server d'esportazione RVA esporta una definizione da un'altra immagine, facendo in modo che venga visualizzata come se venisse esportata dall'immagine corrente. Il simbolo viene quindi importato ed esportato simultaneamente.

Ad esempio, in Kernel32.dll in Windows XP, l'esportazione denominata "HeapAlloc" viene trasmessa alla stringa "NTDLL. RtlAllocateHeap." In questo modo, le applicazioni possono utilizzare il modulo specifico di Windows XP Ntdll.dll senza effettivamente contenere riferimenti all'importazione. La tabella di importazione dell'applicazione si riferisce solo a Kernel32.dll. Pertanto, l'applicazione non è specifica di Windows XP e può essere eseguita in qualsiasi sistema Win32.

#### <a name="export-name-pointer-table"></a>Esporta tabella puntatore al nome

La tabella puntatore al nome esportazione è una matrice di indirizzi (RVA) nella tabella dei nomi di esportazione. I puntatori sono 32 bit ciascuno e sono relativi alla base dell'immagine. I puntatori vengono ordinati in modo lessicale per consentire ricerche binarie.

Un nome di esportazione viene definito solo se la tabella del puntatore del nome esportazione contiene un puntatore a tale nome.

#### <a name="export-ordinal-table"></a>Esporta tabella ordinale

La tabella dell'ordinale di esportazione è una matrice di indici non distorta a 16 bit nella tabella degli indirizzi di esportazione. I numeri ordinali sono prepolarizzati dal campo ordinale di base della tabella di directory di esportazione. In altre parole, è necessario sottrarre la base ordinale dagli ordinali per ottenere gli indici reali nella tabella degli indirizzi di esportazione.

La tabella puntatore nome esportazione e la tabella ordinale di esportazione formano due matrici parallele separate per consentire l'allineamento del campo naturale. Queste due tabelle, in pratica, operano come una tabella, in cui la colonna del puntatore del nome esportazione punta a un nome pubblico (esportato) e la colonna ordinale di esportazione restituisce il numero ordinale corrispondente per tale nome pubblico. Un membro della tabella dei puntatori del nome di esportazione e un membro della tabella ordinale di esportazione sono associati alla stessa posizione (indice) nelle rispettive matrici.

Pertanto, quando viene eseguita la ricerca della tabella dei puntatori del nome di esportazione e viene trovata una stringa corrispondente nella posizione i, l'algoritmo per la ricerca dell'RVA del simbolo e dell'ordinale parziale è:

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Quando si esegue la ricerca di un simbolo in base all'ordinale (biased), l'algoritmo per trovare il nome RVA e il nome del simbolo è:

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Esporta tabella nome

La tabella nome esportazione contiene i dati di stringa effettivi a cui punta la tabella dei puntatori del nome di esportazione. Le stringhe in questa tabella sono nomi pubblici che possono essere usati da altre immagini per importare i simboli. Questi nomi di esportazione pubblici non sono necessariamente uguali ai nomi di simboli privati presenti nei simboli nel file di immagine e nel codice sorgente, anche se possono essere.

Ogni simbolo esportato ha un valore ordinale, che è solo l'indice nella tabella degli indirizzi di esportazione. L'utilizzo dei nomi di esportazione è tuttavia facoltativo. Alcuni, tutti o nessuno dei simboli esportati possono avere nomi di esportazione. Per i simboli esportati per i quali sono presenti nomi di esportazione, le voci corrispondenti nella tabella puntatore Esporta nome e nella tabella ordinale di esportazione interagiscono per associare ogni nome a un ordinale.

La struttura della tabella dei nomi di esportazione è una serie di stringhe ASCII con terminazione null di lunghezza variabile.

### <a name="the-idata-section"></a>Sezione. idata

Tutti i file di immagine che importano simboli, inclusi praticamente tutti i file eseguibili (EXE), hanno una sezione. idata. Di seguito è riportato un layout di file tipico per le informazioni di importazione:

-   Tabella directory

    Voce di directory null

-   Tabella di ricerca importazione DLL1

    Null

-   Tabella di ricerca importazione DLL2

    Null

-   Tabella di ricerca importazione DLL3

    Null

-   Tabella Hint-Name

#### <a name="import-directory-table"></a>Importa tabella directory

Le informazioni di importazione iniziano con la tabella Import directory, che descrive il resto delle informazioni di importazione. La tabella di importazione directory contiene informazioni sull'indirizzo utilizzate per risolvere i riferimenti di correzione ai punti di ingresso all'interno di un'immagine DLL. La tabella di importazione directory è costituita da una matrice di voci di directory di importazione, una voce per ogni DLL a cui fa riferimento l'immagine. L'ultima voce di directory è vuota (riempita con valori null), che indica la fine della tabella di directory.

Ogni voce di importazione directory ha il formato seguente:



| Offset         | Dimensione          | Campo                                                 | Descrizione                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Importa tabella di ricerca RVA (caratteristiche) <br/> | RVA della tabella di ricerca dell'importazione. Questa tabella contiene un nome o un ordinale per ogni importazione. Il nome "caratteristiche" viene usato in Winnt. h, ma non descrive più questo campo. <br/> |
| 4 <br/>  | 4 <br/> | Indicatore di data e ora <br/>                           | Timbro impostato su zero fino a quando l'immagine non è associata. Dopo che l'immagine è stata associata, questo campo viene impostato sull'indicatore di data/ora della DLL. <br/>                                          |
| 8 <br/>  | 4 <br/> | Catena d'inoltri <br/>                           | Indice del primo riferimento al server di riferimento. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Nome RVA <br/>                                  | Indirizzo di una stringa ASCII che contiene il nome della DLL. Questo indirizzo è relativo alla base dell'immagine. <br/>                                                                   |
| 16 <br/> | 4 <br/> | Importa tabella indirizzi RVA (tabella thunk) <br/>    | RVA della tabella degli indirizzi di importazione. Il contenuto di questa tabella è identico al contenuto della tabella di ricerca dell'importazione fino a quando l'immagine non è associata. <br/>                              |



 

#### <a name="import-lookup-table"></a>Importa tabella di ricerca

Una tabella di ricerca di importazione è una matrice di numeri a 32 bit per PE32 o una matrice di numeri a 64 bit per PE32 +. Ogni voce usa il formato di campo di bit descritto nella tabella seguente. In questo formato, il bit 31 è il bit più significativo per PE32 e bit 63 è il bit più significativo per PE32 +. La raccolta di queste voci descrive tutte le importazioni da una determinata DLL. L'ultima voce è impostata su zero (NULL) per indicare la fine della tabella.



| Bit/i            | Dimensione           | Campo di bit                       | Descrizione                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Flag ordinale/nome <br/>   | Se questo bit è impostato, importa in base al numero ordinale. In caso contrario, importare in base al nome. Bit viene mascherato come 0x80000000 per PE32, 0x8000000000000000 per PE32 +. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Numero ordinale <br/>      | Numero ordinale a 16 bit. Questo campo viene utilizzato solo se il campo di bit del flag ordinale/nome è 1 (importazione in base al numero ordinale). BITS 30-15 o 62-15 deve essere 0. <br/>                  |
| 30-0 <br/>  | 31 <br/> | Hint/nome tabella RVA <br/> | RVA a 31 bit di una voce di tabella hint/Name. Questo campo viene utilizzato solo se il campo di bit del flag ordinale/nome è 0 (importa per nome). Per PE32 + bits 62-31 deve essere zero. <br/> |



 

#### <a name="hintname-table"></a>Tabella di hint/nomi

Una tabella hint/Name è sufficiente per l'intera sezione Import. Ogni voce nella tabella hint/Name presenta il formato seguente:



| Offset         | Dimensione                 | Campo            | Descrizione                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Hint <br/> | Indice nella tabella del puntatore al nome dell'esportazione. Una corrispondenza viene tentata prima con questo valore. In caso di errore, viene eseguita una ricerca binaria sulla tabella del puntatore del nome di esportazione della DLL. <br/>            |
| 2 <br/>  | Variabile <br/> | Nome <br/> | Stringa ASCII che contiene il nome da importare. Si tratta della stringa che deve essere confrontata con il nome pubblico nella DLL. Questa stringa fa distinzione tra maiuscole e minuscole e termina con un byte null. <br/> |
| \* <br/> | 0 o 1 <br/>   | Pad <br/>  | Byte finale con riempimento zero visualizzato dopo il byte finale null, se necessario, per allineare la voce successiva su un limite pari. <br/>                                                        |



 

#### <a name="import-address-table"></a>Importa tabella indirizzi

La struttura e il contenuto della tabella degli indirizzi di importazione sono identici a quelli della tabella di ricerca dell'importazione, fino a quando il file non viene associato. Durante l'associazione, le voci della tabella degli indirizzi di importazione vengono sovrascritte con gli indirizzi 32 bit (per PE32) o 64 bit (per PE32 +) dei simboli che vengono importati. Questi indirizzi sono gli indirizzi di memoria effettivi dei simboli, sebbene tecnicamente siano ancora detti "indirizzi virtuali". Il caricatore elabora in genere l'associazione.

### <a name="the-pdata-section"></a>Sezione. pData

La sezione. pData contiene una matrice di voci della tabella di funzioni utilizzate per la gestione delle eccezioni. A cui fa riferimento la voce della tabella di eccezione nella directory dei dati dell'immagine. Le voci devono essere ordinate in base agli indirizzi delle funzioni (il primo campo in ogni struttura) prima di essere emesse nell'immagine finale. La piattaforma di destinazione determina quale delle tre variazioni di formato della voce della tabella di funzione descritte di seguito viene utilizzata.

Per le immagini MIPS a 32 bit, le voci della tabella funzioni hanno il formato seguente:



| Offset         | Dimensione          | Campo                          | Descrizione                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Indirizzo iniziale <br/>      | Il VA della funzione corrispondente. <br/>                              |
| 4 <br/>  | 4 <br/> | Indirizzo finale <br/>        | Il VA della fine della funzione. <br/>                                 |
| 8 <br/>  | 4 <br/> | Gestore eccezioni <br/>  | Puntatore al gestore di eccezioni da eseguire. <br/>               |
| 12 <br/> | 4 <br/> | Dati del gestore <br/>       | Puntatore a informazioni aggiuntive da passare al gestore. <br/> |
| 16 <br/> | 4 <br/> | Indirizzo finale prologo <br/> | Il VA della fine del prologo della funzione. <br/>                        |



 

Per le piattaforme Windows CE ARM, PowerPC, SH3 e SH4, le voci della tabella di funzioni hanno il formato seguente:



| Offset        | Dimensione                | Campo                       | Descrizione                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | Indirizzo iniziale <br/>   | Il VA della funzione corrispondente. <br/>                                                                         |
| 4 <br/> | 8 bit <br/>  | Lunghezza prologo <br/>   | Il numero di istruzioni nel prologo della funzione. <br/>                                                          |
| 4 <br/> | 22 bit <br/> | Lunghezza funzione <br/> | Numero di istruzioni nella funzione. <br/>                                                                   |
| 4 <br/> | 1 bit <br/>   | Flag a 32 bit <br/>     | Se impostata, la funzione è costituita da istruzioni a 32 bit. Se è deselezionata, la funzione è costituita da istruzioni a 16 bit. <br/> |
| 4 <br/> | 1 bit <br/>   | Flag di eccezione <br/>  | Se impostato, esiste un gestore di eccezioni per la funzione. In caso contrario, non esiste alcun gestore di eccezioni. <br/>                 |



 

Per le piattaforme x64 e Itanium, le voci della tabella funzioni hanno il formato seguente:



| Offset        | Dimensione          | Campo                          | Descrizione                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | Indirizzo iniziale <br/>      | RVA della funzione corrispondente. <br/> |
| 4 <br/> | 4 <br/> | Indirizzo finale <br/>        | RVA della fine della funzione. <br/>    |
| 8 <br/> | 4 <br/> | Informazioni di rimozione <br/> | RVA delle informazioni di rimozione. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>Sezione. reloc (solo immagine)

La tabella di rilocazione di base contiene le voci per tutte le rilocazioni di base nell'immagine. Il campo della tabella di rilocazione di base nelle directory dei dati di intestazione facoltative indica il numero di byte nella tabella di rilocazione di base. Per altre informazioni, vedere [directory di dati di intestazione facoltativa (solo immagine)](#optional-header-data-directories-image-only). La tabella di rilocazione di base è divisa in blocchi. Ogni blocco rappresenta le rilocazioni di base per una pagina 4K. Ogni blocco deve iniziare con un limite di 32 bit.

Il caricatore non è necessario per elaborare le rilocazioni di base che vengono risolte dal linker, a meno che non sia possibile caricare l'immagine di caricamento nella base dell'immagine specificata nell'intestazione PE.

#### <a name="base-relocation-block"></a>Blocco di rilocazione di base

Ogni blocco di rilocazione di base inizia con la struttura seguente:



| Offset        | Dimensione          | Campo                  | Descrizione                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | RVA pagina <br/>   | La base dell'immagine più l'RVA della pagina viene aggiunta a ogni offset per creare il VA in cui deve essere applicata la rilocazione di base. <br/>                         |
| 4 <br/> | 4 <br/> | Dimensione blocco <br/> | Il numero totale di byte nel blocco di rilocazione di base, inclusi i campi RVA pagina e dimensioni blocco e i campi tipo/offset che seguono. <br/> |



 

Il campo dimensione blocco viene seguito da un numero qualsiasi di voci di campo tipo o offset. Ogni voce è costituita da una parola (2 byte) e presenta la struttura seguente:



| Offset        | Dimensione                | Campo              | Descrizione                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 bit <br/>  | Tipo <br/>   | Memorizzato nei 4 bit massimi della parola, un valore che indica il tipo di rilocazione di base da applicare. Per altre informazioni, vedere [tipi di rilocazione di base](#base-relocation-types).<br/>                         |
| 0 <br/> | 12 bit <br/> | Offset <br/> | Archiviati nei restanti 12 bit della parola, un offset dall'indirizzo iniziale specificato nel campo RVA della pagina per il blocco. Questo offset specifica dove deve essere applicata la rilocazione di base. <br/> |



 

Per applicare una rilocazione di base, la differenza viene calcolata tra l'indirizzo di base preferito e la base in cui l'immagine viene effettivamente caricata. Se l'immagine viene caricata nella base preferita, la differenza è zero e pertanto non è necessario applicare le rilocazioni di base.

#### <a name="base-relocation-types"></a>Tipi di rilocazione di base



| Costante                                       | Valore          | Descrizione                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMMAGINE \_ \_ assoluta basata su rel \_ <br/>        | 0 <br/>  | La rilocazione di base viene ignorata. Questo tipo può essere utilizzato per riempire un blocco. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ rel \_ basato su \_ High <br/>            | 1 <br/>  | La rilocazione di base aggiunge i 16 bit alti della differenza al campo a 16 bit in corrispondenza dell'offset. Il campo a 16 bit rappresenta il valore massimo di una parola a 32 bit. <br/>                                                                                                                                                               |
| IMMAGINE \_ \_ con base rel \_ bassa <br/>             | 2 <br/>  | La rilocazione di base aggiunge i 16 bit bassi della differenza al campo a 16 bit in corrispondenza dell'offset. Il campo a 16 bit rappresenta la metà inferiore di una parola a 32 bit. <br/>                                                                                                                                                                  |
| \_ \_ HIGHLOW basato su immagine rel \_ <br/>         | 3 <br/>  | La rilocazione di base applica tutti i 32 bit della differenza al campo a 32 bit in corrispondenza dell'offset. <br/>                                                                                                                                                                                                                              |
| \_ \_ HIGHADJ basato su immagine rel \_ <br/>         | 4 <br/>  | La rilocazione di base aggiunge i 16 bit alti della differenza al campo a 16 bit in corrispondenza dell'offset. Il campo a 16 bit rappresenta il valore massimo di una parola a 32 bit. I 16 bit bassi del valore a 32 bit vengono archiviati nella parola a 16 bit che segue questa rilocazione di base. Questo significa che questa rilocazione di base occupa due slot. <br/> |
| \_ \_ JMPADDR MIPS basato su immagine rel \_ \_ <br/>   | 5 <br/>  | L'interpretazione di rilocazione dipende dal tipo di computer. <br/> Quando il tipo di computer è MIPS, la rilocazione di base si applica a un'istruzione Jump MIPS. <br/>                                                                                                                                                    |
| \_ \_ MOV32 ARM basato su immagine rel \_ \_ <br/>      | 5 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è ARM o Thumb. La rilocazione di base applica l'indirizzo a 32 bit di un simbolo in una coppia di istruzioni MOVW/MOVT consecutive. <br/>                                                                                                                                 |
| \_ \_ HIGH20 RISCV basato su immagine rel \_ \_ <br/>   | 5 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è RISC-V. La rilocazione di base si applica ai 20 bit alti di un indirizzo assoluto a 32 bit. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Riservato, deve essere zero. <br/>                                                                                                                                                                                                                                                                                               |
| \_ \_ MOV32 Thumb basato su immagine rel \_ \_ <br/>    | 7 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è Thumb. La rilocazione di base applica l'indirizzo a 32 bit di un simbolo a una coppia di istruzioni MOVW/MOVT consecutive. <br/>                                                                                                                                            |
| \_ \_ LOW12I RISCV basato su immagine rel \_ \_ <br/>   | 7 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è RISC-V. La rilocazione di base si applica ai 12 bit inferiori di un indirizzo assoluto a 32 bit formato nel formato di istruzione RISC-V I-Type. <br/>                                                                                                                           |
| \_ \_ LOW12S RISCV basato su immagine rel \_ \_ <br/>   | 8 <br/>  | Questa rilocazione è significativa solo quando il tipo di computer è RISC-V. La rilocazione di base si applica ai 12 bit inferiori di un indirizzo assoluto a 32 bit formato dal formato di istruzione RISC-V S-Type. <br/>                                                                                                                           |
| \_ \_ JMPADDR16 MIPS basato su immagine rel \_ \_ <br/> | 9 <br/>  | La rilocazione è significativa solo quando il tipo di computer è MIPS. La rilocazione di base si applica a un'istruzione MIPS16 Jump. <br/>                                                                                                                                                                                            |
| \_ \_ DIR64 basato su immagine rel \_ <br/>           | 10 <br/> | La rilocazione di base applica la differenza al campo a 64 bit in corrispondenza dell'offset. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>Sezione. TLS

La sezione. TLS fornisce supporto PE e COFF diretti per l'archiviazione locale di thread statici (TLS). TLS è una classe di archiviazione speciale supportata da Windows in cui un oggetto dati non è una variabile automatica (stack), ma è locale per ogni singolo thread che esegue il codice. Pertanto, ogni thread può mantenere un valore diverso per una variabile dichiarata usando TLS.

Si noti che è possibile supportare qualsiasi quantità di dati TLS usando le chiamate API TlsAlloc, TlsFree, TlsSetValue e TlsGetValue. L'implementazione di PE o COFF è un approccio alternativo all'uso dell'API e ha il vantaggio di essere più semplice dal punto di vista del programmatore in linguaggio alto. Questa implementazione consente di definire e inizializzare i dati TLS in modo analogo alle normali variabili statiche in un programma. Ad esempio, in Visual C++, una variabile TLS statica può essere definita come indicato di seguito, senza usare l'API Windows:

`__declspec (thread) int tlsFlag = 1;`

Per supportare questo costrutto di programmazione, la sezione PE e COFF. TLS specifica le informazioni seguenti: dati di inizializzazione, routine di callback per l'inizializzazione e la terminazione per thread e l'indice TLS, descritti nella discussione seguente.

> [!Note]
>
> Gli oggetti dati TLS dichiarati in modo statico possono essere usati solo nei file di immagine caricati in modo statico. Questo fatto rende non affidabile l'uso di dati TLS statici in una DLL, a meno che non si sia certi che la DLL o qualsiasi elemento collegato in modo statico non venga mai caricato dinamicamente con la funzione API LoadLibrary.

 

Il codice eseguibile accede a un oggetto dati TLS statico mediante i passaggi seguenti:

1.  Al momento del collegamento, il linker imposta l'indirizzo del campo indice della directory TLS. Questo campo punta a una posizione in cui il programma prevede di ricevere l'indice TLS.

    La libreria di runtime Microsoft semplifica questo processo definendo un'immagine di memoria della directory TLS e assegnando al nome speciale " \_ \_ TLS \_ usato" (piattaforme Intel x86) o " \_ TLS \_ usato" (altre piattaforme). Il linker cerca questa immagine di memoria e usa i dati disponibili per creare la directory TLS. Altri compilatori che supportano TLS e lavorano con Microsoft linker devono usare questa stessa tecnica.

2.  Quando viene creato un thread, il caricatore comunica l'indirizzo della matrice TLS del thread inserendo l'indirizzo del blocco dell'ambiente di thread (TEB) nel registro FS. Un puntatore alla matrice TLS è in corrispondenza dell'offset di 0x2C dall'inizio di TEB. Questo comportamento è specifico di Intel x86.

3.  Il caricatore assegna il valore dell'indice TLS alla posizione indicata dall'indirizzo del campo index.

4.  Il codice eseguibile recupera l'indice TLS e anche il percorso della matrice TLS.

5.  Il codice usa l'indice TLS e la posizione della matrice TLS (moltiplicando l'indice per 4 e usandolo come offset per la matrice) per ottenere l'indirizzo dell'area dati TLS per il programma e il modulo specificati. Ogni thread dispone di una propria area dati TLS, ma ciò è trasparente per il programma, che non deve essere in grado di stabilire come vengono allocati i dati per i singoli thread.

6.  È possibile accedere a un singolo oggetto dati TLS come un offset fisso nell'area dati TLS.

La matrice TLS è una matrice di indirizzi gestiti dal sistema per ogni thread. Ogni indirizzo in questa matrice fornisce il percorso dei dati TLS per un modulo specifico (EXE o DLL) all'interno del programma. L'indice TLS indica il membro della matrice da usare. L'indice è un numero (significativo solo per il sistema) che identifica il modulo.

#### <a name="the-tls-directory"></a>Directory TLS

La directory TLS ha il formato seguente:



| Offset (PE32/PE32 +) | Dimensioni (PE32/PE32 +) | Campo                            | Descrizione                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | Avvio dati non elaborati VA <br/>    | Indirizzo iniziale del modello TLS. Il modello è un blocco di dati utilizzato per inizializzare i dati TLS. Il sistema copia tutti i dati ogni volta che viene creato un thread, quindi non deve essere danneggiato. Si noti che questo indirizzo non è un RVA; si tratta di un indirizzo per il quale deve essere presente una rilocazione di base nella sezione. reloc. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | Fine dati RAW VA <br/>      | Indirizzo dell'ultimo byte di TLS, ad eccezione del riempimento zero. Come per il campo Raw Data Start VA, si tratta di un VA, non di un RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Indirizzo dell'indice <br/>     | Posizione in cui ricevere l'indice TLS, assegnato dal caricatore. Questo percorso si trova in una sezione di dati ordinaria, quindi è possibile assegnare un nome simbolico accessibile al programma. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Indirizzo dei callback <br/> | Puntatore a una matrice di funzioni di callback TLS. La matrice è con terminazione null, pertanto se non è supportata alcuna funzione di callback, questo campo punta a 4 byte impostati su zero. Per informazioni sul prototipo di queste funzioni, vedere [funzioni di callback TLS](#tls-callback-functions).<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Dimensioni riempimento zero <br/>    | Dimensioni in byte del modello, oltre ai dati inizializzati delimitati dai campi dati non elaborati avvia VA e fine dati non elaborati. Le dimensioni totali del modello devono corrispondere alle dimensioni totali dei dati TLS nel file di immagine. Il riempimento zero è la quantità di dati che viene eseguita dopo i dati non zero inizializzati. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Caratteristiche <br/>      | I quattro bit \[ 23:20 \] descrivono le informazioni di allineamento. I valori possibili sono quelli definiti come IMAGE \_ SCN \_ align \_ \* , che vengono usati anche per descrivere l'allineamento della sezione nei file oggetto. Gli altri 28 bit sono riservati per un uso futuro. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>Funzioni di callback TLS

Il programma può fornire una o più funzioni di callback TLS per supportare l'inizializzazione e la terminazione aggiuntive per gli oggetti dati TLS. Un uso tipico di tale funzione di callback consiste nel chiamare i costruttori e i distruttori per gli oggetti.

Anche se in genere non è presente più di una funzione di callback, un callback viene implementato come una matrice per consentire l'aggiunta di altre funzioni di callback, se lo si desidera. Se è presente più di una funzione di callback, ogni funzione viene chiamata nell'ordine in cui l'indirizzo viene visualizzato nella matrice. Un puntatore null termina la matrice. È perfettamente valido avere un elenco vuoto (nessun callback supportato), nel qual caso la matrice di callback ha un solo membro, ovvero un puntatore null.

Il prototipo per una funzione di callback (a cui fa riferimento un puntatore di tipo \_ callback TLS PIMAGE \_ ) ha gli stessi parametri di una funzione del punto di ingresso della dll:


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



Il parametro riservato deve essere impostato su zero. Il parametro reason può assumere i valori seguenti:



| Impostazione                          | Valore         | Descrizione                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| \_connessione processo \_ dll <br/> | 1 <br/> | È stato avviato un nuovo processo, incluso il primo thread. <br/>                                   |
| \_connessione thread \_ dll <br/>  | 2 <br/> | È stato creato un nuovo thread. Questa notifica è stata inviata per tutti tranne il primo thread. <br/>      |
| \_ \_ scollegamento thread dll <br/>  | 3 <br/> | Un thread sta per terminare. Questa notifica è stata inviata per tutti tranne il primo thread. <br/> |
| \_ \_ scollegamento processo dll <br/> | 0 <br/> | Un processo sta per terminare, incluso il thread originale. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>Struttura di configurazione di caricamento (solo immagine)

La struttura di configurazione del carico (directory di configurazione del \_ caricamento immagine \_ \_ ) è stata usata in precedenza in casi molto limitati nel sistema operativo Windows NT per descrivere le varie funzionalità troppo complesse o troppo grandi da descrivere nell'intestazione del file o nell'intestazione facoltativa dell'immagine. Le versioni correnti di Microsoft linker e Windows XP e versioni successive di Windows usano una nuova versione di questa struttura per sistemi basati su x86 a 32 bit che includono la tecnologia SEH riservata. Viene fornito un elenco di gestori di eccezioni strutturati sicuri utilizzati dal sistema operativo durante l'invio delle eccezioni. Se l'indirizzo del gestore risiede nell'intervallo di i/o di un'immagine ed è contrassegnato come riservato SEH-Aware (ovvero IMAGE \_ DLLCHARACTERISTICS \_ No \_ SEH is clear nel campo DLLCHARACTERISTICS dell'intestazione facoltativa, come descritto in precedenza), il gestore deve trovarsi nell'elenco dei gestori sicuri noti per tale immagine. In caso contrario, il sistema operativo termina l'applicazione. Ciò consente di evitare l'exploit del "gestore di eccezioni x86" che è stato usato in passato per assumere il controllo del sistema operativo.

Microsoft linker fornisce automaticamente una struttura di configurazione del carico predefinita per includere i dati SEH riservati. Se il codice utente fornisce già una struttura di configurazione del carico, deve includere i nuovi campi SEH riservati. In caso contrario, il linker non può includere i dati SEH riservati e l'immagine non è contrassegnata come contenente SEH riservata.

#### <a name="load-configuration-directory"></a>Carica directory di configurazione

La voce della directory dei dati per una struttura di configurazione del caricamento SEH pre-riservata deve specificare una determinata dimensione della struttura di configurazione del carico, perché il caricatore del sistema operativo prevede sempre un determinato valore. In questo senso, le dimensioni sono in realtà solo un controllo della versione. Per la compatibilità con Windows XP e le versioni precedenti di Windows, le dimensioni devono essere 64 per le immagini x86.

#### <a name="load-configuration-layout"></a>Carica layout di configurazione

La struttura di configurazione load presenta il layout seguente per i file PE a 32 bit e a 64 bit:



| Offset              | Dimensione            | Campo                                      | Descrizione                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Caratteristiche <br/>                | Flag che indicano gli attributi del file, attualmente non utilizzati. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Valore dell'indicatore di data e ora. Il valore è rappresentato dal numero di secondi trascorsi dalla mezzanotte (00:00:00), dal 1 ° gennaio 1970, dall'ora UTC (Universal Coordinated Time), in base al clock di sistema. Il timestamp può essere stampato usando la funzione ora del runtime C (CRT). <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Numero di versione principale. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Numero di versione secondario. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | GlobalFlagsClear <br/>               | Flag del caricatore globale da cancellare per questo processo quando il caricatore avvia il processo. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | GlobalFlagsSet <br/>                 | Flag del caricatore globale da impostare per questo processo quando il caricatore avvia il processo. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | CriticalSectionDefaultTimeout <br/>  | Valore di timeout predefinito da utilizzare per le sezioni critiche di questo processo abbandonate. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | DeCommitFreeBlockThreshold <br/>     | Memoria che deve essere liberata prima che venga restituita al sistema, in byte. <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | DeCommitTotalFreeThreshold <br/>     | Quantità totale di memoria libera, in byte. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | LockPrefixTable <br/>                | \[x86 solo \] il va di un elenco di indirizzi in cui viene usato il prefisso di blocco in modo che possano essere sostituiti con NOP in computer a processore singolo. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | MaximumAllocationSize <br/>          | Dimensioni massime di allocazione, in byte. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | VirtualMemoryThreshold <br/>         | Dimensioni massime della memoria virtuale, in byte. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | ProcessAffinityMask <br/>            | L'impostazione di questo campo su un valore diverso da zero equivale alla chiamata di SetProcessAffinityMask con questo valore durante l'avvio del processo (solo con estensione exe) <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | ProcessHeapFlags <br/>               | Elaborare i flag dell'heap che corrispondono al primo argomento della funzione HeapCreate. Questi flag si applicano all'heap dei processi creato durante l'avvio del processo. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | Identificatore della versione del Service Pack. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Riservato <br/>                       | Deve essere zero. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | Editor <br/>                       | Riservato per l'utilizzo da parte del sistema. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | SecurityCookie <br/>                 | Puntatore a un cookie utilizzato dall'implementazione Visual C++ o GS. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | SEHandlerTable <br/>                 | \[x86 solo \] il va della tabella ordinata di RVA di ogni gestore di se valido e univoco nell'immagine. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | SEHandlerCount <br/>                 | \[solo x86 \] numero di gestori univoci nella tabella. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | GuardCFCheckFunctionPointer <br/>    | Il puntatore della funzione di controllo della protezione del flusso di controllo è memorizzato. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | GuardCFDispatchFunctionPointer <br/> | Il puntatore per la funzione di recapito della Guard flusso di controllo è memorizzato. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | GuardCFFunctionTable <br/>           | Il VA della tabella ordinata di RVA di ogni funzione Guard del flusso di controllo nell'immagine. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | GuardCFFunctionCount <br/>           | Numero di RVA univoci nella tabella precedente. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | GuardFlags <br/>                     | Flag correlati Guard flusso di controllo. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | CodeIntegrity <br/>                  | Informazioni sull'integrità del codice. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryTable <br/> | La tabella che indica l'indirizzo di Guard flusso di controllo che ha effettuato la tabella IAT è archiviata. <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryCount <br/> | Numero di RVA univoci nella tabella precedente. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | GuardLongJumpTargetTable <br/>       | La tabella di destinazione della protezione del flusso di controllo VA a lungo. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | GuardLongJumpTargetCount <br/>       | Numero di RVA univoci nella tabella precedente. <br/>                                                                                                                                                                                                                                    |



 

Il campo GuardFlags contiene una combinazione di uno o più dei seguenti flag e sottocampi:

-   Il modulo esegue controlli di integrità del flusso di controllo utilizzando il supporto fornito dal sistema.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   Il modulo esegue controlli di integrità del flusso di controllo e di scrittura.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   Il modulo contiene metadati di destinazione del flusso di controllo validi.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   Il modulo non usa il cookie di sicurezza/GS.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   Il modulo supporta la IAT a caricamento ritardato di sola lettura.

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   DELAYLOAD importare la tabella nella propria sezione. didat (senza alcun altro elemento) che può essere liberamente riprotetta.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   Il modulo contiene informazioni di esportazione non riportate. Ciò deduce anche che la tabella IAT Address taken è presente anche nella configurazione load.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   Il modulo consente l'eliminazione delle esportazioni.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   Il modulo contiene informazioni sulla destinazione longjmp.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   Maschera per il sottocampo che contiene lo stride delle voci della tabella di funzioni Guard flusso di controllo, ovvero il numero aggiuntivo di byte per ogni voce di tabella.

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

Inoltre, l'intestazione Windows SDK Winnt. h definisce questa macro per la quantità di bit da spostare a destra del valore GuardFlags per giustificare il corretto funzionamento della tabella della funzione Guard flusso di controllo:

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>Sezione. rsrc

Le risorse vengono indicizzate da una struttura ad albero con ordinamento binario a più livelli. Il progetto generale può incorporare 2 \* \* 31 livelli. Per convenzione, tuttavia, Windows utilizza tre livelli:

<dl> Type  
Nome  
Linguaggio  
</dl>

Una serie di tabelle di directory delle risorse mette in correlazione tutti i livelli nel modo seguente: ogni tabella di directory è seguita da una serie di voci di directory che forniscono il nome o l'identificatore (ID) per tale livello (tipo, nome o livello di lingua) e un indirizzo di una descrizione dei dati o di un'altra tabella di directory. Se l'indirizzo punta a una descrizione dei dati, i dati sono foglia nell'albero. Se l'indirizzo punta a un'altra tabella di directory, la tabella elenca le voci di directory al livello successivo.

Il tipo, il nome e gli ID della lingua di un'foglia sono determinati dal percorso utilizzato dalle tabelle di directory per raggiungere la foglia. La prima tabella determina l'ID del tipo, la seconda tabella, a cui fa riferimento la voce della directory nella prima tabella, determina l'ID del nome e la terza tabella determina l'ID della lingua.

La struttura generale della sezione. rsrc è la seguente:



| Data                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabelle di directory delle risorse (e voci della directory delle risorse) <br/> | Una serie di tabelle, una per ogni gruppo di nodi nell'albero. Tutti i nodi di primo livello (tipo) sono elencati nella prima tabella. Le voci di questa tabella puntano a tabelle di secondo livello. Ogni albero di secondo livello ha lo stesso ID tipo, ma ID nome diversi. Gli alberi di terzo livello hanno gli stessi ID di tipo e nome ma con ID lingua differenti. <br/> Ogni singola tabella è immediatamente seguita dalle voci di directory, in cui ogni voce ha un nome o un identificatore numerico e un puntatore a una descrizione dei dati o a una tabella al livello inferiore successivo. <br/> |
| Stringhe di directory delle risorse <br/>                                 | Stringhe Unicode allineate a due byte, che vengono utilizzate come dati stringa a cui puntano voci di directory. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Descrizione dati della risorsa <br/>                                  | Matrice di record, a cui puntano le tabelle, che descrivono le dimensioni effettive e la posizione dei dati della risorsa. Questi record sono le foglie nell'albero della descrizione della risorsa. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Dati della risorsa <br/>                                              | Dati non elaborati della sezione delle risorse. Le informazioni sulle dimensioni e sulla posizione nel campo descrizioni dati risorse delimitano le singole aree dei dati della risorsa. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Tabella directory delle risorse

Ogni tabella di directory delle risorse ha il formato seguente. Questa struttura di dati deve essere considerata l'intestazione di una tabella perché la tabella è costituita effettivamente da voci di directory (descritte nella sezione 6.9.2, "voci della directory delle risorse") e questa struttura:



| Offset         | Dimensione          | Campo                              | Descrizione                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Caratteristiche <br/>        | Flag di risorsa. Questo campo è riservato per un utilizzo futuro. È attualmente impostata su zero. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Indicatore di data e ora <br/>        | Ora di creazione dei dati della risorsa da parte del compilatore di risorse. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Versione principale <br/>          | Numero di versione principale, impostato dall'utente. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Versione secondaria <br/>          | Numero di versione secondario, impostato dall'utente. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Numero di voci di nome <br/> | Numero di voci di directory immediatamente successive alla tabella che utilizzano stringhe per identificare il tipo, il nome o le voci della lingua (a seconda del livello della tabella). <br/> |
| 14 <br/> | 2 <br/> | Numero di voci ID <br/>   | Numero di voci di directory immediatamente successive alle voci di nome che utilizzano ID numerici per le voci relative a tipo, nome o lingua. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Voci della directory delle risorse

Le voci di directory costituiscono le righe di una tabella. Ogni voce della directory delle risorse ha il formato seguente. Se la voce è un nome o una voce ID è indicata dalla tabella directory delle risorse, che indica il numero di voci di nome e ID che seguono (tenere presente che tutte le voci di nome precedono tutte le voci di ID per la tabella). Tutte le voci della tabella sono ordinate in ordine crescente: le voci di nome per stringa con distinzione tra maiuscole e minuscole e le voci di ID per valore numerico. Gli offset sono relativi all'indirizzo nella \_ voce della directory della \_ \_ risorsa DataDirectory. Per altre informazioni, vedere [peering all'interno di PE: Panoramica del formato di file eseguibile di Win32 Portable](/previous-versions/ms809762(v=msdn.10)#pe-file-resources) .



| Offset        | Dimensione          | Campo                           | Descrizione                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Offset nome <br/>         | Offset di una stringa che fornisce il tipo, il nome o la voce dell'ID lingua, a seconda del livello della tabella. <br/>     |
| 0 <br/> | 4 <br/> | ID di tipo integer <br/>          | Intero A 32 bit che identifica il tipo, il nome o la voce di ID della lingua. <br/>                                   |
| 4 <br/> | 4 <br/> | Offset immissione dati <br/>   | Bit elevato 0. Indirizzo di una voce di dati della risorsa (foglia). <br/>                                                   |
| 4 <br/> | 4 <br/> | Offset sottodirectory <br/> | Bit alto 1. I 31 bit inferiori sono l'indirizzo di un'altra tabella di directory delle risorse, ovvero il livello successivo. <br/> |



 

#### <a name="resource-directory-string"></a>Stringa di directory delle risorse

L'area della stringa di directory delle risorse è costituita da stringhe Unicode, che sono allineate a parole. Queste stringhe vengono archiviate insieme dopo l'ultima voce di directory delle risorse e prima della prima voce di dati della risorsa. Questo consente di ridurre al minimo l'effetto di queste stringhe a lunghezza variabile nell'allineamento delle voci di directory a dimensione fissa. Ogni stringa di directory di risorsa ha il formato seguente:



| Offset        | Dimensione                 | Campo                      | Descrizione                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Length <br/>         | Dimensione della stringa, escluso il campo di lunghezza. <br/> |
| 2 <br/> | Variabile <br/> | Stringa Unicode <br/> | Dati della stringa Unicode a lunghezza variabile, allineati a parole. <br/>     |



 

#### <a name="resource-data-entry"></a>Immissione dati risorsa

Ogni voce relativa ai dati delle risorse descrive un'unità effettiva di dati non elaborati nell'area dati della risorsa. Una voce di dati delle risorse ha il formato seguente:



| Offset         | Dimensione          | Campo                            | Descrizione                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | RVA dati <br/>             | Indirizzo di un'unità di dati della risorsa nell'area dati della risorsa. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Dimensione <br/>                 | Dimensione, in byte, dei dati della risorsa a cui fa riferimento il campo RVA dei dati. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | Tabella codici utilizzata per decodificare i valori dei punti di codice all'interno dei dati della risorsa. In genere, la tabella codici corrisponde alla tabella codici Unicode. <br/> |
| 12 <br/> | 4 <br/> | Riservato, deve essere 0. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>Sezione. cormeta (solo oggetto)

I metadati CLR vengono archiviati in questa sezione. Viene utilizzato per indicare che il file oggetto contiene codice gestito. Il formato dei metadati non è documentato, ma può essere passato alle interfacce CLR per la gestione dei metadati.

### <a name="the-sxdata-section"></a>Sezione. sxdata

I gestori di eccezioni validi di un oggetto sono elencati nella sezione **. sxdata** di tale oggetto. La sezione è contrassegnata come IMAGE \_ SCN \_ lnk \_ info. Contiene l'indice del simbolo COFF di ogni gestore valido, usando 4 byte per indice.

Inoltre, il compilatore contrassegna un oggetto COFF come SEH registrato creando il simbolo assoluto " @feat.00 " con LSB del campo valore impostato su 1. Un oggetto COFF senza gestori SEH registrati avrà il @feat.00 simbolo "", ma nessuna sezione **. sxdata** .

## <a name="archive-library-file-format"></a>Formato file archivio (libreria)

- [Firma del file di archivio](#archive-file-signature)
- [Intestazioni membro archivio](#archive-member-headers)
- [Primo membro del linker](#first-linker-member)
- [Secondo membro del linker](#second-linker-member)
- [Membro longnames](#longnames-member)

Il formato di archivio COFF fornisce un meccanismo standard per archiviare raccolte di file oggetto. Queste raccolte sono comunemente chiamate librerie nella documentazione di programmazione.

I primi 8 byte di un archivio sono costituiti dalla firma del file. Il resto dell'archivio è costituito da una serie di membri dell'archivio, come indicato di seguito:

-   Il primo e il secondo membro sono "membri del linker". Ognuno di questi membri ha un proprio formato, come descritto nella sezione [Import Name Type](#import-name-type). In genere, un linker inserisce le informazioni in questi membri dell'archivio. I membri del linker contengono la directory dell'archivio.

-   Il terzo membro è il membro "longnames". Questo membro facoltativo è costituito da una serie di stringhe ASCII con terminazione null in cui ogni stringa è il nome di un altro membro dell'archivio.

-   Il resto dell'archivio è costituito da membri standard (file oggetto). Ognuno di questi membri contiene il contenuto di un file oggetto nel suo complesso.

Un'intestazione del membro Archive precede ogni membro. Nell'elenco seguente viene illustrata la struttura generale di un archivio:

-   Firma: "! &lt; Arch &gt; \\ n "
-   Intestazione

    <dl> primo membro del linker  
    </dl>

-   Intestazione

    <dl> 2 ° membro del linker  
    </dl>

-   Intestazione

    <dl> Membro longnames  
    </dl>

-   Intestazione

    <dl> Contenuto del file OBJ 1  
    (Formato COFF)  
    </dl>

-   Intestazione

    <dl> Contenuto del file OBJ 2  
    (Formato COFF)  
    </dl>

### <a name="archive-file-signature"></a>Firma del file di archivio

La firma del file di archivio identifica il tipo di file. Qualsiasi utilità (ad esempio, un linker) che accetta un file di archivio come input può controllare il tipo di file leggendo questa firma. La firma è costituita dai caratteri ASCII seguenti, in cui ogni carattere riportato di seguito viene rappresentato letteralmente, ad eccezione del carattere di nuova riga ( \\ n):

`!<arch>\n`

### <a name="archive-member-headers"></a>Intestazioni membro archivio

Ogni membro (linker, longnames o membro del file oggetto) è preceduto da un'intestazione. Un'intestazione del membro Archive presenta il formato seguente, in cui ogni campo è una stringa di testo ASCII che rimane giustificata e riempita con spazi fino alla fine del campo. Nessun carattere di terminazione null in uno di questi campi.

Ogni intestazione del membro viene avviata sul primo indirizzo anche dopo la fine del membro dell'archivio precedente.



| Offset         | Dimensione           | Campo                     | Descrizione                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Nome <br/>          | Nome del membro di archivio con una barra (/) aggiunta per terminare il nome. Se il primo carattere è una barra, il nome ha un'interpretazione speciale, come descritto nella tabella seguente. <br/> |
| 16 <br/> | 12 <br/> | Data <br/>          | Data e ora in cui è stato creato il membro dell'archivio: questa è la rappresentazione decimale ASCII del numero di secondi a partire da 1/1/1970 dotto. <br/>                                                    |
| 28 <br/> | 6 <br/>  | ID utente <br/>       | Rappresentazione decimale ASCII dell'ID utente. Questo campo non contiene un valore significativo nelle piattaforme Windows perché gli strumenti Microsoft emettono tutti gli spazi vuoti. <br/>                                    |
| 34 <br/> | 6 <br/>  | ID gruppo <br/>      | Rappresentazione decimale ASCII dell'ID gruppo. Questo campo non contiene un valore significativo nelle piattaforme Windows perché gli strumenti Microsoft emettono tutti gli spazi vuoti. <br/>                                   |
| 40 <br/> | 8 <br/>  | Modalità <br/>          | Rappresentazione ottale ASCII della modalità file del membro. Si tratta del valore della modalità ST della \_ funzione di runtime del linguaggio C \_ wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Dimensione <br/>          | Rappresentazione decimale ASCII della dimensione totale del membro Archive, esclusa la dimensione dell'intestazione. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Fine intestazione <br/> | I due byte nella stringa C "̃ \\ n" (0X60 0x0A). <br/>                                                                                                                                               |



 

Il campo nome dispone di uno dei formati indicati nella tabella seguente. Come indicato in precedenza, ciascuna di queste stringhe viene lasciata giustificata e riempita con spazi finali all'interno di un campo di 16 byte:



| Contenuto del campo del nome | Descrizione                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nome <br/>      | Nome del membro dell'archivio. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | Il membro Archive è uno dei due membri del linker. Entrambi i membri del linker hanno questo nome. <br/>                                                                                                                                                                                          |
| // <br/>         | Il membro Archive è il membro longnames, che è costituito da una serie di stringhe ASCII con terminazione null. Il membro longnames è il terzo membro dell'archivio ed è facoltativo. <br/>                                                                     |
| /n <br/>         | Il nome del membro dell'archivio si trova in corrispondenza dell'offset n all'interno del membro longnames. Il numero n è la rappresentazione decimale dell'offset. Ad esempio: "/26" indica che il nome del membro dell'archivio è posizionato a 26 byte oltre l'inizio del contenuto del membro longnames. <br/> |



 

### <a name="first-linker-member"></a>Primo membro del linker

Il nome del primo membro del linker è "/". Il primo membro del linker è incluso per la compatibilità con le versioni precedenti. Non viene usato dai linker correnti, ma il formato deve essere corretto. Questo membro del linker fornisce una directory di nomi di simboli, così come il secondo membro del linker. Per ogni simbolo, le informazioni indicano dove trovare il membro dell'archivio che contiene il simbolo.

Il primo membro del linker ha il formato seguente. Queste informazioni vengono visualizzate dopo l'intestazione:



| Offset         | Dimensione               | Campo                         | Descrizione                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Numero di simboli <br/> | Long senza segno che contiene il numero di simboli indicizzati. Questo numero è archiviato nel formato big-endian. Ogni membro del file oggetto definisce in genere uno o più simboli esterni. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Offset <br/>           | Matrice di offset di file per archiviare le intestazioni dei membri, in cui n è uguale al campo numero di simboli. Ogni numero nella matrice è un long senza segno archiviato nel formato big-endian. Per ogni simbolo denominato nella tabella di stringhe, l'elemento corrispondente nella matrice di offset fornisce la posizione del membro archivio che contiene il simbolo. <br/> |
| \* <br/> | \* <br/>     | Tabella di stringhe <br/>      | Serie di stringhe con terminazione null che denominano tutti i simboli presenti nella directory. Ogni stringa inizia immediatamente dopo il carattere null nella stringa precedente. Il numero di stringhe deve essere uguale al valore del campo numero di simboli. <br/>                                                                                                       |



 

Gli elementi nella matrice di offset devono essere disposti in ordine crescente. Questo fatto implica che i simboli nella tabella di stringhe devono essere disposti in base all'ordine dei membri dell'archivio. Ad esempio, tutti i simboli nel primo membro del file oggetto devono essere elencati prima dei simboli nel secondo file oggetto.

### <a name="second-linker-member"></a>Secondo membro del linker

Il secondo membro del linker ha il nome "/" come il primo membro del linker. Sebbene entrambi i membri del linker forniscano una directory di simboli e membri di archivio che li contengono, il secondo membro del linker viene usato in modo preferenziale per il primo da tutti i linker correnti. Il secondo membro del linker include i nomi dei simboli nell'ordine lessicale, che consente una ricerca più rapida in base al nome.

Il secondo membro ha il formato seguente. Queste informazioni vengono visualizzate dopo l'intestazione:



| Offset         | Dimensione               | Campo                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Numero di membri <br/> | Long senza segno che contiene il numero di membri dell'archivio. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* m <br/> | Offset <br/>           | Matrice di offset di file per archiviare le intestazioni dei membri, disposte in ordine crescente. Ogni offset è un oggetto long senza segno. Il numero m è uguale al valore del campo numero di membri. <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Numero di simboli <br/> | Long senza segno contenente il numero di simboli indicizzati. Ogni membro del file oggetto definisce in genere uno o più simboli esterni. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Indici <br/>           | Matrice di indici in base 1 (unsigned short) che mappa i nomi dei simboli per archiviare gli offset dei membri. Il numero n è uguale al campo numero di simboli. Per ogni simbolo denominato nella tabella di stringhe, l'elemento corrispondente nella matrice indici fornisce un indice nella matrice degli offset. La matrice degli offset, a sua volta, fornisce la posizione del membro archivio che contiene il simbolo. <br/> |
| \* <br/> | \* <br/>     | Tabella di stringhe <br/>      | Serie di stringhe con terminazione null che denominano tutti i simboli presenti nella directory. Ogni stringa inizia immediatamente dopo il byte null nella stringa precedente. Il numero di stringhe deve essere uguale al valore del campo numero di simboli. Questa tabella elenca tutti i nomi di simboli in ordine lessicale crescente. <br/>                                                                             |



 

### <a name="longnames-member"></a>Membro longnames

Il nome del membro longnames è "//". Il membro longnames è una serie di stringhe di nomi di membri dell'archivio. Qui viene visualizzato un nome solo se lo spazio disponibile nel campo nome è insufficiente (16 byte). Il membro longnames è facoltativo. Può essere vuota solo con un'intestazione oppure può essere completamente assente senza neanche un'intestazione.

Le stringhe sono con terminazione null. Ogni stringa inizia immediatamente dopo il byte null nella stringa precedente.

## <a name="import-library-format"></a>Importa formato libreria

- [Importa intestazione](#import-header)
- [Tipo di importazione](#import-type)

Librerie di importazione tradizionali, ovvero librerie che descrivono le esportazioni da un'immagine per l'uso da parte di un altro, in genere seguono il layout descritto nella sezione 7 del [formato di file archivio (libreria)](#archive-library-file-format). La differenza principale consiste nel fatto che i membri della libreria di importazione contengono file pseudo-oggetto anziché quelli reali, in cui ogni membro include i contributi della sezione necessari per compilare le tabelle di importazione descritte nella sezione 6,4, la [sezione. idata](#the-idata-section) che il linker genera l'archivio durante la compilazione dell'applicazione di esportazione.

La sezione contributi per un'importazione può essere dedotta da un piccolo set di informazioni. Il linker può generare le informazioni dettagliate complete nella libreria di importazione per ogni membro al momento della creazione della libreria oppure scrivere solo le informazioni canoniche nella libreria e consentire all'applicazione che in seguito lo userà per generare i dati necessari in modo immediato.

In una libreria di importazione con il formato esteso, un singolo membro contiene le informazioni seguenti:

<dl> Intestazione membro archivio  
Intestazione del file  
Intestazioni di sezione  
Dati che corrispondono a ognuna delle intestazioni di sezione  
Tabella di simboli COFF  
Stringhe  
  
</dl>

Al contrario, una libreria di importazione breve viene scritta nel modo seguente:

<dl> Intestazione membro archivio  
Importa intestazione  
Stringa del nome di importazione con terminazione null  
Stringa del nome DLL con terminazione null  
</dl>

Si tratta di informazioni sufficienti per ricostruire accuratamente l'intero contenuto del membro al momento dell'utilizzo.

### <a name="import-header"></a>Importa intestazione

L'intestazione Import contiene i campi e gli offset seguenti:



| Offset         | Dimensione                | Campo                       | Descrizione                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | Il computer del file di immagine deve essere \_ \_ \_ sconosciuto. Per ulteriori informazioni, vedere [tipi di computer](#machine-types). <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Deve essere 0xFFFF. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Versione <br/>         | Versione della struttura. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Computer <br/>         | Numero che identifica il tipo di computer di destinazione. Per ulteriori informazioni, vedere [tipi di computer](#machine-types).<br/> |
| 8 <br/>  | 4 <br/>       | Timbro Time-Date <br/> | Data e ora di creazione del file. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Dimensioni dei dati <br/>    | Dimensioni delle stringhe che seguono l'intestazione. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordinale/hint <br/>    | Numero ordinale o suggerimento per l'importazione, determinato dal valore nel campo nome tipo. <br/>                   |
| 18 <br/> | 2 bit <br/>  | Tipo <br/>            | Tipo di importazione. Per i valori e le descrizioni specifici, vedere [tipo di importazione](#import-type).<br/>                           |
|                | 3 bit <br/>  | Tipo di nome <br/>       | Tipo di nome dell'importazione. Per ulteriori informazioni, vedere [Import Name Type](#import-name-type). <br/>                           |
|                | 11 bit <br/> | Riservato <br/>        | Riservato, deve essere 0. <br/>                                                                                             |



 

Questa struttura è seguita da due stringhe con terminazione null che descrivono il nome del simbolo importato e la DLL da cui provengono.

### <a name="import-type"></a>Tipo di importazione

I valori seguenti sono definiti per il campo tipo nell'intestazione di importazione:

| Costante                  | Valore         | Descrizione                                      |
|---------------------------|---------------|--------------------------------------------------|
| Importa \_ codice <br/>  | 0 <br/> | Codice eseguibile. <br/>                     |
| Importa \_ dati <br/>  | 1 <br/> | Dati. <br/>                                |
| Importa \_ const <br/> | 2 <br/> | Specificato come CONSt nel file def. <br/> |

Questi valori vengono utilizzati per determinare quali contributi della sezione devono essere generati dallo strumento che utilizza la libreria se deve accedere a tali dati.

### <a name="import-name-type"></a>Importa tipo di nome

Il nome del simbolo di importazione con terminazione null segue immediatamente l'intestazione di importazione associata. I valori seguenti sono definiti per il campo tipo nome nell'intestazione Import. Indica il modo in cui il nome deve essere utilizzato per generare i simboli corretti che rappresentano l'importazione:

| Costante | Valore | Descrizione |
| - | - | - |
| Importa \_ ordinale | 0 | L'importazione è ordinata in base all'ordinale. Indica che il valore nel campo ordinale/hint dell'intestazione di importazione è l'ordinale dell'importazione. Se questa costante non viene specificata, il campo ordinale/hint deve essere sempre interpretato come hint dell'importazione. |
| \_Nome importazione | 1 | Il nome dell'importazione è identico al nome del simbolo pubblico. |
| Importa \_ nome \_ NoPrefix | 2 | Il nome dell'importazione è il nome del simbolo pubblico, ma viene ignorato il carattere di apertura, @ o facoltativamente \_ . |
| \_Nome importazione senza \_ decorare | 3 | Il nome dell'importazione è il nome del simbolo pubblico, ma viene ignorato il carattere iniziale, @ oppure, facoltativamente \_ , e viene troncato il primo @ . |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Appendice A: calcolo dell'hash dell'immagine del PE Authenticode

- [Che cos'è un hash dell'immagine del PE Authenticode?](#what-is-an-authenticode-pe-image-hash)
- [Che cosa viene trattato in un hash dell'immagine del PE Authenticode?](#what-is-covered-in-an-authenticode-pe-image-hash)

Per verificare l'integrità delle immagini, è previsto che vengano utilizzati diversi certificati di attributo. Tuttavia, la più comune è firma Authenticode. È possibile utilizzare una firma Authenticode per verificare che le sezioni pertinenti di un file di immagine PE non siano state modificate in alcun modo dal formato originale del file. Per eseguire questa operazione, le firme Authenticode contengono qualcosa denominato hash dell'immagine PE

### <a name="what-is-an-authenticode-pe-image-hash"></a>Che cos'è un hash dell'immagine del PE Authenticode?

L'hash dell'immagine del PE Authenticode, o l'hash del file per brevità, è simile al checksum di un file in quanto produce un valore ridotto che è correlato all'integrità di un file. Un checksum è prodotto da un algoritmo semplice e viene usato principalmente per rilevare gli errori di memoria. Ovvero viene usato per rilevare se un blocco di memoria su disco è peggiorato e i valori archiviati sono diventati danneggiati. Un hash di file è simile a un checksum in quanto rileva anche il danneggiamento del file. Tuttavia, a differenza della maggior parte degli algoritmi di checksum, è molto difficile modificare un file in modo che abbia lo stesso hash del file del formato originale (non modificato). In altre circostanze, un checksum è progettato per rilevare errori di memoria semplici che comportano il danneggiamento, ma è possibile usare un hash file per rilevare modifiche intenzionali e persino minime a un file, ad esempio quelle introdotte da virus, pirati informatici o programmi Trojan Horse.

In una firma Authenticode, l'hash del file viene firmato digitalmente utilizzando una chiave privata nota solo al firmatario del file. Un consumer di software può verificare l'integrità del file calcolando il valore hash del file e confrontandolo con il valore dell'hash firmato contenuto nella firma digitale Authenticode. Se gli hash di file non corrispondono, parte del file coperto dall'hash dell'immagine PE è stata modificata.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>Che cosa viene trattato in un hash dell'immagine del PE Authenticode?

Non è possibile o auspicabile includere tutti i dati dei file di immagine nel calcolo dell'hash dell'immagine PE. In alcuni casi presenta semplicemente caratteristiche indesiderate (ad esempio, non è possibile rimuovere le informazioni di debug dai file rilasciati pubblicamente); a volte è semplicemente impossibile. Ad esempio, non è possibile includere tutte le informazioni all'interno di un file di immagine in una firma Authenticode, quindi inserire la firma Authenticode che contiene tale hash dell'immagine PE nell'immagine PE e successivamente generare un hash dell'immagine PE identico includendo nuovamente tutti i dati del file di immagine nel calcolo, perché il file contiene ora la firma Authenticode che non era originariamente presente.

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Processo per la generazione dell'hash dell'immagine del PE Authenticode

In questa sezione vengono descritte le modalità di calcolo di un hash di immagini PE e le parti dell'immagine PE che è possibile modificare senza invalidare la firma Authenticode.

> [!NOTE]
> L'hash dell'immagine PE per un file specifico può essere incluso in un file di catalogo separato senza includere un certificato di attributo all'interno del file con hash. Questa operazione è pertinente, perché è possibile invalidare l'hash dell'immagine PE in un file di catalogo con firma Authenticode modificando un'immagine PE che non contiene effettivamente una firma Authenticode.

Tutti i dati nelle sezioni dell'immagine PE specificati nella tabella della sezione vengono completati con hashing, ad eccezione dei seguenti intervalli di esclusione:

- **Il campo CheckSum file dei campi specifici di Windows dell'intestazione facoltativa.** Questo checksum include l'intero file (inclusi eventuali certificati di attributo nel file). In ogni probabilità, il checksum sarà diverso dal valore originale dopo aver inserito la firma Authenticode.

- **Informazioni correlate ai certificati di attributo**. Le aree dell'immagine PE correlate alla firma Authenticode non sono incluse nel calcolo dell'hash dell'immagine PE, perché le firme Authenticode possono essere aggiunte o rimosse da un'immagine senza influire sull'integrità complessiva dell'immagine. Questo non è un problema, perché esistono scenari utente che dipendono dalla ripetizione della firma di immagini PE o dall'aggiunta di un timestamp. Authenticode esclude le informazioni seguenti dal calcolo hash:

  - Campo della tabella dei certificati delle directory dei dati di intestazione facoltative.

  - La tabella dei certificati e i certificati corrispondenti a cui fa riferimento il campo della tabella dei certificati elencati immediatamente sopra.

  Per calcolare l'hash dell'immagine PE, Authenticode Ordina le sezioni specificate nella sezione tabella per intervallo di indirizzi, quindi genera un hash per la sequenza di byte risultante, passando gli intervalli di esclusione.

- **Informazioni oltre la fine dell'ultima sezione.** Non viene eseguito l'hashing dell'area oltre l'ultima sezione (definita dall'offset massimo). Questa area contiene in genere informazioni di debug. Le informazioni di debug possono in genere essere considerate consultive per i debugger. non influisce sull'integrità effettiva del programma eseguibile. È letteralmente possibile rimuovere le informazioni di debug da un'immagine dopo che un prodotto è stato recapitato e non influisce sulla funzionalità del programma. In realtà, questa operazione viene a volte eseguita come misura di salvataggio su disco. Vale la pena notare che le informazioni di debug contenute nelle sezioni specificate dell'immagine PE non possono essere rimosse senza invalidare la firma Authenticode.

È possibile utilizzare gli strumenti MakeCert e SignTool disponibili in Windows Platform SDK per sperimentare la creazione e la verifica delle firme Authenticode. Per ulteriori informazioni, vedere la sezione di riferimento riportata di seguito.

## <a name="references"></a>Riferimenti

[Download e strumenti per Windows (include il Windows SDK)](https://developer.microsoft.com/windows/downloads)

[Creazione, visualizzazione e gestione dei certificati](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Procedura dettagliata per la firma del codice in modalità kernel (doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Formato di firma eseguibile portatile Windows Authenticode (. docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[Funzioni ImageHlp](/windows/desktop/Debug/imagehlp-functions)