---
description: Specifica del file system exFat.
title: Specifica file system exFAT
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 94b5bcdc69201573bc92290c148a7d3ce8304868
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119016"
---
# <a name="exfat-file-system-specification"></a>Specifica file system exFAT

## <a name="1-introduction"></a>1 Introduzione

L'file system exFAT è il successore di FAT32 nella famiglia di file system FAT. Questa specifica descrive il file system exFAT e fornisce tutte le informazioni necessarie per l'implementazione del file system exFAT.

### <a name="11-design-goals"></a>1.1 Obiettivi di progettazione

Il modello exFAT file system tre obiettivi di progettazione centrali (vedere l'elenco seguente).

1. *Mantenere la semplicità dei file system basati su FAT.*

   > Due dei punti di forza dei file system basati su FAT sono la relativa semplicità e facilità di implementazione. Nell'anima dei predecessori, gli implementatori dovrebbero trovare exFAT relativamente semplice e facile da implementare.

2. *Abilitare file e dispositivi di archiviazione di dimensioni molto grandi.*

   > L'file system exFAT usa 64 bit per descrivere le dimensioni del file, consentendo così applicazioni che dipendono da file di dimensioni molto grandi. L'file system exFAT consente anche cluster di dimensioni fino a 32 MB, consentendo in modo efficace dispositivi di archiviazione di grandi dimensioni.

3. *Incorporare l'estendibilità per l'innovazione futura.*

   > L'file system exFAT incorpora l'estendibilità nella progettazione, consentendo al file system di tenere il passo con le innovazioni nell'archiviazione e i cambiamenti nell'utilizzo.

### <a name="12-specific-terminology"></a>1.2 Terminologia specifica

Nel contesto di questa specifica, alcuni termini (vedere la tabella [1)](#table-1-definition-of-terms-which-carry-very-specific-meaning)hanno un significato specifico per la progettazione e l'implementazione del file system exFAT.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Tabella 1 Definizione di termini che hanno un significato molto specifico**

<table>
<thead>
<tr class="header">
<th><strong>Termine</strong></th>
<th><strong>Definizione</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Deve</td>
<td>Questa specifica usa il termine "deve" per descrivere un comportamento obbligatorio.</td>
</tr>
<tr class="even">
<td>Dovrebbe</td>
<td>Questa specifica usa il termine "should" per descrivere un comportamento fortemente consigliato, ma non obbligatorio.</td>
</tr>
<tr class="odd">
<td>Mag</td>
<td>Questa specifica usa il termine "may" per descrivere un comportamento facoltativo.</td>
</tr>
<tr class="even">
<td>Obbligatorio</td>
<td>Questo termine descrive un campo o una struttura che un'implementazione deve modificare e deve interpretare come descrive questa specifica.</td>
</tr>
<tr class="odd">
<td>Facoltativo</td>
<td>Questo termine descrive un campo o una struttura che un'implementazione può supportare o meno. Se un'implementazione supporta un campo o una struttura facoltativa specifica, deve modificare e interpretare il campo o la struttura come descritto in questa specifica.</td>
</tr>
<tr class="even">
<td>Non definito</td>
<td>Questo termine descrive il contenuto del campo o della struttura che un'implementazione può modificare in base alle esigenze (ad esempio, deselezionare zero quando si impostano i campi o le strutture circostanti) e non deve interpretare per contenere alcun significato specifico.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td><p>Questo termine descrive il contenuto del campo o della struttura per le implementazioni seguenti:</p>
<ol type="1">
<li><p>Deve inizializzare su zero e non deve essere utilizzato per alcun scopo</p></li>
<li><p>Non deve interpretare, tranne quando si calcolano i checksum</p></li>
<li><p>Deve mantenere tra le operazioni che modificano i campi o le strutture circostanti</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1.3 Full text degli acronimi comuni

Questa specifica usa acronimi in uso comune nel settore personal computer (vedere [la tabella 2](#table-2-full-text-of-common-acronyms)).

<div id="table-2-full-text-of-common-acronyms" />

**Tabella 2 Full Text degli acronimi comuni**

| **Acronimo** | **Full-text**                                      |
|-------------|----------------------------------------------------|
| ASCII       | American Standard Code for Information Interchange |
| BIOS        | Sistema di output di input di base                          |
| CPU         | Unità di elaborazione centrale                            |
| exFAT       | Tabella di allocazione file estendibile                   |
| FAT         | Tabella di allocazione file                              |
| FAT12       | Tabella di allocazione file, indici cluster a 12 bit      |
| FAT16       | Tabella di allocazione file, indici cluster a 16 bit      |
| FAT32       | Tabella di allocazione file, indici cluster a 32 bit      |
| GPT         | tabella delle partizioni GUID                               |
| GUID        | Identificatore univoco globale (vedere [la sezione 10.1)](#101-globally-unique-identifiers-guids)      |
| INT         | Interrompere                                          |
| MBR         | record di avvio principale                                 |
| texFAT      | ExFAT sicuro per le transazioni                             |
| UTC         | Coordinated Universal Time                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1.4 Qualificatori di campo e struttura predefiniti

I campi e le strutture in questa specifica hanno i qualificatori seguenti (vedere l'elenco seguente), a meno che la specifica non venga indicata diversamente.

1. Sono senza segno

2. Usare la notazione decimale per descrivere i valori, se non diversamente specificato; questa specifica usa la lettera successiva alla correzione "h" per indicare i numeri esadecimali e racchiude i GUID tra parentesi graffe

3. Sono in formato little-endian

4. Non è necessario un carattere di terminazione Null per le stringhe

### <a name="15-windows-ce-and-texfat"></a>1.5 Windows CE e TexFAT

TexFAT è un'estensione di exFAT che aggiunge una semantica operativa sicura per le transazioni sulla base file system. TexFAT viene usato da Windows CE.
TexFAT richiede l'uso dei due FAT e delle bitmap di allocazione da usare nelle transazioni. Definisce anche diverse strutture aggiuntive, tra cui descrittori di spaziatura interna e descrittori di sicurezza.

## <a name="2-volume-structure"></a>2 Struttura del volume

Un volume è il set di tutte le strutture file system dati e lo spazio dati necessario per archiviare e recuperare i dati utente. Tutti i volumi exFAT contengono quattro aree (vedere [la tabella 3).](#table-3-volume-structure)

<div id="table-3-volume-structure" />

**Tabella 3 Struttura del volume**

<table>
<thead>
<tr class="header">
<th><strong>Nome dell'area secondaria</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(settore)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(settori)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Area di avvio principale</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Settore di avvio principale</td>
<td>0</td>
<td>1</td>
<td>Questa sotto-area è obbligatoria e <a href="#31-main-and-backup-boot-sector-sub-regions">la Sezione 3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Settori di avvio estesi principali</td>
<td>1</td>
<td>8</td>
<td>Questa sotto-area è obbligatoria e <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">la sezione 3.2</a>ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Parametri OEM principali</td>
<td>9</td>
<td>1</td>
<td>Questa sotto-area è obbligatoria e <a href="#33-main-and-backup-oem-parameters-sub-regions">la sezione 3.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato principale</td>
<td>10</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e il relativo contenuto è riservato.</td>
</tr>
<tr class="even">
<td>Checksum di avvio principale</td>
<td>11</td>
<td>1</td>
<td>Questa sotto-area è obbligatoria e <a href="#34-main-and-backup-boot-checksum-sub-regions">la Sezione 3.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td><strong>Area di avvio del backup</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Settore di avvio del backup</td>
<td>12</td>
<td>1</td>
<td>Questa sotto-area è obbligatoria e <a href="#31-main-and-backup-boot-sector-sub-regions">la Sezione 3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Settori di avvio estesi di backup</td>
<td>13</td>
<td>8</td>
<td>Questa sotto-area è obbligatoria e <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">la sezione 3.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Parametri OEM di backup</td>
<td>21</td>
<td>1</td>
<td>Questa sotto-area è obbligatoria e <a href="#33-main-and-backup-oem-parameters-sub-regions">la sezione 3.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Backup riservato</td>
<td>22</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e il relativo contenuto è riservato.</td>
</tr>
<tr class="even">
<td>Checksum di avvio del backup</td>
<td>23</td>
<td>1</td>
<td>Questa sotto-area è obbligatoria e <a href="#34-main-and-backup-boot-checksum-sub-regions">la Sezione 3.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td><strong>Area FAT</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Allineamento FAT</td>
<td>24</td>
<td>FatOffset - 24</td>
<td><p>Questa area secondaria è obbligatoria e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo FatOffset.</p></td>
</tr>
<tr class="odd">
<td>Primo FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>Questa sotto-area è obbligatoria e <a href="#41-first-and-second-fat-sub-regions">la Sezione 4.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi FatOffset e FatLength.</p></td>
</tr>
<tr class="even">
<td>Seconda fat</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOfFats – 1)</td>
<td><p>Questa sotto-area è obbligatoria e <a href="#41-first-and-second-fat-sub-regions">la Sezione 4.1</a> ne definisce il contenuto, se presente.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi FatOffset, FatLength e NumberOfFats. Il campo NumberOfFats può contenere solo valori 1 e 2.</p></td>
</tr>
<tr class="odd">
<td><strong>Area dati</strong></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>Allineamento heap cluster</td>
<td>FatOffset + FatLength * NumberOfFats</td>
<td>ClusterHeapOffset : (FatOffset + FatLength * NumberOfFats)</td>
<td><p>Questa area secondaria è obbligatoria e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi FatOffset, FatLength, NumberOfFats e ClusterHeapOffset. I valori validi del campo NumberOfFats sono 1 e 2.</p></td>
</tr>
<tr class="odd">
<td>Cluster Heap</td>
<td>ClusterHeapOffset</td>
<td>ClusterCount * 2<sup>SectorsPerClusterShift</sup></td>
<td><p>Questa sotto-area è obbligatoria e <a href="#51-cluster-heap-sub-region">la sezione 5.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi ClusterHeapOffset, ClusterCount e SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td>Spazio in eccesso</td>
<td>ClusterHeapOffset + ClusterCount * 2<sup>SectorsPerClusterShift</sup></td>
<td>VolumeLength : (ClusterHeapOffset + ClusterCount * 2<sup>SectorsPerClusterShift</sup>)</td>
<td><p>Questa area secondaria è obbligatoria e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi ClusterHeapOffset, ClusterCount, SectorsPerClusterShift e VolumeLength.</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 aree di avvio principale e di backup

L'area avvio principale fornisce tutte le istruzioni di avvio necessarie, le informazioni di identificazione e file system parametri per consentire a un'implementazione di eseguire le operazioni seguenti:

1. Boot-strap un sistema di computer da un volume exFAT.

2. Identificare il file system nel volume come exFAT.

3. Individuare la posizione delle strutture file system exFAT.

L'area Avvio backup è un backup dell'area avvio principale. Consente il ripristino del volume exFAT nel caso in cui l'area di avvio principale sia in uno stato incoerente. Ad eccezione di casi poco frequenti, ad esempio l'aggiornamento delle istruzioni di avvio, le implementazioni non devono modificare il contenuto dell'area Di avvio backup.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3.1 Sottoaree del settore di avvio principale e di backup

Il settore di avvio principale contiene il codice per l'avvio da un volume exFAT e i parametri exFAT fondamentali che descrivono la struttura del volume (vedere [la tabella 4](#table-4-main-and-backup-boot-sector-structure)). BIOS, MBR o altri agenti di avvio possono esaminare questo settore e caricare ed eseguire le istruzioni di avvio contenute in tale settore.

Il settore di avvio del backup è un backup del settore di avvio principale e ha la stessa struttura (vedere [la tabella 4](#table-4-main-and-backup-boot-sector-structure)). Il settore di avvio del backup può facilitare le operazioni di ripristino. Tuttavia, le implementazioni trattano il contenuto dei campi VolumeFlags e PercentInUse come non obsoleti.

Prima di usare il contenuto del settore di avvio principale o di backup, le implementazioni devono verificarne il contenuto convalidando il checksum di avvio corrispondente e verificando che tutti i campi siano entro l'intervallo di valori validi.

Mentre l'operazione di formattazione iniziale iniziali inizialirà il contenuto dei settori di avvio principale e di backup, le implementazioni possono aggiornare questi settori e aggiornare anche il rispettivo checksum di avvio in base alle esigenze. Tuttavia, le implementazioni possono aggiornare i campi VolumeFlags o PercentInUse senza aggiornare il checksum di avvio corrispondente (il checksum esclude in modo specifico questi due campi).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tabella 4 Struttura del settore di avvio principale e di backup**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>Questo campo è obbligatorio <a href="#311-jumpboot-field">e la Sezione 3.1.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#312-filesystemname-field">e la Sezione 3.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>Questo campo è obbligatorio <a href="#313-mustbezero-field">e la sezione 3.1.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#314-partitionoffset-field">e la sezione 3.1.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#315-volumelength-field">e la sezione 3.1.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#316-fatoffset-field">e la sezione 3.1.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#317-fatlength-field">e la sezione 3.1.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#318-clusterheapoffset-field">e la sezione 3.1.8</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>ClusterCount</td>
<td>92</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#319-clustercount-field">e la sezione 3.1.9</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3110-firstclusterofrootdirectory-field">e la sezione 3.1.10</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3111-volumeserialnumber-field">e la sezione 3.1.11</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#3112-filesystemrevision-field">e la sezione 3.1.12</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Flag volume</td>
<td>106</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#3113-volumeflags-field">e la sezione 3.1.13</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#3114-bytespersectorshift-field">e la sezione 3.1.14</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SettoriPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#3115-sectorsperclustershift-field">e la sezione 3.1.15</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>NumberOfFats</td>
<td>110</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#3116-numberoffats-field">e la sezione 3.1.16</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Selezione unità</td>
<td>111</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#3117-driveselect-field">e la sezione 3.1.17</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#3118-percentinuse-field">e la sezione 3.1.18</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>113</td>
<td>7</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="even">
<td>Codice di avvio</td>
<td>120</td>
<td>390</td>
<td>Questo campo è obbligatorio <a href="#3119-bootcode-field">e la sezione 3.1.19</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#3120-bootsignature-field">e la sezione 3.1.20</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Spazio in eccesso</td>
<td>512</td>
<td>2<sup>BytesPerSectorShift</sup> – 512</td>
<td><p>Questo campo è obbligatorio e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori principale e di avvio del backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 JumpBoot Field

Il campo JumpBoot conterrà l'istruzione di salto per le CPU comuni nei personal computer, che, quando eseguita, "salta" la CPU per eseguire le istruzioni di avvio nel campo BootCode.

Il valore valido per questo campo è EBh 76h 90h (in ordine di byte di ordine basso a byte più alto).

#### <a name="312-filesystemname-field"></a>3.1.2 Campo FileSystemName

Il campo FileSystemName deve contenere il nome del file system nel volume.

Il valore valido per questo campo è, in caratteri ASCII, "EXFAT", che include tre spazi vuoti finali.

#### <a name="313-mustbezero-field"></a>3.1.3 Campo MustBeZero

Il campo MustBeZero deve corrispondere direttamente all'intervallo di byte utilizzato dal blocco di parametri BIOS compressi nei volumi FAT12/16/32.

Il valore valido per questo campo è 0, che consente di impedire alle implementazioni FAT12/16/32 di montare erroneamente un volume exFAT.

#### <a name="314-partitionoffset-field"></a>3.1.4 Campo PartitionOffset

Il campo PartitionOffset deve descrivere l'offset di settore relativo ai supporti della partizione che ospita il volume exFAT specificato. Questo campo favorisce l'avvio dal volume usando int 13h esteso nei personal computer.

Tutti i valori possibili per questo campo sono validi. Tuttavia, il valore 0 indica che le implementazioni devono ignorare questo campo.

#### <a name="315-volumelength-field"></a>3.1.5 Campo VolumeLength

Il campo VolumeLength deve descrivere le dimensioni del volume exFAT specificato nei settori.

L'intervallo valido di valori per questo campo deve essere:

- Almeno<sup>2 20/2</sup><sup>BytesPerSectorShift,</sup>che garantisce che il volume più piccolo non sia inferiore a 1 MB

- Al massimo 2<sup>64</sup>- 1, il valore più grande che questo campo può descrivere

Tuttavia, se la dimensione della sottoarea Spazio in eccesso è 0, il valore di questo campo è ClusterHeapOffset + (2<sup>32</sup>- 11) \* 2<sup>SectorsPerClusterShift</sup>.

#### <a name="316-fatoffset-field"></a>3.1.6 Campo FatOffset

Il campo FatOffset descrive l'offset del settore relativo al volume della prima fat. Questo campo consente alle implementazioni di allineare la prima FAT alle caratteristiche del supporto di archiviazione sottostante.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 24, che rappresenta i settori utilizzati dall'avvio principale e dall'avvio di backup

- Al massimo ClusterHeapOffset - (FatLength NumberOfFats), che rappresenta i settori utilizzati \* dall'heap del cluster

#### <a name="317-fatlength-field"></a>3.1.7 Campo FatLength

Il campo FatLength descrive la lunghezza, in settori, di ogni tabella FAT (il volume può contenere fino a due FAT).

L'intervallo valido di valori per questo campo deve essere:

- Almeno (ClusterCount + 2) \* 2<sup>2/2</sup><sup>BytesPerSectorShift</sup>arrotondato per eccesso all'intero più vicino, assicurando che ogni FAT abbia spazio sufficiente per descrivere tutti i cluster nell'heap del cluster

- Al massimo (ClusterHeapOffset - FatOffset) / NumberOfFats arrotondato per eccesso all'intero più vicino, che garantisce l'esistenza dei fat prima dell'heap del cluster

Questo campo può contenere un valore superiore al limite inferiore (come descritto in precedenza) per consentire anche l'allineamento della seconda FAT, se presente, alle caratteristiche del supporto di archiviazione sottostante. Il contenuto dello spazio che supera quello richiesto dalla fat stessa, se presente, non è definito.

#### <a name="318-clusterheapoffset-field"></a>3.1.8 Campo ClusterHeapOffset

Il campo ClusterHeapOffset descrive l'offset del settore relativo al volume dell'heap del cluster. Questo campo consente alle implementazioni di allineare l'heap del cluster alle caratteristiche del supporto di archiviazione sottostante.

L'intervallo valido di valori per questo campo deve essere:

- Almeno FatOffset + FatLength NumberOfFats, per conto dei settori utilizzati da \* tutte le aree precedenti

- Al massimo 2<sup>32</sup>- 1 o VolumeLength - (ClusterCount \* 2<sup>SectorsPerClusterShift</sup>), a seconda del calcolo meno

#### <a name="319-clustercount-field"></a>3.1.9 Campo ClusterCount

Il campo ClusterCount descrive il numero di cluster contenuti nell'heap del cluster.

Il valore valido per questo campo deve essere minore di quanto segue:

- (VolumeLength - ClusterHeapOffset) / 2<sup>SectorsPerClusterShift</sup>arrotondato per esere all'intero più vicino, che corrisponde esattamente al numero di cluster che possono essere compresi tra l'inizio dell'heap cluster e la fine del volume

- 2<sup>32</sup>- 11, ovvero il numero massimo di cluster che una FAT può descrivere

Il valore del campo ClusterCount determina le dimensioni minime di una fat. Per evitare faT estremamente grandi, le implementazioni possono controllare il numero di cluster nell'heap del cluster aumentando le dimensioni del cluster (tramite il campo SectorsPerClusterShift). Questa specifica consiglia non più di 2<sup>cluster da 24</sup>a 2 nell'heap cluster. Tuttavia, le implementazioni devono essere in grado di gestire i volumi con un massimo di 2<sup>cluster da 32</sup>a 11 nell'heap del cluster.

#### <a name="3110-firstclusterofrootdirectory-field"></a>3.1.10 Campo FirstClusterOfRootDirectory

Il campo FirstClusterOfRootDirectory deve contenere l'indice cluster del primo cluster della directory radice. Le implementazioni devono eseguire ogni sforzo per inserire il primo cluster della directory radice nel primo cluster non negativo dopo l'utilizzo della mappa di bit di allocazione e della tabella up case nei cluster.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 2, l'indice del primo cluster nell'heap del cluster

- Al massimo ClusterCount + 1, l'indice dell'ultimo cluster nell'heap del cluster

#### <a name="3111-volumeserialnumber-field"></a>3.1.11 Campo VolumeSerialNumber

Il campo VolumeSerialNumber deve contenere un numero di serie univoco. Ciò consente alle implementazioni di distinguere tra i diversi volumi exFAT.
Le implementazioni devono generare il numero di serie combinando la data e l'ora di formattazione del volume exFAT. Il meccanismo per combinare data e ora per formare un numero di serie è specifico dell'implementazione.

Tutti i valori possibili per questo campo sono validi.

#### <a name="3112-filesystemrevision-field"></a>3.1.12 Campo FileSystemRevision

Il campo FileSystemRevision descrive i numeri di revisione principale e secondaria delle strutture exFAT nel volume specificato.

Il byte più alto è il numero di revisione principale e il byte meno significativo è il numero di revisione secondario. Ad esempio, se il byte di ordine elevato contiene il valore 01h e se il byte di ordine più basso contiene il valore 05h, il campo FileSystemRevision descrive il numero di revisione 1,05.
Analogamente, se il byte di ordine elevato contiene il valore 0Ah e se il byte di ordine più basso contiene il valore 0Fh, il campo FileSystemRevision descrive il numero di revisione 10,15.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 0 per il byte meno significativo e 1 per il byte di ordine elevato

- Al massimo 99 per il byte di ordine basso e 99 per il byte di ordine elevato

Il numero di revisione di exFAT descritto da questa specifica è 1,00.
Le implementazioni di questa specifica devono montare qualsiasi volume exFAT con numero di revisione principale 1 e non montare alcun volume exFAT con altri numeri di revisione principali. Le implementazioni rispettano il numero di revisione secondario e non devono eseguire operazioni o creare strutture file system non descritte nella specifica corrispondente del numero di revisione secondario specificato.

#### <a name="3113-volumeflags-field"></a>3.1.13 Campo VolumeFlags

Il campo VolumeFlags deve contenere flag che indicano lo stato di varie strutture file system nel volume exFAT (vedere [la tabella 5).](#table-5-volumeflags-field-structure)

Le implementazioni non devono includere questo campo durante il calcolo del checksum dell'area di avvio principale o di backup corrispondente. Quando si fa riferimento al settore di avvio del backup, le implementazioni devono considerare questo campo come obsoleto.

<div id="table-5-volumeflags-field-structure" />

**Tabella 5 Struttura dei campi VolumeFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveFat</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#31131-activefat-field">e la sezione 3.1.13.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#31132-volumedirty-field">e la sezione 3.1.13.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#31133-mediafailure-field">e la sezione 3.1.13.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#31134-cleartozero-field">e la sezione 3.1.13.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>4</td>
<td>12</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>3.1.13.1 Campo ActiveFat

Il campo ActiveFat descrive quali fat e bitmap di allocazione sono attivi (e le implementazioni devono usare), come indicato di seguito:

- 0, ovvero la prima bitmap FAT e la prima bitmap di allocazione sono attive

- 1, ovvero la seconda bitmap fat e la seconda bitmap di allocazione sono attive ed è possibile solo quando il campo NumberOfFats contiene il valore 2

Le implementazioni considerano inattivi FAT e Bitmap di allocazione come non obsoleti. Solo le implementazioni in grado di riconoscere TexFAT devono cambiare le bitmap fat e di allocazione attive (vedere [la sezione 7.1).](#71-allocation-bitmap-directory-entry)

##### <a name="31132-volumedirty-field"></a>3.1.13.2 Campo VolumeDirty

Il campo VolumeDirty deve indicare se il volume è dirty o meno, come indicato di seguito:

- 0, ovvero il volume è probabilmente in uno stato coerente

- 1, ovvero il volume è probabilmente in uno stato incoerente

Le implementazioni devono impostare il valore di questo campo su 1 quando si verificano file system incoerenze dei metadati che non vengono risolte. Se, al momento del montaggio di un volume, il valore di questo campo è 1, solo le implementazioni che risolvono file system incoerenze dei metadati possono cancellare il valore di questo campo su 0. Tali implementazioni devono cancellare il valore di questo campo su 0 solo dopo aver file system che si trova in uno stato coerente.

Se, al momento del montaggio di un volume, il valore di questo campo è 0, le implementazioni devono impostare questo campo su 1 prima di aggiornare i metadati di file system e deselezionare questo campo su 0 in seguito, in modo analogo all'ordinamento di scrittura consigliato descritto nella Sezione [8.1.](#81-recommended-write-ordering)

##### <a name="31133-mediafailure-field"></a>3.1.13.3 Campo MediaFailure

Il campo MediaFailure deve descrivere se un'implementazione ha rilevato o meno errori multimediali, come indicato di seguito:

- 0, ovvero il supporto di hosting non ha segnalato errori o eventuali errori noti sono già registrati nei cluster FAT come "non erati"

- 1, ovvero il supporto di hosting ha segnalato errori (ad esempio, non sono riuscite operazioni di lettura o scrittura)

Un'implementazione deve impostare questo campo su 1 quando:

1. Il supporto di hosting non riesce ad accedere a qualsiasi area nel volume

2. L'implementazione ha esaurito gli algoritmi di ripetizione dei tentativi di accesso, se presenti

Se, al momento del montaggio di un volume, il valore di questo campo è 1, le implementazioni che analizzano l'intero volume alla ricerca di errori dei supporti e registrano tutti gli errori come cluster "non valido" nella FAT (o in caso contrario risolvono gli errori dei supporti) possono cancellare il valore di questo campo su 0.

##### <a name="31134-cleartozero-field"></a>3.1.13.4 Campo ClearToZero

Il campo ClearToZero non ha un significato significativo in questa specifica.

I valori validi per questo campo sono:

- 0, che non ha alcun significato particolare

- 1, ovvero le implementazioni devono cancellare il campo su 0 prima di modificare file system, directory o file

#### <a name="3114-bytespersectorshift-field"></a>Campo BytesPerSectorShift 3.1.14

Il campo BytesPerSectorShift deve descrivere i byte per settore espressi come log<sub>2</sub>(N), dove N è il numero di byte per settore. Ad esempio, per 512 byte per settore, il valore di questo campo è 9.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 9 (dimensione del settore di 512 byte), che è il settore più piccolo possibile per un volume exFAT

- Al massimo 12 (dimensioni del settore di 4096 byte), ovvero le dimensioni della pagina di memoria delle CPU comuni nei personal computer

#### <a name="3115-sectorsperclustershift-field"></a>3.1.15 SettoriPerClusterShift Campo

Il campo SectorsPerClusterShift descrive i settori per cluster espressi come log<sub>2</sub>(N), dove N è il numero di settori per cluster. Ad esempio, per 8 settori per cluster, il valore di questo campo è 3.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 0 (1 settore per cluster), che è il cluster più piccolo possibile

- Al massimo 25 - BytesPerSectorShift, che restituisce una dimensione del cluster di 32 MB

#### <a name="3116-numberoffats-field"></a>3.1.16 Campo NumberOfFats

Il campo NumberOfFats deve descrivere il numero di fat e bitmap di allocazione contenuti nel volume.

L'intervallo valido di valori per questo campo deve essere:

- 1, che indica che il volume contiene solo la prima bitmap FAT e la prima bitmap di allocazione

- 2, che indica che il volume contiene la prima fat, la seconda FAT, la prima bitmap di allocazione e la seconda bitmap di allocazione; questo valore è valido solo per i volumi TexFAT

#### <a name="3117-driveselect-field"></a>3.1.17 DriveSelect Field

Il campo DriveSelect deve contenere il numero di unità INT 13h esteso, che consente l'avvio da questo volume usando INT 13h esteso nei personal computer.

Tutti i valori possibili per questo campo sono validi. Campi simili nei file system precedenti basati su FAT contenevano spesso il valore 80h.

#### <a name="3118-percentinuse-field"></a>3.1.18 Campo PercentInUse

Il campo PercentInUse descrive la percentuale di cluster allocati nell'heap del cluster.

L'intervallo valido di valori per questo campo deve essere:

- Tra 0 e 100 inclusi, ovvero la percentuale di cluster allocati nell'heap del cluster, arrotondata per esere al numero intero più vicino

- Esattamente FFh, che indica che la percentuale di cluster allocati nell'heap del cluster non è disponibile

Le implementazioni modificano il valore di questo campo per riflettere le modifiche nell'allocazione dei cluster nell'heap del cluster o lo modificano in FFh.

Le implementazioni non devono includere questo campo durante il calcolo del checksum dell'area di avvio principale o di backup corrispondente. Quando si fa riferimento al settore di avvio del backup, le implementazioni devono considerare questo campo come obsoleto.

#### <a name="3119-bootcode-field"></a>3.1.19 Campo BootCode

Il campo BootCode deve contenere istruzioni di boot-strapping.
Le implementazioni possono popolare questo campo con le istruzioni della CPU necessarie per l'avvio di un sistema informatico. Le implementazioni che non forniscono istruzioni di boot-strapping devono inizializzare ogni byte in questo campo su F4h (l'istruzione di arresto per le CPU comuni nei personal computer) come parte del relativo funzionamento del formato.

#### <a name="3120-bootsignature-field"></a>3.1.20 Campo BootSignature

Il campo BootSignature descrive se lo scopo di un determinato settore è che sia un settore di avvio o meno.

Il valore valido per questo campo è AA55h. Qualsiasi altro valore in questo campo invalida il rispettivo settore di avvio. Le implementazioni devono verificare il contenuto di questo campo prima di a seconda di qualsiasi altro campo nel rispettivo settore di avvio.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3.2 Sottoreti principali e di backup dei settori di avvio estesi

Ogni settore dei principali settori di avvio esteso ha la stessa struttura. tuttavia, ogni settore può contenere istruzioni di avvio distinte (vedere la tabella 6). Gli agenti di avvio, ad esempio le istruzioni di avvio nel settore di avvio principale, le implementazioni alternative del BIOS o il firmware di un sistema incorporato, possono caricare questi settori ed eseguire le istruzioni contenute.

I settori di avvio estesi di backup sono un backup dei principali settori di avvio esteso e hanno la stessa struttura (vedere [la tabella 6](#table-6-extended-boot-sector-structure)).

Prima di eseguire le istruzioni dei settori di avvio principale o di backup esteso, le implementazioni devono verificarne il contenuto assicurando che il campo ExtendedBootSignature di ogni settore contenga il valore prescritto.

Mentre l'operazione di formattazione iniziale iniziali inizialirà il contenuto dei settori di avvio principale e di avvio esteso di backup, le implementazioni possono aggiornare questi settori (e aggiornano anche il rispettivo checksum di avvio) in base alle esigenze.

<div id="table-6-extended-boot-sector-structure" />

**Tabella 6 Struttura del settore di avvio esteso**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td><p>Questo campo è obbligatorio <a href="#321-extendedbootcode-field">e la Sezione 3.2.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td>4</td>
<td><p>Questo campo è obbligatorio <a href="#322-extendedbootsignature-field">e la Sezione 3.2.2</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 Campo ExtendedBootCode

Il campo ExtendedBootCode deve contenere istruzioni di avvio.
Le implementazioni possono popolare questo campo con le istruzioni della CPU necessarie per l'avvio di un sistema informatico. Le implementazioni che non forniscono istruzioni di avvio devono inizializzare ogni byte in questo campo su 00h come parte dell'operazione di formattazione.

#### <a name="322-extendedbootsignature-field"></a>3.2.2 Campo ExtendedBootSignature

Il campo ExtendedBootSignature deve indicare se la finalità di un determinato settore è che sia un settore di avvio esteso o meno.

Il valore valido per questo campo è AA550000h. Qualsiasi altro valore in questo campo invalida il rispettivo settore di avvio principale o di backup esteso.
Le implementazioni devono verificare il contenuto di questo campo prima di a seconda di qualsiasi altro campo nel rispettivo settore di avvio esteso.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3.3 Sottoreti principali e parametri OEM di backup

La sotto-area parametri OEM principale contiene dieci strutture di parametri che possono contenere informazioni specifiche del produttore (vedere [la tabella 7).](#table-7-oem-parameters-structure) Ognuna delle dieci strutture di parametri deriva dal modello Parametri generici (vedere [la Sezione 3.3.2).](#332-generic-parameters-template) I produttori possono derivare le proprie strutture di parametri personalizzati dal modello Parametri generici. Questa specifica definisce due strutture di parametri: Parametri Null (vedere La sezione [3.3.3)](#333-null-parameters)e Parametri Flash (vedere [La sezione 3.3.4).](#334-flash-parameters)

I parametri OEM di backup sono un backup dei parametri OEM principali e hanno la stessa struttura (vedere [la tabella 7).](#table-7-oem-parameters-structure)

Prima di usare il contenuto dei parametri OEM Main o Backup, le implementazioni devono verificarne il contenuto convalidando il checksum di avvio corrispondente.

I produttori devono popolare i parametri OEM Main e Backup con le proprie strutture di parametri personalizzati, se presenti, e qualsiasi altra struttura di parametri. Le operazioni di formato successive mantengono il contenuto dei parametri OEM principale e di backup.

Le implementazioni possono aggiornare i parametri OEM Principale e Backup in base alle esigenze (e devono anche aggiornare il rispettivo checksum di avvio).

<div id="table-7-oem-parameters-structure" />

**Tabella 7 Struttura dei parametri OEM**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parametri[0]</td>
<td>0</td>
<td>48</td>
<td>Questo campo è obbligatorio <a href="#331-parameters0--parameters9">e la sezione 3.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Parametri[9]</td>
<td>432</td>
<td>48</td>
<td>Questo campo è obbligatorio <a href="#331-parameters0--parameters9">e la sezione 3.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>480</td>
<td>2<sup>BytesPerSectorShift</sup> – 480</td>
<td><p>Questo campo è obbligatorio e il relativo contenuto è riservato.</p>
<p>Nota: i settori principale e di avvio del backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 Parametri \[ 0 \] ... Parametri \[ 9\]

Ogni campo Parameters in questa matrice contiene una struttura di parametri, che deriva dal modello Generic Parameters (vedere [la sezione 3.3.2).](#332-generic-parameters-template)
Tutti i campi Parametri inutilizzati devono essere descritti come contenenti una struttura di parametri Null (vedere [la sezione 3.3.3).](#333-null-parameters)

#### <a name="332-generic-parameters-template"></a>3.3.2 Modello di parametri generici

Il modello Parametri generici fornisce la definizione di base di una struttura di parametri (vedere [la tabella 8).](#table-8-generic-parameters-template) Tutte le strutture di parametri derivano da questo modello. Il supporto per questo modello di parametri generici è obbligatorio.

<div id="table-8-generic-parameters-template" />

**Tabella 8 Modello di parametri generici**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Guida ai parametri</td>
<td>0</td>
<td>16</td>
<td>Questo campo è obbligatorio <a href="#3321-parametersguid-field">e la sezione 3.3.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello ne definiscono il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>3.3.2.1 Campo ParametersGuid

Il campo ParametersGuid deve descrivere un GUID, che determina il layout del resto della struttura dei parametri specificata.

Tutti i valori possibili per questo campo sono validi. Tuttavia, i produttori devono usare uno strumento per la generazione di GUID, ad esempio GuidGen.exe, per selezionare un GUID durante la derivazione di strutture di parametri personalizzati da questo modello.

#### <a name="333-null-parameters"></a>3.3.3 Parametri Null

La struttura Parametri Null deriva dal modello Parametri generici (vedere la sezione [3.3.2)](#332-generic-parameters-template)e deve descrivere un campo Parametri inutilizzati (vedere [la tabella 9).](#table-9-null-parameters-structure) Quando si crea o si aggiorna la struttura dei parametri OEM, le implementazioni popolano i campi parameters inutilizzati con la struttura Parametri Null. Inoltre, durante la creazione o l'aggiornamento della struttura Parameters OEM, le implementazioni devono consolidare le strutture dei parametri Null alla fine della matrice, lasciando tutte le altre strutture Parameters all'inizio della struttura Parameters OEM.

Il supporto per la struttura Dei parametri Null è obbligatorio.

<div id="table-9-null-parameters-structure" />

**Struttura dei parametri Null della tabella 9**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Guida ai parametri</td>
<td>0</td>
<td>16</td>
<td>Questo campo è obbligatorio <a href="#3331-parametersguid-field">e la sezione 3.3.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>16</td>
<td>32</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>3.3.3.1 Campo ParametersGuid

Il campo ParametersGuid deve essere conforme alla definizione fornita dal modello Parametri generici (vedere [la sezione 3.3.2.1).](#3321-parametersguid-field)

Il valore valido per questo campo, nella notazione GUID, è {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>3.3.4 Parametri flash

La struttura dei parametri Flash deriva dal modello Parametri generici (vedere la sezione [3.3.2)](#332-generic-parameters-template)e contiene i parametri per i supporti flash (vedere [la tabella 10).](#table-10-flash-parameters-structure) I produttori di dispositivi di archiviazione basati su flash possono popolare un campo Parametri (preferibilmente il campo Parametri \[ \] 0) con questa struttura di parametri. Le implementazioni possono usare le informazioni contenute nella struttura Parametri flash per ottimizzare le operazioni di accesso durante le operazioni di lettura/scrittura e per l'allineamento delle strutture file system che modificano la formattazione dei supporti.

Il supporto per la struttura Parametri Flash è facoltativo.

<div id="table-10-flash-parameters-structure" />

**Tabella 10 Struttura dei parametri flash**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Guida ai parametri</td>
<td>0</td>
<td>16</td>
<td>Questo campo è obbligatorio <a href="#3341-parametersguid-field">e la sezione 3.3.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3342-eraseblocksize-field">e la sezione 3.3.4.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3343-pagesize-field">e la sezione 3.3.4.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3344-sparesectors-field">e la sezione 3.3.4.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3345-randomaccesstime-field">e la sezione 3.3.4.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>ProgrammingTime</td>
<td>32</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3346-programmingtime-field">e la sezione 3.3.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3347-readcycle-field">e la sezione 3.3.4.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#3348-writecycle-field">e la sezione 3.3.4.8</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>44</td>
<td>4</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

Tutti i valori possibili per tutti i campi Parametri Flash, ad eccezione del campo ParametersGuid, sono validi. Tuttavia, il valore 0 indica che il campo è effettivamente senza significato (le implementazioni devono ignorare il campo specificato).

##### <a name="3341-parametersguid-field"></a>3.3.4.1 ParametersGuid Field

Il campo ParametersGuid deve essere conforme alla definizione fornita nel modello Parametri generici (vedere [la Sezione 3.3.2.1).](#3321-parametersguid-field)

Il valore valido per questo campo, nella notazione GUID, è {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}.

##### <a name="3342-eraseblocksize-field"></a>3.3.4.2 Campo EraseBlockSize

Il campo EraseBlockSize descrive le dimensioni, in byte, del blocco di cancellazione del supporto flash.

##### <a name="3343-pagesize-field"></a>3.3.4.3 Campo PageSize

Il campo PageSize descrive le dimensioni, in byte, della pagina del supporto flash.

##### <a name="3344-sparesectors-field"></a>3.3.4.4 Campo SpareSectors

Il campo SpareSectors descrive il numero di settori disponibili per le operazioni interne di sparing dei supporti flash.

##### <a name="3345-randomaccesstime-field"></a>3.3.4.5 Campo RandomAccessTime

Il campo RandomAccessTime descrive il tempo medio di accesso casuale del supporto flash, in nanosecondi.

##### <a name="3346-programmingtime-field"></a>3.3.4.6 Campo ProgrammingTime

Il campo ProgrammingTime descrive il tempo medio di programmazione del supporto flash, in nanosecondi.

##### <a name="3347-readcycle-field"></a>3.3.4.7 Campo ReadCycle

Il campo ReadCycle descrive il tempo medio del ciclo di lettura del supporto flash, in nanosecondi.

##### <a name="3348-writecycle-field"></a>3.3.4.8 Campo WriteCycle

Il campo WriteCycle descrive il tempo medio del ciclo di scrittura, in nanosecondi.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3.4 Sottoreti principali e di checksum di avvio di backup

I checksum di avvio principale e di backup contengono ognuno un modello ripetuto del checksum a quattro byte del contenuto di tutte le altre aree secondarie nelle rispettive aree di avvio. Il calcolo del checksum non deve includere i campi VolumeFlags e PercentInUse nel rispettivo settore di avvio (vedere [la figura 1).](#figure-1-boot-checksum-computation) Il modello ripetuto del checksum a quattro byte riempie la rispettiva sottoarea boot checksum dall'inizio alla fine dell'area secondaria.

Prima di usare il contenuto di una delle altre aree secondarie nelle aree Principale o Avvio backup, le implementazioni devono verificarne il contenuto convalidando il checksum di avvio corrispondente.

Mentre l'operazione di formattazione iniziale popola i checksum di avvio principale e di backup con il modello di checksum ripetuto, le implementazioni aggiornano questi settori quando il contenuto degli altri settori nelle rispettive aree di avvio cambia.

<div id="figure-1-boot-checksum-computation" />

**Figura 1 Calcolo del checksum di avvio**

```c
UInt32 BootChecksum
(
    UCHAR  * Sectors,        // points to an in-memory copy of the 11 sectors
    USHORT   BytesPerSector
)
{
    UInt32 NumberOfBytes = (UInt32)BytesPerSector * 11;
    UInt32 Checksum = 0;
    UInt32 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 106) || (Index == 107) || (Index == 112))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Sectors[Index];
    }

    return Checksum;
}
```

## <a name="4-file-allocation-table-region"></a>4 Area tabella di allocazione file

L'area Tabella di allocazione file (FAT) può contenere fino a due fat, una nella prima sottoarea FAT e l'altra nella seconda sottoarea FAT.
Il campo NumberOfFats descrive il numero di domande frequenti contenute in questa area. I valori validi per il campo NumberOfFats sono 1 e 2. Pertanto, la prima sottoarea FAT contiene sempre una fat. Se il campo NumberOfFats è due, anche la seconda sottoarea FAT contiene un file FAT.

Il campo ActiveFat del campo VolumeFlags descrive quale FAT è attivo. Solo il campo VolumeFlags nel settore di avvio principale è corrente.
Le implementazioni trattano la FAT che non è attiva come non obsoleta. L'uso della FAT inattiva e il passaggio da un fat all'altro è specifico dell'implementazione.

### <a name="41-first-and-second-fat-sub-regions"></a>4.1 Prime e seconde sottoaree FAT

Una FAT deve descrivere le catene di cluster nell'heap del cluster (vedere [la tabella 11).](#table-11-file-allocation-table-structure)
Una catena di cluster è una serie di cluster che fornisce spazio per la registrazione del contenuto di file, directory e file system strutture. Una FAT rappresenta una catena di cluster come elenco di indici del cluster collegati in modo singly. Ad eccezione delle prime due voci, ogni voce in una FAT rappresenta esattamente un cluster.

<div id="table-11-file-allocation-table-structure" />

**Tabella 11 Struttura della tabella di allocazione file**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry[0]</td>
<td>0</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#412-fatentry1-field">e la Sezione 4.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FatEntry[1]</td>
<td>4</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#412-fatentry1-field">e la Sezione 4.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>FatEntry[2]</td>
<td>8</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#413-fatentry2--fatentryclustercount1-fields">e la Sezione 4.1.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>FatEntry[ClusterCount+1]</td>
<td>(ClusterCount + 1) * 4</td>
<td>4</td>
<td><p>Questo campo è obbligatorio <a href="#413-fatentry2--fatentryclustercount1-fields">e la Sezione 4.1.3</a> ne definisce il contenuto.</p>
<p>ClusterCount + 1 non può mai superare FFFFFFF6h.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo ClusterCount.</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>(ClusterCount + 2) * 4</td>
<td>(FatLength * 2<sup>BytesPerSectorShift</sup>) – ((ClusterCount + 2) * 4)</td>
<td><p>Questo campo è obbligatorio e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi ClusterCount, FatLength e BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 Campo FatEntry \[ 0 \]

Il campo FatEntry 0 deve descrivere il tipo di supporto nel primo byte (il byte di ordine più basso) e deve contenere \[ \] FFh nei restanti tre byte.

Il tipo di supporto (il primo byte) deve essere F8h.

#### <a name="412-fatentry1-field"></a>4.1.2 Campo FatEntry \[ 1 \]

Il campo FatEntry 1 esiste solo a causa della \[ \] precedenza cronologica e non descrive alcun elemento di interesse.

Il valore valido per questo campo è FFFFFFFFh. Le implementazioni devono inizializzare questo campo sul valore prescritto e non devono usare questo campo per alcun scopo. Le implementazioni non devono interpretare questo campo e devono mantenere il contenuto tra le operazioni che modificano i campi circostanti.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] ... Campi \[ FatEntry ClusterCount+1 \]

Ogni campo FatEntry in questa matrice deve rappresentare un cluster nell'heap del cluster. FatEntry \[ 2 \] rappresenta il primo cluster nell'heap del cluster e \[ FatEntry ClusterCount+1 rappresenta l'ultimo \] cluster nell'heap del cluster.

L'intervallo valido di valori per questi campi deve essere:

- Tra 2 e ClusterCount + 1, inclusivamente, che punta al fatEntry successivo nella catena di cluster specificata; l'oggetto FatEntry specificato non deve puntare a fatEntry che lo precede nella catena di cluster specificata

- Esattamente FFFFFFF7h, che contrassegna il cluster corrispondente di FatEntry specificato come "bad"

- Esattamente FFFFFFFFh, che contrassegna il cluster corrispondente di FatEntry specificato come ultimo cluster di una catena di cluster; questo è l'unico valore valido per l'ultimo FatEntry di una catena di cluster specificata

## <a name="5-data-region"></a>5 Area dati

L'area Dati contiene l'heap del cluster, che fornisce spazio gestito per file system, directory e file.

### <a name="51-cluster-heap-sub-region"></a>5.1 Sotto-area heap cluster

La struttura dell'heap del cluster è molto semplice (vedere [la tabella 12](#table-12-cluster-heap-structure)). ogni serie consecutiva di settori descrive un cluster, come definisce il campo SectorsPerClusterShift. È importante notare che il primo cluster dell'heap del cluster ha l'indice 2, che corrisponde direttamente all'indice di FatEntry \[ \] 2.

In un volume exFAT, una bitmap di allocazione (vedere [la Sezione 7.1.5)](#715-allocation-bitmap)mantiene il record dello stato di allocazione di tutti i cluster. Si tratta di una differenza significativa rispetto ai predecessori di exFAT (FAT12, FAT16 e FAT32), in cui una FAT ha mantenuto un record dello stato di allocazione di tutti i cluster nell'heap del cluster.

<div id="table-12-cluster-heap-structure" />

**Tabella 12 Struttura dell'heap del cluster**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(settore)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(settori)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cluster[2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Questo campo è obbligatorio <a href="#511-cluster2--clusterclustercount1-fields">e la Sezione 5.1.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi ClusterHeapOffset e SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>Cluster[ClusterCount+1]</td>
<td>ClusterHeapOffset + (ClusterCount – 1) * 2<sup>SectorsPerClusterShift</sup></td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Questo campo è obbligatorio <a href="#511-cluster2--clusterclustercount1-fields">e la Sezione 5.1.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi ClusterCount, ClusterHeapOffset e SectorsPerClusterShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 Cluster \[ 2 \] ... Campi \[ Cluster ClusterCount+1 \]

Ogni campo Cluster in questa matrice è una serie di settori contigui, le cui dimensioni sono definite dal campo SectorsPerClusterShift.

## <a name="6-directory-structure"></a>6 Struttura di directory

L'file system exFAT usa un approccio ad albero di directory per gestire le file system e i file presenti nell'heap del cluster. Le directory hanno una relazione uno-a-molti tra padre e figlio nell'albero delle directory.

La directory a cui fa riferimento il campo FirstClusterOfRootDirectory è la radice dell'albero della directory. Tutte le altre directory discendono dalla directory radice in modo collegato in modo singly.

Ogni directory è costituita da una serie di voci di directory (vedere [la tabella 13](#table-13-directory-structure)).

Una o più voci di directory vengono combinate in un set di voci di directory che descrive qualcosa di interessante, ad esempio una file system, una sottodirectory o un file.

<div id="table-13-directory-structure" />

**Tabella 13 Struttura della directory**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry[0]</td>
<td>0</td>
<td>32</td>
<td>Questo campo è obbligatorio <a href="#61-directoryentry0--directoryentryn--1">e la Sezione 6.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>DirectoryEntry[N-1]</td>
<td>(N - 1) * 32</td>
<td>32</td>
<td><p>Questo campo è obbligatorio <a href="#61-directoryentry0--directoryentryn--1">e la Sezione 6.1</a> ne definisce il contenuto.</p>
<p>N, il numero di campi DirectoryEntry, è la dimensione, in byte, della catena di cluster che contiene la directory specificata, divisa per le dimensioni di un campo DirectoryEntry, 32 byte.</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6.1 DirectoryEntry \[ 0 \] ... DirectoryEntry \[ N--1\]

Ogni campo DirectoryEntry in questa matrice deriva dal modello DirectoryEntry generico (vedere [la Sezione 6.2).](#62-generic-directoryentry-template)

### <a name="62-generic-directoryentry-template"></a>6.2 Modello DirectoryEntry generico

Il modello DirectoryEntry generico fornisce la definizione di base per le voci di directory (vedere [la tabella 14).](#table-14-generic-directoryentry-template) Tutte le strutture di voci di directory derivano da questo modello e sono valide solo le strutture di voci di directory definite da Microsoft (exFAT non dispone di provisioning per le strutture di voci di directory definite dal produttore, ad eccezione di quanto definito nella Sezione [7.8](#78-vendor-extension-directory-entry) e [Sezione 7.9).](#79-vendor-allocation-directory-entry) La possibilità di interpretare il modello DirectoryEntry generico è obbligatoria.

<div id="table-14-generic-directoryentry-template" />

**Tabella 14 Modello DirectoryEntry generico**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#621-entrytype-field">e la sezione 6.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>1</td>
<td>19</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello possono definirne il contenuto.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#622-firstcluster-field">e la sezione 6.2.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#623-datalength-field">e la sezione 6.2.3</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 Campo EntryType

Il campo EntryType ha tre modalità di utilizzo definite dal valore del campo (vedere l'elenco seguente).

- 00h, che è un marcatore di fine directory e si applicano le condizioni seguenti:

  - Tutti gli altri campi nell'oggetto DirectoryEntry specificato sono effettivamente riservati

  - Anche tutte le voci di directory successive nella directory specificata sono marcatori di fine directory

  - I marcatori di fine directory sono validi solo all'esterno dei set di voci di directory

  - Le implementazioni possono sovrascrivere i marcatori di fine directory in base alle esigenze

- Tra 01h e 7Fh in modo inclusivo, che è un marcatore di voce di directory inutilizzato e si applicano le condizioni seguenti:

  - Tutti gli altri campi nell'oggetto DirectoryEntry specificato non sono effettivamente definiti

  - Le voci di directory non utilizzate sono valide solo al di fuori dei set di voci di directory

  - Le implementazioni possono sovrascrivere le voci di directory non utilizzate in base alle esigenze

  - Questo intervallo di valori corrisponde al campo InUse (vedere [la Sezione 6.2.1.4)](#6214-inuse-field)contenente il valore 0

- Tra 81h e FFh in modo inclusivo, che è una normale voce di directory e si applicano le condizioni seguenti:

  - Il contenuto del campo EntryType (vedere [la tabella 15)](#table-15-generic-entrytype-field-structure)determina il layout del resto della struttura DirectoryEntry

  - Questo intervallo di valori e solo questo intervallo di valori sono validi all'interno di un set di voci di directory

  - Questo intervallo di valori corrisponde direttamente al campo InUse (vedere [la Sezione 6.2.1.4)](#6214-inuse-field)contenente il valore 1

Per evitare modifiche al campo InUse (vedere la Sezione [6.2.1.4)](#6214-inuse-field)causando erroneamente un marcatore di fine directory, il valore 80h non è valido.

<div id="table-15-generic-entrytype-field-structure" />

**Tabella 15 Struttura del campo EntryType generico**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Questo campo è obbligatorio <a href="#6211-typecode-field">e la sezione 6.2.1.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>TypeImportance</td>
<td>5</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#6212-typeimportance-field">sezione 6.2.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>TypeCategory</td>
<td>6</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#6213-typecategory-field">e la sezione 6.2.1.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#6214-inuse-field">e la sezione 6.2.1.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>6.2.1.1 Campo TypeCode

Il campo TypeCode descrive parzialmente il tipo specifico della voce di directory specificata. Questo campo, più i campi TypeImportance e TypeCategory (vedere rispettivamente [Sezione 6.2.1.2](#6212-typeimportance-field) e [Sezione 6.2.1.3)](#6213-typecategory-field)identificano in modo univoco il tipo di voce di directory specificata.

Tutti i valori possibili di questo campo sono validi, a meno che i campi TypeImportance e TypeCategory contengano entrambi il valore 0. In tal caso, il valore 0 non è valido per questo campo.

##### <a name="6212-typeimportance-field"></a>6.2.1.2 Campo TypeImportance

Il campo TypeImportance descrive l'importanza della voce di directory specificata.

I valori validi per questo campo devono essere:

- 0, ovvero la voce di directory specificata è critica (vedere rispettivamente [Sezione 6.3.1.2.1](#63121-critical-primary-directory-entries) e [Sezione 6.4.1.2.1](#64121-critical-secondary-directory-entries) per le voci di directory primarie e secondarie critiche critiche)

- 1, ovvero la voce di directory specificata è benigna (vedere rispettivamente [Sezione 6.3.1.2.2](#63122-benign-primary-directory-entries) e [Sezione 6.4.1.2.2](#64122-benign-secondary-directory-entries) per le voci di directory secondarie non dannose)

##### <a name="6213-typecategory-field"></a>6.2.1.3 Campo TypeCategory

Il campo TypeCategory descrive la categoria della voce di directory specificata.

I valori validi per questo campo devono essere:

- 0, ovvero la voce di directory specificata è primaria (vedere [la Sezione 6.3)](#63-generic-primary-directoryentry-template)

- 1, ovvero la voce di directory specificata è secondaria (vedere [la Sezione 6.4)](#64-generic-secondary-directoryentry-template)

##### <a name="6214-inuse-field"></a>6.2.1.4 Campo InUse

Il campo InUse deve indicare se la voce di directory specificata è in uso o meno.

I valori validi per questo campo devono essere:

- 0, ovvero la voce di directory specificata non è in uso. ciò significa che la struttura specificata è effettivamente una voce di directory inutilizzata

- 1, ovvero la voce di directory specificata è in uso. ciò significa che la struttura specificata è una normale voce di directory

#### <a name="622-firstcluster-field"></a>6.2.2 Campo FirstCluster

Il campo FirstCluster deve contenere l'indice del primo cluster di un'allocazione nell'heap cluster associato alla voce di directory specificata.

L'intervallo valido di valori per questo campo deve essere:

- Esattamente 0, il che significa che non esiste alcuna allocazione del cluster

- Tra 2 e ClusterCount + 1, ovvero l'intervallo di indici del cluster validi

Le strutture che derivano da questo modello possono ridefinire entrambi i campi FirstCluster e DataLength, se un'allocazione del cluster non è compatibile con la struttura derivata.

#### <a name="623-datalength-field"></a>6.2.3 Campo DataLength

Il campo DataLength descrive le dimensioni, in byte, dei dati contenuti nell'allocazione del cluster associata.

L'intervallo di valori valido per questo campo è:

- Almeno 0; se il campo FirstCluster contiene il valore 0, l'unico valore valido di questo campo è 0

- Al massimo ClusterCount \* 2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

Le strutture che derivano da questo modello possono ridefinire entrambi i campi FirstCluster e DataLength, se non è possibile un'allocazione del cluster per la struttura derivata.

### <a name="63-generic-primary-directoryentry-template"></a>6.3 Modello directory primaria generica

La prima voce di directory in un set di voci di directory deve essere una voce di directory primaria. Tutte le voci di directory successive, se presenti, nel set di voci di directory devono essere voci di directory secondarie (vedere [la Sezione 6.4).](#64-generic-secondary-directoryentry-template)

La possibilità di interpretare il modello DirectoryEntry primario generico è obbligatoria.

Tutte le strutture di voci di directory primarie derivano dal modello DirectoryEntry primario generico (vedere la tabella [16),](#table-16-generic-primary-directoryentry-template)che deriva dal modello DirectoryEntry generico (vedere la Sezione [6.2).](#62-generic-directoryentry-template)

<div id="table-16-generic-primary-directoryentry-template" />

**Tabella 16 Generic Primary DirectoryEntry Template**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#631-entrytype-field">e la sezione 6.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#632-secondarycount-field">e la sezione 6.3.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#633-setchecksum-field">e la sezione 6.3.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#634-generalprimaryflags-field">e la sezione 6.3.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>6</td>
<td>14</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello ne definiscono il contenuto.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#635-firstcluster-field">e la sezione 6.3.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#636-datalength-field">e la sezione 6.3.6</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>6.3.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1).](#621-entrytype-field)

##### <a name="6311-typecode-field"></a>6.3.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1.1).](#6211-typecode-field)

##### <a name="6312-typeimportance-field"></a>6.3.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1.2).](#6212-typeimportance-field)

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 Voci di directory primarie critiche

Le voci di directory primarie critiche contengono informazioni fondamentali per la corretta gestione di un volume exFAT. Solo la directory radice contiene voci di directory primarie critiche (le voci della directory file sono un'eccezione, vedere [la Sezione 7.4).](#74-file-directory-entry)

La definizione di voci di directory primarie critiche è correlata al numero di revisione exFAT principale. Le implementazioni devono supportare tutte le voci di directory primarie critiche e devono registrare solo le strutture di voci di directory primarie critiche definite da questa specifica.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 Voci di directory primarie non valide

Le voci della directory primaria non dannose contengono informazioni aggiuntive che possono essere utili per la gestione di un volume exFAT. Qualsiasi directory può contenere voci di directory primarie non valide.

La definizione di voci di directory primarie non dannose è correlata al numero di revisione exFAT secondario. Il supporto per qualsiasi voce di directory primaria non valida definita da questa specifica o da qualsiasi specifica successiva è facoltativo. Una voce di directory primaria non riconosciuta esegue il rendering dell'intero set di voci di directory come non riconosciuto (oltre la definizione dei modelli di voce di directory applicabili).

##### <a name="6313-typecategory-field"></a>6.3.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1.3).](#6213-typecategory-field)

Per questo modello, il valore valido per questo campo deve essere 0.

##### <a name="6314-inuse-field"></a>6.3.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1.4).](#6214-inuse-field)

#### <a name="632-secondarycount-field"></a>6.3.2 Campo SecondaryCount

Il campo SecondaryCount descrive il numero di voci di directory secondarie che seguono immediatamente la voce di directory primaria specificata. Queste voci della directory secondaria, insieme alla voce di directory primaria specificata, costituiscono il set di voci di directory.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 0, ovvero questa voce di directory primaria è l'unica voce nel set di voci di directory

- Al massimo 255, ovvero le 255 voci di directory seguenti e questa voce di directory primaria comprendono il set di voci di directory

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire entrambi i campi SecondaryCount e SetChecksum.

#### <a name="633-setchecksum-field"></a>6.3.3 Campo SetChecksum

Il campo SetChecksum deve contenere il checksum di tutte le voci di directory nel set di voci di directory specificato. Tuttavia, il checksum esclude questo campo (vedere [la figura 2).](#figure-2-entrysetchecksum-computation) Le implementazioni verificano che il contenuto di questo campo sia valido prima di usare qualsiasi altra voce di directory nel set di voci di directory specificato.

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire entrambi i campi SecondaryCount e SetChecksum.

<div id="figure-2-entrysetchecksum-computation" />

**Figura 2 Calcolo entrySetChecksum**

```C
UInt16 EntrySetChecksum
(
    UCHAR * Entries,       // points to an in-memory copy of the directory entry set
    UCHAR   SecondaryCount
)
{
    UInt16 NumberOfBytes = ((UInt16)SecondaryCount + 1) * 32;
    UInt16 Checksum = 0;
    UInt16 Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        if ((Index == 2) || (Index == 3))
        {
            continue;
        }
        Checksum = ((Checksum&1) ? 0x8000 : 0) + (Checksum>>1) +  (UInt16)Entries[Index];
    }
    return Checksum;
}
```

#### <a name="634-generalprimaryflags-field"></a>6.3.4 Campo GeneralPrimaryFlags

Il campo GeneralPrimaryFlags contiene flag (vedere [la tabella 17).](#table-17-generic-generalprimaryflags-field-structure)

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire questo campo.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Tabella 17 Struttura dei campi Generic GeneralPrimaryFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#6341-allocationpossible-field">e la sezione 6.3.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#6342-nofatchain-field">e la sezione 6.3.4.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello possono definire questo campo.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>6.3.4.1 AllocationPossible Field

Il campo AllocationPossible deve indicare se è possibile o meno un'allocazione nell'heap del cluster per la voce di directory specificata.

I valori validi per questo campo devono essere:

- 0, ovvero un'allocazione associata di cluster non è possibile e i campi FirstCluster e DataLength non sono effettivamente definiti (le strutture che derivano da questo modello possono ridefinire tali campi)

- 1, ovvero è possibile un'allocazione associata di cluster e che i campi FirstCluster e DataLength sono definiti

##### <a name="6342-nofatchain-field"></a>6.3.4.2 Campo NoFatChain

Il campo NoFatChain indica se la FAT attiva descrive o meno la catena di cluster dell'allocazione specificata.

I valori validi per questo campo devono essere:

- 0, ovvero le voci FAT corrispondenti per la catena di cluster dell'allocazione sono valide e le implementazioni le interpretano; se il campo AllocationPossible contiene il valore 0 o se il campo AllocationPossible contiene il valore 1 e il campo FirstCluster contiene il valore 0, l'unico valore valido di questo campo è 0

- 1, ovvero l'allocazione associata è una serie contigua di cluster. le voci FAT corrispondenti per i cluster non sono valide e le implementazioni non le interpretano. Le implementazioni possono usare l'equazione seguente per calcolare le dimensioni dell'allocazione associata: DataLength / (2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>) arrotondato per es.

Se le strutture di voci di directory primarie critiche che derivano da questo modello ridefinino il campo GeneralPrimaryFlags, le voci FAT corrispondenti per la catena di cluster dell'allocazione associata sono valide.

#### <a name="635-firstcluster-field"></a>6.3.5 Campo FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.2).](#622-firstcluster-field)

Se il bit NoFatChain è 1, FirstCluster deve puntare a un cluster valido nell'heap del cluster.

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire i campi FirstCluster e DataLength. Altre strutture che derivano da questo modello possono ridefinire i campi FirstCluster e DataLength solo se il campo AllocationPossible contiene il valore 0.

#### <a name="636-datalength-field"></a>6.3.6 Campo DataLength

Il campo DataLength deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.3).](#623-datalength-field)

Se il bit NoFatChain è 1, DataLength non deve essere zero. Se il campo FirstCluster è zero, anche DataLength deve essere zero.

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire i campi FirstCluster e DataLength. Altre strutture che derivano da questo modello possono ridefinire i campi FirstCluster e DataLength solo se il campo AllocationPossible contiene il valore 0.

### <a name="64-generic-secondary-directoryentry-template"></a>6.4 Modello DirectoryEntry secondario generico

Lo scopo principale delle voci di directory secondarie è fornire informazioni aggiuntive su un set di voci di directory. La possibilità di interpretare il modello DirectoryEntry secondario generico è obbligatoria.

La definizione di voci di directory secondarie critiche e non dannose è correlata al numero di revisione secondario exFAT. Il supporto per qualsiasi voce di directory secondaria critica o non valida definita da questa specifica o da specifiche successive è facoltativo.

Tutte le strutture di voci di directory secondarie derivano dal modello DirectoryEntry secondario generico (vedere la tabella [18](#table-18-generic-secondary-directoryentry-template)), che deriva dal modello DirectoryEntry generico (vedere la Sezione [6.2).](#62-generic-directoryentry-template)

<div id="table-18-generic-secondary-directoryentry-template" />

**Tabella 18 Modello directory secondaria generica**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#641-entrytype-field">sezione 6.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#642-generalsecondaryflags-field">e la sezione 6.4.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>18</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello ne definiscono il contenuto.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#643-firstcluster-field">e la sezione 6.4.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#644-datalength-field">e la sezione 6.4.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>6.4.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1)](#621-entrytype-field)

##### <a name="6411-typecode-field"></a>6.4.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1.1).](#6211-typecode-field)

##### <a name="6412-typeimportance-field"></a>6.4.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la Sezione 6.2.1.2).](#6212-typeimportance-field)

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 Voci di directory secondarie critiche

Le voci di directory secondarie critiche contengono informazioni fondamentali per la gestione appropriata del relativo set di voci di directory contenitore.
Anche se il supporto per qualsiasi voce di directory secondaria critica specifica è facoltativo, una voce di directory critica non riconosciuta rende non riconosciuto l'intero set di voci di directory (oltre la definizione dei modelli di voce di directory applicabili).

Tuttavia, se un set di voci di directory contiene almeno una voce di directory secondaria critica che un'implementazione non riconosce, l'implementazione interpreterà al massimo i modelli delle voci di directory nel set di voci di directory e non i dati associati a qualsiasi voce di directory nel set di voci di directory (le voci della directory file sono un'eccezione, vedere la sezione [7.4).](#74-file-directory-entry)

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 Voci di directory secondarie non dannose

Le voci di directory secondarie non dannose contengono informazioni aggiuntive che possono essere utili per la gestione del relativo set di voci di directory contenitore. Il supporto per qualsiasi voce di directory secondaria non dannosa specifica è facoltativo.
Le voci di directory secondarie non riconoscite non vengono riconosciate come non riconoscite per l'intero set di voci di directory.

Le implementazioni possono ignorare qualsiasi voce secondaria non dannosa che non riconosce.

##### <a name="6413-typecategory-field"></a>6.4.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la sezione 6.2.1.3).](#6213-typecategory-field)

Per questo modello, il valore valido per questo campo è 1.

##### <a name="6414-inuse-field"></a>6.4.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la sezione 6.2.1.4).](#6214-inuse-field)

#### <a name="642-generalsecondaryflags-field"></a>6.4.2 Campo GeneralSecondaryFlags

Il campo GeneralSecondaryFlags contiene flag (vedere [la tabella 19).](#table-19-generic-generalsecondaryflags-field-structure)

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Tabella 19 Struttura dei campi Generic GeneralSecondaryFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#6421-allocationpossible-field">e la sezione 6.4.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#6422-nofatchain-field">e la sezione 6.4.2.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello possono definire questo campo.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>6.4.2.1 Campo AllocationPossible

Il campo AllocationPossible deve avere la stessa definizione del campo con lo stesso nome nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.4.1).](#6341-allocationpossible-field)

##### <a name="6422-nofatchain-field"></a>6.4.2.2 Campo NoFatChain

Il campo NoFatChain deve avere la stessa definizione del campo con lo stesso nome nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.4.2).](#6342-nofatchain-field)

#### <a name="643-firstcluster-field"></a>6.4.3 Campo FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la sezione 6.2.2).](#622-firstcluster-field)

Se il bit NoFatChain è 1, FirstCluster deve puntare a un cluster valido nell'heap del cluster.

#### <a name="644-datalength-field"></a>6.4.4 Campo DataLength

Il campo DataLength deve essere conforme alla definizione fornita nel modello DirectoryEntry generico (vedere [la sezione 6.2.3).](#623-datalength-field)

Se il bit NoFatChain è 1, DataLength non deve essere zero. Se il campo FirstCluster è zero, anche DataLength deve essere zero.

## <a name="7-directory-entry-definitions"></a>7 Definizioni delle voci di directory

La revisione 1.00 del file system exFAT definisce le voci di directory seguenti:

- Primario critico

  - Bitmap di allocazione ([Sezione 7.1](#71-allocation-bitmap-directory-entry))

  - Tabella up-case ([Sezione 7.2](#72-up-case-table-directory-entry))

  - Etichetta di volume ([Sezione 7.3](#73-volume-label-directory-entry))

  - File ([Sezione 7.4](#74-file-directory-entry))

- Primario non dannoso

  - GUID volume ([Sezione 7.5](#75-volume-guid-directory-entry))

  - Riempimento TexFAT ([Sezione 7.10](#710-texfat-padding-directory-entry))

<!-- -->

- Secondario critico

  - Estensione stream ([Sezione 7.6](#76-stream-extension-directory-entry))

  - Nome file ([Sezione 7.7](#77-file-name-directory-entry))

- Secondario non dannoso

  - Estensione del fornitore ([Sezione 7.8](#78-vendor-extension-directory-entry))

  - Allocazione del fornitore ([Sezione 7.9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7.1 Voce di directory bitmap di allocazione

Nella tabella exFAT file system fat non descrive lo stato di allocazione dei cluster. invece di una bitmap di allocazione. Le bitmap di allocazione sono presenti nell'heap del cluster (vedere la sezione [7.1.5)](#715-allocation-bitmap)e hanno voci di directory primarie critiche corrispondenti nella directory radice (vedere [la tabella 20).](#table-20-allocation-bitmap-directoryentry-structure)

Il campo NumberOfFats determina il numero di voci di directory Allocation Bitmap valide nella directory radice. Se il campo NumberOfFats contiene il valore 1, l'unico numero valido di voci di directory Allocation Bitmap è 1. Inoltre, la voce di directory Allocation Bitmap (Bitmap di allocazione) è valida solo se descrive la prima bitmap di allocazione (vedere [la sezione 7.1.2.1).](#7121-bitmapidentifier-field) Se il campo NumberOfFats contiene il valore 2, l'unico numero valido di voci di directory Allocation Bitmap è 2.
Inoltre, le due voci della directory Allocation Bitmap sono valide solo se una descrive la prima bitmap di allocazione e l'altra descrive la seconda bitmap di allocazione.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Tabella 20 Struttura DirectoryEntry della bitmap allocation**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#711-entrytype-field">e la sezione 7.1.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#712-bitmapflags-field">e la sezione 7.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>2</td>
<td>18</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#713-firstcluster-field">e la sezione 7.1.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#714-datalength-field">e la sezione 7.1.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>7.1.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1).](#631-entrytype-field)

##### <a name="7111-typecode-field"></a>7.1.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.1).](#6311-typecode-field)

Per una voce della directory Allocation Bitmap, il valore valido per questo campo è 1.

##### <a name="7112-typeimportance-field"></a>7.1.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.2).](#6312-typeimportance-field)

Per una voce della directory Allocation Bitmap, il valore valido per questo campo è 0.

##### <a name="7113-typecategory-field"></a>7.1.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.3).](#6313-typecategory-field)

##### <a name="7114-inuse-field"></a>7.1.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.4).](#6314-inuse-field)

#### <a name="712-bitmapflags-field"></a>7.1.2 Campo BitmapFlags

Il campo BitmapFlags contiene flag (vedere [la tabella 21).](#table-21-bitmapflags-field-structure)

<div id="table-21-bitmapflags-field-structure" />

**Tabella 21 Struttura del campo BitmapFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#7121-bitmapidentifier-field">e la sezione 7.1.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>1</td>
<td>7</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>7.1.2.1 Campo BitmapIdentifier

Il campo BitmapIdentifier indicherà la bitmap di allocazione descritta dalla voce di directory specificata. Le implementazioni devono usare la prima bitmap di allocazione in combinazione con il primo FAT e useranno la seconda bitmap di allocazione insieme al secondo FAT. Il campo ActiveFat descrive quali fat e bitmap di allocazione sono attivi.

I valori validi per questo campo devono essere:

- 0, ovvero la voce di directory specificata descrive la prima bitmap di allocazione

- 1, ovvero la voce di directory specificata descrive la seconda bitmap di allocazione ed è possibile solo quando NumberOfFats contiene il valore 2

#### <a name="713-firstcluster-field"></a>7.1.3 Campo FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.5).](#635-firstcluster-field)

Questo campo contiene l'indice del primo cluster della catena di cluster, come descritto dal FAT, che ospita la bitmap di allocazione.

#### <a name="714-datalength-field"></a>7.1.4 Campo DataLength

Il campo DataCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry primaria generica (vedere [la sezione 6.3.6).](#636-datalength-field)

#### <a name="715-allocation-bitmap"></a>7.1.5 Bitmap di allocazione

Una bitmap di allocazione registra lo stato di allocazione dei cluster nell'heap del cluster. Ogni bit in una bitmap di allocazione indica se il cluster corrispondente è disponibile per l'allocazione o meno.

Una bitmap di allocazione rappresenta i cluster dall'indice più basso a quello più alto (vedere [la tabella 22).](#table-22-allocation-bitmap-structure) Per motivi cronologici, il primo cluster ha l'indice 2.
Nota: il primo bit nella bitmap è il bit più basso del primo byte.

<div id="table-22-allocation-bitmap-structure" />

**Tabella 22 Struttura della bitmap di allocazione**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry[2]</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">la sezione 7.1.5.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="odd">
<td>BitmapEntry[ClusterCount+1]</td>
<td>ClusterCount - 1</td>
<td>1</td>
<td><p>Questo campo è obbligatorio <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">e la sezione 7.1.5.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori principale e di avvio del backup contengono entrambi il campo ClusterCount.</p></td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>ClusterCount</td>
<td>(DataLength * 8) - ClusterCount</td>
<td><p>Questo campo è obbligatorio e il relativo contenuto, se presente, è riservato.</p>
<p>Nota: i settori principale e di avvio del backup contengono entrambi il campo ClusterCount.</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ 2 \] ... Campi BitmapEntry \[ ClusterCount+1 \]

Ogni campo BitmapEntry in questa matrice rappresenta un cluster nell'heap del cluster. BitmapEntry \[ 2 \] rappresenta il primo cluster nell'heap del cluster e BitmapEntry \[ ClusterCount+1 rappresenta \] l'ultimo cluster nell'heap del cluster.

I valori validi per questi campi devono essere:

- 0, che descrive il cluster corrispondente come disponibile per l'allocazione

- 1, che descrive il cluster corrispondente come non disponibile per l'allocazione (un'allocazione del cluster potrebbe già utilizzare il cluster corrispondente o il fat attivo può descrivere il cluster corrispondente come non eroso)

### <a name="72-up-case-table-directory-entry"></a>7.2 Voce della directory della tabella up-case

La tabella Up-case definisce la conversione da caratteri minuscoli a caratteri maiuscoli. Ciò è importante perché la voce di directory Nome file (vedere la sezione 7.7) usa caratteri Unicode e il file system exFAT non fa distinzione tra maiuscole e minuscole e non fa distinzione tra maiuscole e minuscole. La tabella Up-case esiste nell'heap del cluster (vedere la sezione [7.2.5)](#725-up-case-table)e ha una voce di directory primaria critica corrispondente nella directory radice (vedere [la tabella 23).](#table-23-up-case-table-directoryentry-structure) Il numero valido di voci della directory Tabella maiuscole/minuscole è 1.

A causa della relazione tra la tabella Up-case e i nomi di file, le implementazioni non devono modificare la tabella Up-case, tranne in seguito a operazioni di formattazione.

<div id="table-23-up-case-table-directoryentry-structure" />

**Tabella 23 Struttura DirectoryEntry della tabella up case**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#721-entrytype-field">e la sezione 7.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="odd">
<td>TableChecksum</td>
<td>4</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#722-tablechecksum-field">e la sezione 7.2.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#723-firstcluster-field">e la sezione 7.2.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#724-datalength-field">e la sezione 7.2.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>7.2.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1).](#631-entrytype-field)

##### <a name="7211-typecode-field"></a>7.2.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.1).](#6311-typecode-field)

Per la voce della directory Tabella up case, il valore valido per questo campo è
2.

##### <a name="7212-typeimportance-field"></a>7.2.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.2).](#6312-typeimportance-field)

Per la voce della directory Tabella up case, il valore valido per questo campo è
0.

##### <a name="7213-typecategory-field"></a>7.2.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.3).](#6313-typecategory-field)

##### <a name="7214-inuse-field"></a>7.2.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.4).](#6314-inuse-field)

#### <a name="722-tablechecksum-field"></a>7.2.2 Campo TableChecksum

Il campo TableChecksum contiene il checksum della tabella Up-case (descritta dai campi FirstCluster e DataLength). Le implementazioni verificano che il contenuto di questo campo sia valido prima di usare la tabella Up-case.

<div id="figure-3-tablechecksum-computation" />

**Figura 3 Calcolo tableChecksum**

```C
UInt32 TableChecksum
(
    UCHAR  * Table,    // points to an in-memory copy of the up-case table
    UInt64   DataLength
)
{
    UInt32 Checksum = 0;
    UInt64 Index;

    for (Index = 0; Index < DataLength; Index++)
    {
        Checksum = ((Checksum&1) ? 0x80000000 : 0) + (Checksum>>1) + (UInt32)Table[Index];
    }

    return Checksum;
}
```

#### <a name="723-firstcluster-field"></a>7.2.3 Campo FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.5).](#635-firstcluster-field)

Questo campo contiene l'indice del primo cluster della catena di cluster, come descritto dal fat, che ospita la tabella Up-case.

#### <a name="724-datalength-field"></a>7.2.4 Campo DataLength

Il campo DataCluster deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.6).](#636-datalength-field)

#### <a name="725-up-case-table"></a>7.2.5 Tabella up case

Una tabella up-case è una serie di mapping di caratteri Unicode. Un mapping dei caratteri è costituito da un campo a 2 byte, con l'indice del campo nella tabella maiuscole/minuscole che rappresenta il carattere Unicode di cui eseguire l'up-case e il campo a 2 byte che rappresenta il carattere Unicode con distinzione tra maiuscole e minuscole.

I primi 128 caratteri Unicode hanno mapping obbligatori (vedere [la tabella 24).](#table-24-mandatory-first-128-up-case-table-entries)
Una tabella up-case con qualsiasi altro mapping di caratteri per i primi 128 caratteri Unicode non è valida.

Le implementazioni che supportano solo caratteri dell'intervallo di mapping obbligatorio possono ignorare i mapping del resto della tabella up-case. Tali implementazioni devono usare solo caratteri dell'intervallo di mapping obbligatorio durante la creazione o la ridenominazione dei file (tramite la voce di directory Nome file, vedere [la sezione 7.7).](#77-file-name-directory-entry) Quando si esegue l'up-casing dei nomi di file esistenti, tali implementazioni non devono eseguire l'up-case dei caratteri dell'intervallo di mapping non obbligatorio, ma devono lasciarli intatti nel nome file con distinzione tra maiuscole e minuscole risultante (si tratta di un up-casing parziale). Durante il confronto dei nomi di file, tali implementazioni devono considerare equivalenti i nomi di file che differiscono dal nome confrontato solo con i caratteri Unicode dell'intervallo di mapping non obbligatorio. Anche se tali nomi di file sono potenzialmente equivalenti, tali implementazioni non possono garantire che il nome di file completamente con distinzione tra maiuscole e minuscole non sia in conflitto con il nome in fase di confronto.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tabella 24 Prime 128 voci obbligatorie della tabella up case**

| Indice di tabella | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| **0000h**       | 0000h             | 0001h     | 0002h     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002 Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040h**       | 0040h             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**Nota: le voci con mapping di maiuscole/minuscole senza identità sono in grassetto.**

Durante la formattazione di un volume, le implementazioni possono generare una tabella up-case in un formato compresso usando la compressione del mapping di identità, poiché gran parte dello spazio dei caratteri Unicode non ha alcun concetto di distinzione tra maiuscole e minuscole (il che significa che i caratteri "minuscoli" e "maiuscoli" sono equivalenti).
Le implementazioni comprimeno una tabella up case rappresentando una serie di mapping di identità con il valore FFFFh seguito dal numero di mapping di identità.

Ad esempio, un'implementazione può rappresentare i primi mapping di 100 caratteri (64 ore) con le otto voci seguenti di una tabella up case compressa:

> FFFFh, 0061h, 0041h, 0042h, 0043h

Le prime due voci indicano che i primi 97 (61h) caratteri (da 0000h a 0060h) hanno mapping di identità. I caratteri successivi, da 0061h a 0063h, vengono mappati rispettivamente ai caratteri da 0041h a 0043h.

La possibilità di fornire una tabella up case compressa al momento della formattazione di un volume è facoltativa. Tuttavia, la possibilità di interpretare sia una tabella non compressa che una tabella up-case compressa è obbligatoria. Il valore del campo TableChecksum è sempre conforme alla modalità di esistenza della tabella up case nel volume, che può essere in formato compresso o non compresso.

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1 Tabella up case consigliata

Quando si formatta un volume, le implementazioni devono registrare la tabella up-case consigliata in formato compresso (vedere la tabella [25](#table-25-recommended-up-case-table-in-compressed-format)), per cui il valore del campo TableChecksum è E619D30Dh.

Se un'implementazione definisce la propria tabella up-case, compressa o non compressa, tale tabella dovrà coprire l'intervallo di caratteri Unicode completo (dai codici carattere 0000h a FFFFh inclusi).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tabella 25 Tabella up case consigliata in formato compresso**

| Offset non elaborato | + 0 |  + 1       |  + 2       |  + 3       |  + 4       | + 5        |  + 6       | + 7        |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
| **0000h**      | 0000h                        | 0001h   | 0002h   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002 Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040h**      | 0040h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0048h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0050h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0058h**      | 0058h                        | 0059h   | 005Ah   | 005Bh   | 005Ch   | 005Dh   | 005Eh   | 005Fh   |
| **0060h**      | 0060h                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
| **0068h**      | 0048h                        | 0049h   | 004Ah   | 004Bh   | 004Ch   | 004Dh   | 004Eh   | 004Fh   |
| **0070h**      | 0050h                        | 0051h   | 0052h   | 0053h   | 0054h   | 0055h   | 0056h   | 0057h   |
| **0078h**      | 0058h                        | 0059h   | 005Ah   | 007Bh   | 007Ch   | 007Dh   | 007Eh   | 007Fh   |
| **0080h**      | 0080h                        | 0081h   | 0082h   | 0083h   | 0084h   | 0085h   | 0086h   | 0087h   |
| **0088h**      | 0088h                        | 0089h   | 008Ah   | 008Bh   | 008Ch   | 008Dh   | 008Eh   | 008Fh   |
| **0090h**      | 0090h                        | 0091h   | 0092h   | 0093h   | 0094h   | 0095h   | 0096h   | 0097h   |
| **0098h**      | 0098h                        | 0099h   | 009Ah   | 009Bh   | 009Ch   | 009 Dh   | 009Eh   | 009Fh   |
| **00A0h**      | 00A0h                        | 00A1h   | 00A2h   | 00A3h   | 00A4h   | 00A5h   | 00A6h   | 00A7h   |
| **00A8h**      | 00A8h                        | 00A9h   | 00AAh   | 00ABh   | 00ACh   | 00ADh   | 00AEh   | 00AFh   |
| **00B0h**      | 00B0h                        | 00B1h   | 00B2h   | 00B3h   | 00B4h   | 00B5h   | 00B6h   | 00B7h   |
| **00B8h**      | 00B8h                        | 00B9h   | 00BAh   | 00BBh   | 00BCh   | 00BDh   | 00BEh   | 00BFh   |
| **00C0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00C8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00D0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00D7h   |
| **00D8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00 DCh   | 00DDh   | 00DEh   | 00DFh   |
| **00E0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00E8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00F0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00F7h   |
| **00F8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00 DCh   | 00DDh   | 00DEh   | 0178h   |
| **0100h**      | 0100h                        | 0100h   | 0102h   | 0102h   | 0104h   | 0104h   | 0106h   | 0106h   |
| **0108h**      | 0108h                        | 0108h   | 010Ah   | 010Ah   | 010Ch   | 010Ch   | 010Eh   | 010Eh   |
| **0110h**      | 0110h                        | 0110h   | 0112h   | 0112h   | 0114h   | 0114h   | 0116h   | 0116h   |
| **0118h**      | 0118h                        | 0118h   | 011Ah   | 011Ah   | 011Ch   | 011Ch   | 011Eh   | 011Eh   |
| **0120h**      | 0120h                        | 0120h   | 0122h   | 0122h   | 0124h   | 0124h   | 0126h   | 0126h   |
| **0128h**      | 0128h                        | 0128h   | 012Ah   | 012Ah   | 012Ch   | 012Ch   | 012Eh   | 012Eh   |
| **0130h**      | 0130h                        | 0131h   | 0132h   | 0132h   | 0134h   | 0134h   | 0136h   | 0136h   |
| **0138h**      | 0138h                        | 0139h   | 0139h   | 013Bh   | 013Bh   | 013Dh   | 013Dh   | 013Fh   |
| **0140h**      | 013Fh                        | 0141h   | 0141h   | 0143h   | 0143h   | 0145h   | 0145h   | 0147h   |
| **0148h**      | 0147h                        | 0149h   | 014Ah   | 014Ah   | 014Ch   | 014Ch   | 014Eh   | 014Eh   |
| **0150h**      | 0150h                        | 0150h   | 0152h   | 0152h   | 0154h   | 0154h   | 0156h   | 0156h   |
| **0158h**      | 0158h                        | 0158h   | 015Ah   | 015Ah   | 015Ch   | 015Ch   | 015Eh   | 015Eh   |
| **0160h**      | 0160h                        | 0160h   | 0162h   | 0162h   | 0164h   | 0164h   | 0166h   | 0166h   |
| **0168h**      | 0168h                        | 0168h   | 016Ah   | 016Ah   | 016Ch   | 016Ch   | 016Eh   | 016Eh   |
| **0170h**      | 0170h                        | 0170h   | 0172h   | 0172h   | 0174h   | 0174h   | 0176h   | 0176h   |
| **0178h**      | 0178h                        | 0179h   | 0179h   | 017Bh   | 017Bh   | 017Dh   | 017Dh   | 017Fh   |
| **0180h**      | 0243h                        | 0181h   | 0182h   | 0182h   | 0184h   | 0184h   | 0186h   | 0187h   |
| **0188h**      | 0187h                        | 0189h   | 018Ah   | 018Bh   | 018Bh   | 018Dh   | 018Eh   | 018Fh   |
| **0190h**      | 0190h                        | 0191h   | 0191h   | 0193h   | 0194h   | 01F6h   | 0196h   | 0197h   |
| **0198h**      | 0198h                        | 0198h   | 023Dh   | 019Bh   | 019Ch   | 019Dh   | 0220h   | 019Fh   |
| **01A0h**      | 01A0h                        | 01A0h   | 01A2h   | 01A2h   | 01A4h   | 01A4h   | 01A6h   | 01A7h   |
| **01A8h**      | 01A7h                        | 01A9h   | 01AAh   | 01ABh   | 01ACh   | 01ACh   | 01AEh   | 01AFh   |
| **01B0h**      | 01AFh                        | 01B1h   | 01B2h   | 01B3h   | 01B3h   | 01B5h   | 01B5h   | 01B7h   |
| **01B8h**      | 01B8h                        | 01B8h   | 01BAh   | 01BBh   | 01BCh   | 01BCh   | 01BEh   | 01F7h   |
| **01C0h**      | 01C0h                        | 01C1h   | 01C2h   | 01C3h   | 01C4h   | 01C5h   | 01C4h   | 01C7h   |
| **01C8h**      | 01C8h                        | 01C7h   | 01CAh   | 01CBh   | 01CAh   | 01CDh   | 01CDh   | 01CFh   |
| **01D0h**      | 01CFh                        | 01D1h   | 01D1h   | 01D3h   | 01D3h   | 01D5h   | 01D5h   | 01D7h   |
| **01D8h**      | 01D7h                        | 01D9h   | 01D9h   | 01DBh   | 01DBh   | 018Eh   | 01DEh   | 01DEh   |
| **01E0h**      | 01E0h                        | 01E0h   | 01E2h   | 01E2h   | 01E4h   | 01E4h   | 01E6h   | 01E6h   |
| **01E8h**      | 01E8h                        | 01E8h   | 01EAh   | 01EAh   | 01ECh   | 01ECh   | 01EEh   | 01EEh   |
| **01F0h**      | 01F0h                        | 01F1h   | 01F2h   | 01F1h   | 01F4h   | 01F4h   | 01F6h   | 01F7h   |
| **01F8h**      | 01F8h                        | 01F8h   | 01FAh   | 01FAh   | 01FCh   | 01FCh   | 01FEh   | 01FEh   |
| **0200h**      | 0200h                        | 0200h   | 0202h   | 0202h   | 0204h   | 0204h   | 0206h   | 0206h   |
| **0208h**      | 0208h                        | 0208h   | 020Ah   | 020Ah   | 020Ch   | 020Ch   | 020Eh   | 020Eh   |
| **0210h**      | 0210h                        | 0210h   | 0212h   | 0212h   | 0214h   | 0214h   | 0216h   | 0216h   |
| **0218h**      | 0218h                        | 0218h   | 021Ah   | 021Ah   | 021Ch   | 021Ch   | 021Eh   | 021Eh   |
| **0220h**      | 0220h                        | 0221h   | 0222h   | 0222h   | 0224h   | 0224h   | 0226h   | 0226h   |
| **0228h**      | 0228h                        | 0228h   | 022Ah   | 022Ah   | 022Ch   | 022Ch   | 022Eh   | 022Eh   |
| **0230h**      | 0230h                        | 0230h   | 0232h   | 0232h   | 0234h   | 0235h   | 0236h   | 0237h   |
| **0238h**      | 0238h                        | 0239h   | 2C65h   | 023Bh   | 023Bh   | 023Dh   | 2C66h   | 023Fh   |
| **0240h**      | 0240h                        | 0241h   | 0241h   | 0243h   | 0244h   | 0245h   | 0246h   | 0246h   |
| **0248h**      | 0248h                        | 0248h   | 024Ah   | 024Ah   | 024Ch   | 024Ch   | 024Eh   | 024Eh   |
| **0250h**      | 0250h                        | 0251h   | 0252h   | 0181h   | 0186h   | 0255h   | 0189h   | 018Ah   |
| **0258h**      | 0258h                        | 018Fh   | 025Ah   | 0190h   | 025Ch   | 025Dh   | 025Eh   | 025Fh   |
| **0260h**      | 0193h                        | 0261h   | 0262h   | 0194h   | 0264h   | 0265h   | 0266h   | 0267h   |
| **0268h**      | 0197h                        | 0196h   | 026Ah   | 2C62h   | 026Ch   | 026Dh   | 026Eh   | 019Ch   |
| **0270h**      | 0270h                        | 0271h   | 019Dh   | 0273h   | 0274h   | 019Fh   | 0276h   | 0277h   |
| **0278h**      | 0278h                        | 0279h   | 027Ah   | 027Bh   | 027Ch   | 2C64h   | 027Eh   | 027Fh   |
| **0280h**      | 01A6h                        | 0281h   | 0282h   | 01A9h   | 0284h   | 0285h   | 0286h   | 0287h   |
| **0288h**      | 01AEh                        | 0244h   | 01B1h   | 01B2h   | 0245h   | 028Dh   | 028Eh   | 028Fh   |
| **0290h**      | 0290h                        | 0291h   | 01B7h   | 0293h   | 0294h   | 0295h   | 0296h   | 0297h   |
| **0298h**      | 0298h                        | 0299h   | 029Ah   | 029Bh   | 029Ch   | 029Dh   | 029Eh   | 029Fh   |
| **02A0h**      | 02A0h                        | 02A1h   | 02A2h   | 02A3h   | 02A4h   | 02A5h   | 02A6h   | 02A7h   |
| **02A8h**      | 02A8h                        | 02A9h   | 02AAh   | 02ABh   | 02ACh   | 02ADh   | 02AEh   | 02AFh   |
| **02B0h**      | 02B0h                        | 02B1h   | 02B2h   | 02B3h   | 02B4h   | 02B5h   | 02B6h   | 02B7h   |
| **02B8h**      | 02B8h                        | 02B9h   | 02BAh   | 02BBh   | 02BCh   | 02BDh   | 02BEh   | 02BFh   |
| **02C0h**      | 02C0h                        | 02C1h   | 02C2h   | 02C3h   | 02C4h   | 02C5h   | 02C6h   | 02C7h   |
| **02C8h**      | 02C8h                        | 02C9h   | 02CAh   | 02CBh   | 02CCh   | 02CDh   | 02CEh   | 02CFh   |
| **02D0h**      | 02D0h                        | 02D1h   | 02D2h   | 02D3h   | 02D4h   | 02D5h   | 02D6h   | 02D7h   |
| **02D8h**      | 02D8h                        | 02D9h   | 02DAh   | 02DBh   | 02DCh   | 02DDh   | 02DEh   | 02DFh   |
| **02E0h**      | 02E0h                        | 02E1h   | 02E2h   | 02E3h   | 02E4h   | 02E5h   | 02E6h   | 02E7h   |
| **02E8h**      | 02E8h                        | 02E9h   | 02EAh   | 02EBh   | 02ECh   | 02EDh   | 02EEh   | 02EFh   |
| **02F0h**      | 02F0h                        | 02F1h   | 02F2h   | 02F3h   | 02F4h   | 02F5h   | 02F6h   | 02F7h   |
| **02F8h**      | 02F8h                        | 02F9h   | 02FAh   | 02FBh   | 02FCh   | 02FDh   | 02FEh   | 02FFh   |
| **0300h**      | 0300h                        | 0301h   | 0302h   | 0303h   | 0304h   | 0305h   | 0306h   | 0307h   |
| **0308h**      | 0308h                        | 0309h   | 030Ah   | 030Bh   | 030Ch   | 030Dh   | 030Eh   | 030Fh   |
| **0310h**      | 0310h                        | 0311h   | 0312h   | 0313h   | 0314h   | 0315h   | 0316h   | 0317h   |
| **0318h**      | 0318h                        | 0319h   | 031Ah   | 031Bh   | 031Ch   | 031Dh   | 031Eh   | 031Fh   |
| **0320h**      | 0320h                        | 0321h   | 0322h   | 0323h   | 0324h   | 0325h   | 0326h   | 0327h   |
| **0328h**      | 0328h                        | 0329h   | 032Ah   | 032Bh   | 032Ch   | 032Dh   | 032Eh   | 032Fh   |
| **0330h**      | 0330h                        | 0331h   | 0332h   | 0333h   | 0334h   | 0335h   | 0336h   | 0337h   |
| **0338h**      | 0338h                        | 0339h   | 033Ah   | 033Bh   | 033Ch   | 033Dh   | 033Eh   | 033Fh   |
| **0340h**      | 0340h                        | 0341h   | 0342h   | 0343h   | 0344h   | 0345h   | 0346h   | 0347h   |
| **0348h**      | 0348h                        | 0349h   | 034Ah   | 034Bh   | 034Ch   | 034Dh   | 034Eh   | 034Fh   |
| **0350h**      | 0350h                        | 0351h   | 0352h   | 0353h   | 0354h   | 0355h   | 0356h   | 0357h   |
| **0358h**      | 0358h                        | 0359h   | 035Ah   | 035Bh   | 035Ch   | 035Dh   | 035Eh   | 035Fh   |
| **0360h**      | 0360h                        | 0361h   | 0362h   | 0363h   | 0364h   | 0365h   | 0366h   | 0367h   |
| **0368h**      | 0368h                        | 0369h   | 036Ah   | 036Bh   | 036Ch   | 036Dh   | 036Eh   | 036Fh   |
| **0370h**      | 0370h                        | 0371h   | 0372h   | 0373h   | 0374h   | 0375h   | 0376h   | 0377h   |
| **0378h**      | 0378h                        | 0379h   | 037Ah   | 03FDh   | 03FEh   | 03FFh   | 037Eh   | 037Fh   |
| **0380h**      | 0380h                        | 0381h   | 0382h   | 0383h   | 0384h   | 0385h   | 0386h   | 0387h   |
| **0388h**      | 0388h                        | 0389h   | 038Ah   | 038Bh   | 038Ch   | 038Dh   | 038Eh   | 038Fh   |
| **0390h**      | 0390h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **0398h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03A0h**      | 03A0h                        | 03A1h   | 03A2h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03A8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 0386h   | 0388h   | 0389h   | 038Ah   |
| **03B0h**      | 03B0h                        | 0391h   | 0392h   | 0393h   | 0394h   | 0395h   | 0396h   | 0397h   |
| **03B8h**      | 0398h                        | 0399h   | 039Ah   | 039Bh   | 039Ch   | 039Dh   | 039Eh   | 039Fh   |
| **03C0h**      | 03A0h                        | 03A1h   | 03A3h   | 03A3h   | 03A4h   | 03A5h   | 03A6h   | 03A7h   |
| **03C8h**      | 03A8h                        | 03A9h   | 03AAh   | 03ABh   | 038Ch   | 038Eh   | 038Fh   | 03CFh   |
| **03D0h**      | 03D0h                        | 03D1h   | 03D2h   | 03D3h   | 03D4h   | 03D5h   | 03D6h   | 03D7h   |
| **03D8h**      | 03D8h                        | 03D8h   | 03DAh   | 03DAh   | 03 DCh   | 03 DCh   | 03DEh   | 03DEh   |
| **03E0h**      | 03E0h                        | 03E0h   | 03E2h   | 03E2h   | 03E4h   | 03E4h   | 03E6h   | 03E6h   |
| **03E8h**      | 03E8h                        | 03E8h   | 03EAh   | 03EAh   | 03ECh   | 03ECh   | 03EEh   | 03EEh   |
| **03F0h**      | 03F0h                        | 03F1h   | 03F9h   | 03F3h   | 03F4h   | 03F5h   | 03F6h   | 03F7h   |
| **03F8h**      | 03F7h                        | 03F9h   | 03FAh   | 03FAh   | 03FCh   | 03FDh   | 03FEh   | 03FFh   |
| **0400h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0408h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0410h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0418h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0420h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0428h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0430h**      | 0410h                        | 0411h   | 0412h   | 0413h   | 0414h   | 0415h   | 0416h   | 0417h   |
| **0438h**      | 0418h                        | 0419h   | 041Ah   | 041Bh   | 041Ch   | 041Dh   | 041Eh   | 041Fh   |
| **0440h**      | 0420h                        | 0421h   | 0422h   | 0423h   | 0424h   | 0425h   | 0426h   | 0427h   |
| **0448h**      | 0428h                        | 0429h   | 042Ah   | 042Bh   | 042Ch   | 042Dh   | 042Eh   | 042Fh   |
| **0450h**      | 0400h                        | 0401h   | 0402h   | 0403h   | 0404h   | 0405h   | 0406h   | 0407h   |
| **0458h**      | 0408h                        | 0409h   | 040Ah   | 040Bh   | 040Ch   | 040Dh   | 040Eh   | 040Fh   |
| **0460h**      | 0460h                        | 0460h   | 0462h   | 0462h   | 0464h   | 0464h   | 0466h   | 0466h   |
| **0468h**      | 0468h                        | 0468h   | 046Ah   | 046Ah   | 046Ch   | 046Ch   | 046Eh   | 046Eh   |
| **0470h**      | 0470h                        | 0470h   | 0472h   | 0472h   | 0474h   | 0474h   | 0476h   | 0476h   |
| **0478h**      | 0478h                        | 0478h   | 047Ah   | 047Ah   | 047Ch   | 047Ch   | 047Eh   | 047Eh   |
| **0480h**      | 0480h                        | 0480h   | 0482h   | 0483h   | 0484h   | 0485h   | 0486h   | 0487h   |
| **0488h**      | 0488h                        | 0489h   | 048Ah   | 048Ah   | 048Ch   | 048Ch   | 048Eh   | 048Eh   |
| **0490h**      | 0490h                        | 0490h   | 0492h   | 0492h   | 0494h   | 0494h   | 0496h   | 0496h   |
| **0498h**      | 0498h                        | 0498h   | 049Ah   | 049Ah   | 049Ch   | 049Ch   | 049Eh   | 049Eh   |
| **04A0h**      | 04A0h                        | 04A0h   | 04A2h   | 04A2h   | 04A4h   | 04A4h   | 04A6h   | 04A6h   |
| **04A8h**      | 04A8h                        | 04A8h   | 04AAh   | 04AAh   | 04ACh   | 04ACh   | 04AEh   | 04AEh   |
| **04B0h**      | 04B0h                        | 04B0h   | 04B2h   | 04B2h   | 04B4h   | 04B4h   | 04B6h   | 04B6h   |
| **04B8h**      | 04B8h                        | 04B8h   | 04BAh   | 04BAh   | 04BCh   | 04BCh   | 04BEh   | 04BEh   |
| **04C0h**      | 04C0h                        | 04C1h   | 04C1h   | 04C3h   | 04C3h   | 04C5h   | 04C5h   | 04C7h   |
| **04C8h**      | 04C7h                        | 04C9h   | 04C9h   | 04CBh   | 04CBh   | 04CDh   | 04CDh   | 04C0h   |
| **04D0h**      | 04D0h                        | 04D0h   | 04D2h   | 04D2h   | 04D4h   | 04D4h   | 04D6h   | 04D6h   |
| **04D8h**      | 04D8h                        | 04D8h   | 04DAh   | 04DAh   | 04DCh   | 04DCh   | 04DEh   | 04DEh   |
| **04E0h**      | 04E0h                        | 04E0h   | 04E2h   | 04E2h   | 04E4h   | 04E4h   | 04E6h   | 04E6h   |
| **04E8h**      | 04E8h                        | 04E8h   | 04EAh   | 04EAh   | 04ECh   | 04ECh   | 04EEh   | 04EEh   |
| **04F0h**      | 04F0h                        | 04F0h   | 04F2h   | 04F2h   | 04F4h   | 04F4h   | 04F6h   | 04F6h   |
| **04F8h**      | 04F8h                        | 04F8h   | 04FAh   | 04FAh   | 04FCh   | 04FCh   | 04FEh   | 04FEh   |
| **0500h**      | 0500h                        | 0500h   | 0502h   | 0502h   | 0504h   | 0504h   | 0506h   | 0506h   |
| **0508h**      | 0508h                        | 0508h   | 050Ah   | 050Ah   | 050Ch   | 050Ch   | 050Eh   | 050Eh   |
| **0510h**      | 0510h                        | 0510h   | 0512h   | 0512h   | 0514h   | 0515h   | 0516h   | 0517h   |
| **0518h**      | 0518h                        | 0519h   | 051Ah   | 051Bh   | 051Ch   | 051Dh   | 051Eh   | 051Fh   |
| **0520h**      | 0520h                        | 0521h   | 0522h   | 0523h   | 0524h   | 0525h   | 0526h   | 0527h   |
| **0528h**      | 0528h                        | 0529h   | 052Ah   | 052Bh   | 052Ch   | 052Dh   | 052Eh   | 052Fh   |
| **0530h**      | 0530h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0538h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0540h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0548h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0550h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | 0557h   |
| **0558h**      | 0558h                        | 0559h   | 055Ah   | 055Bh   | 055Ch   | 055Dh   | 055Eh   | 055Fh   |
| **0560h**      | 0560h                        | 0531h   | 0532h   | 0533h   | 0534h   | 0535h   | 0536h   | 0537h   |
| **0568h**      | 0538h                        | 0539h   | 053Ah   | 053Bh   | 053Ch   | 053Dh   | 053Eh   | 053Fh   |
| **0570h**      | 0540h                        | 0541h   | 0542h   | 0543h   | 0544h   | 0545h   | 0546h   | 0547h   |
| **0578h**      | 0548h                        | 0549h   | 054Ah   | 054Bh   | 054Ch   | 054Dh   | 054Eh   | 054Fh   |
| **0580h**      | 0550h                        | 0551h   | 0552h   | 0553h   | 0554h   | 0555h   | 0556h   | FFFFh   |
| **0588h**      | 17F6h                        | 2C63h   | 1 D7Eh   | 1 D7Fh   | 1D80h   | 1D81h   | 1D82h   | 1D83h   |
| **0590h**      | 1D84h                        | 1 D85h   | 1D86h   | 1D87h   | 1D88h   | 1 D89h   | 1D8Ah   | 1D8Bh   |
| **0598h**      | 1D8Ch                        | 1D8Dh   | 1 D8Eh   | 1D8Fh   | 1D90h   | 1D91h   | 1D92h   | 1 D93h   |
| **05A0h**      | 1 D94h                        | 1 D95h   | 1 D96h   | 1D97h   | 1 D98h   | 1 D99h   | 1D9Ah   | 1D9Bh   |
| **05A8h**      | 1 D9Ch                        | 1D9Dh   | 1 D9Eh   | 1 D9Fh   | 1DA0h   | 1DA1h   | 1DA2h   | 1DA3h   |
| **05B0h**      | 1DA4h                        | 1DA5h   | 1DA6h   | 1DA7h   | 1DA8h   | 1DA9h   | 1DAAh   | 1DABh   |
| **05B8h**      | 1daCh                        | 1DADh   | 1DAEh   | 1DAFh   | 1DB0h   | 1DB1h   | 1DB2h   | 1DB3h   |
| **05C0h**      | 1DB4h                        | 1DB5h   | 1DB6h   | 1DB7h   | 1DB8h   | 1DB9h   | 1DBAh   | 1DBBh   |
| **05C8h**      | 1DBCh                        | 1DBDh   | 1DBEh   | 1DBFh   | 1DC0h   | 1DC1h   | 1DC2h   | 1DC3h   |
| **05D0h**      | 1DC4h                        | 1DC5h   | 1DC6h   | 1DC7h   | 1DC8h   | 1DC9h   | 1DCAh   | 1DCBh   |
| **05D8h**      | 1 DDCCh                        | 1DCDh   | 1DCEh   | 1DCFh   | 1DD0h   | 1DD1h   | 1DD2h   | 1DD3h   |
| **05E0h**      | 1DD4h                        | 1DD5h   | 1DD6h   | 1DD7h   | 1DD8h   | 1DD9h   | 1DDAh   | 1DDBh   |
| **05E8h**      | 1DDCh                        | 1DDDh   | 1DDEh   | 1DDFh   | 1DE0h   | 1DE1h   | 1DE2h   | 1DE3h   |
| **05F0h**      | 1DE4h                        | 1DE5h   | 1DE6h   | 1DE7h   | 1DE8h   | 1DE9h   | 1DEAh   | 1DEBh   |
| **05F8h**      | 1DECh                        | 1DEDh   | 1DEEh   | 1DEFh   | 1DF0h   | 1DF1h   | 1DF2h   | 1DF3h   |
| **0600h**      | 1DF4h                        | 1DF5h   | 1DF6h   | 1DF7h   | 1DF8h   | 1DF9h   | 1DFAh   | 1DFBh   |
| **0608h**      | 1DFCh                        | 1DFDh   | 1DFEh   | 1DFFh   | 1E00h   | 1E00h   | 1E02h   | 1E02h   |
| **0610h**      | 1E04h                        | 1E04h   | 1E06h   | 1E06h   | 1E08h   | 1E08h   | 1E0Ah   | 1E0Ah   |
| **0618h**      | 1E0Ch                        | 1E0Ch   | 1E0Eh   | 1E0Eh   | 1E10h   | 1E10h   | 1E12h   | 1E12h   |
| **0620h**      | 1E14h                        | 1E14h   | 1E16h   | 1E16h   | 1E18h   | 1E18h   | 1E1Ah   | 1E1Ah   |
| **0628h**      | 1E1Ch                        | 1E1Ch   | 1E1Eh   | 1E1Eh   | 1E20h   | 1E20h   | 1E22h   | 1E22h   |
| **0630h**      | 1E24h                        | 1E24h   | 1E26h   | 1E26h   | 1E28h   | 1E28h   | 1E2Ah   | 1E2Ah   |
| **0638h**      | 1E2Ch                        | 1E2Ch   | 1E2Eh   | 1E2Eh   | 1E30h   | 1E30h   | 1E32h   | 1E32h   |
| **0640h**      | 1E34h                        | 1E34h   | 1E36h   | 1E36h   | 1E38h   | 1E38h   | 1E3Ah   | 1E3Ah   |
| **0648h**      | 1E3Ch                        | 1E3Ch   | 1E3Eh   | 1E3Eh   | 1E40h   | 1E40h   | 1E42h   | 1E42h   |
| **0650h**      | 1E44h                        | 1E44h   | 1E46h   | 1E46h   | 1E48h   | 1E48h   | 1E4Ah   | 1E4Ah   |
| **0658h**      | 1E4Ch                        | 1E4Ch   | 1E4Eh   | 1E4Eh   | 1E50h   | 1E50h   | 1E52h   | 1E52h   |
| **0660h**      | 1E54h                        | 1E54h   | 1E56h   | 1E56h   | 1E58h   | 1E58h   | 1E5Ah   | 1E5Ah   |
| **0668h**      | 1E5Ch                        | 1E5Ch   | 1E5Eh   | 1E5Eh   | 1E60h   | 1E60h   | 1E62h   | 1E62h   |
| **0670h**      | 1E64h                        | 1E64h   | 1E66h   | 1E66h   | 1E68h   | 1E68h   | 1E6Ah   | 1E6Ah   |
| **0678h**      | 1E6Ch                        | 1E6Ch   | 1E6Eh   | 1E6Eh   | 1E70h   | 1E70h   | 1E72h   | 1E72h   |
| **0680h**      | 1E74h                        | 1E74h   | 1E76h   | 1E76h   | 1E78h   | 1E78h   | 1E7Ah   | 1E7Ah   |
| **0688h**      | 1E7Ch                        | 1E7Ch   | 1E7Eh   | 1E7Eh   | 1E80h   | 1E80h   | 1E82h   | 1E82h   |
| **0690h**      | 1E84h                        | 1E84h   | 1E86h   | 1E86h   | 1E88h   | 1E88h   | 1E8Ah   | 1E8Ah   |
| **0698h**      | 1E8Ch                        | 1E8Ch   | 1E8Eh   | 1E8Eh   | 1E90h   | 1E90h   | 1E92h   | 1E92h   |
| **06A0h**      | 1E94h                        | 1E94h   | 1E96h   | 1E97h   | 1E98h   | 1E99h   | 1E9Ah   | 1E9Bh   |
| **06A8h**      | 1E9Ch                        | 1E9Dh   | 1E9Eh   | 1E9Fh   | 1EA0h   | 1EA0h   | 1EA2h   | 1EA2h   |
| **06B0h**      | 1EA4h                        | 1EA4h   | 1EA6h   | 1EA6h   | 1EA8h   | 1EA8h   | 1EAAh   | 1EAAh   |
| **06B8h**      | 1ACh                        | 1ACh   | 1EAEh   | 1EAEh   | 1EB0h   | 1EB0h   | 1EB2h   | 1EB2h   |
| **06C0h**      | 1EB4h                        | 1EB4h   | 1EB6h   | 1EB6h   | 1EB8h   | 1EB8h   | 1EBAh   | 1EBAh   |
| **06C8h**      | 1EBCh                        | 1EBCh   | 1EBEh   | 1EBEh   | 1EC0h   | 1EC0h   | 1EC2h   | 1EC2h   |
| **06D0h**      | 1EC4h                        | 1EC4h   | 1EC6h   | 1EC6h   | 1EC8h   | 1EC8h   | 1ECAh   | 1ECAh   |
| **06D8h**      | 1CCh                        | 1CCh   | 1ECEh   | 1ECEh   | 1ED0h   | 1ED0h   | 1ED2h   | 1ED2h   |
| **06E0h**      | 1ED4h                        | 1ED4h   | 1ED6h   | 1ED6h   | 1ED8h   | 1ED8h   | 1EDAh   | 1EDAh   |
| **06E8h**      | 1EDCh                        | 1EDCh   | 1EDEh   | 1EDEh   | 1EE0h   | 1EE0h   | 1EE2h   | 1EE2h   |
| **06F0h**      | 1EE4h                        | 1EE4h   | 1EE6h   | 1EE6h   | 1EE8h   | 1EE8h   | 1EEAh   | 1EEAh   |
| **06F8h**      | 1EECh                        | 1EECh   | 1EEEh   | 1EEEh   | 1EF0h   | 1EF0h   | 1EF2h   | 1EF2h   |
| **0700h**      | 1EF4h                        | 1EF4h   | 1EF6h   | 1EF6h   | 1EF8h   | 1EF8h   | 1EFAh   | 1EFBh   |
| **0708h**      | 1EFCh                        | 1EFDh   | 1EFEh   | 1EFFh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0710h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F08h   | 1F09h   | 1F0Ah   | 1F0Bh   |
| **0718h**      | 1F0Ch                        | 1F0Dh   | 1F0Eh   | 1F0Fh   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0720h**      | 1F1Ch                        | 1F1Dh   | 1F16h   | 1F17h   | 1F18h   | 1F19h   | 1F1Ah   | 1F1Bh   |
| **0728h**      | 1F1Ch                        | 1F1Dh   | 1F1Eh   | 1F1Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0730h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F28h   | 1F29h   | 1F2Ah   | 1F2Bh   |
| **0738h**      | 1F2Ch                        | 1F2Dh   | 1F2Eh   | 1F2Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0740h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F38h   | 1F39h   | 1F3Ah   | 1F3Bh   |
| **0748h**      | 1F3Ch                        | 1F3Dh   | 1F3Eh   | 1F3Fh   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0750h**      | 1F4Ch                        | 1F4Dh   | 1F46h   | 1F47h   | 1F48h   | 1F49h   | 1F4Ah   | 1F4Bh   |
| **0758h**      | 1F4Ch                        | 1F4Dh   | 1F4Eh   | 1F4Fh   | 1F50h   | 1F59h   | 1F52h   | 1F5Bh   |
| **0760h**      | 1F54h                        | 1F5Dh   | 1F56h   | 1F5Fh   | 1F58h   | 1F59h   | 1F5Ah   | 1F5Bh   |
| **0768h**      | 1F5Ch                        | 1F5Dh   | 1F5Eh   | 1F5Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0770h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1F68h   | 1F69h   | 1F6Ah   | 1F6Bh   |
| **0778h**      | 1F6Ch                        | 1F6Dh   | 1F6Eh   | 1F6Fh   | 1FBAh   | 1FBBh   | 1FC8h   | 1FC9h   |
| **0780h**      | 1FCAh                        | 1FCBh   | 1FDAh   | 1FDBh   | 1FF8h   | 1FF9h   | 1FEAh   | 1FEBh   |
| **0788h**      | 1FFAh                        | 1FFBh   | 1F7Eh   | 1F7Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0790h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F88h   | 1F89h   | 1F8Ah   | 1F8Bh   |
| **0798h**      | 1F8Ch                        | 1F8Dh   | 1F8Eh   | 1F8Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A0h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1F98h   | 1F99h   | 1F9Ah   | 1F9Bh   |
| **07A8h**      | 1F9Ch                        | 1F9Dh   | 1F9Eh   | 1F9Fh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B0h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FA8h   | 1FA9h   | 1FAAh   | 1FABh   |
| **07B8h**      | 1FACh                        | 1FADh   | 1FAEh   | 1FAFh   | 1FB8h   | 1FB9h   | 1FB2h   | 1FBCh   |
| **07C0h**      | 1FB4h                        | 1FB5h   | 1FB6h   | 1FB7h   | 1FB8h   | 1FB9h   | 1FBAh   | 1FBBh   |
| **07C8h**      | 1FBCh                        | 1FBDh   | 1FBEh   | 1FBFh   | 1FC0h   | 1FC1h   | 1FC2h   | 1FC3h   |
| **07D0h**      | 1FC4h                        | 1FC5h   | 1FC6h   | 1FC7h   | 1FC8h   | 1FC9h   | 1FCAh   | 1FCBh   |
| **07D8h**      | 1FC3h                        | 1FCDh   | 1FCEh   | 1FCFh   | 1FD8h   | 1FD9h   | 1FD2h   | 1FD3h   |
| **07E0h**      | 1FD4h                        | 1FD5h   | 1FD6h   | 1FD7h   | 1FD8h   | 1FD9h   | 1FDAh   | 1FDBh   |
| **07E8h**      | 1FDCh                        | 1FDDh   | 1FDEh   | 1FDFh   | 1FE8h   | 1FE9h   | 1FE2h   | 1FE3h   |
| **07F0h**      | 1FE4h                        | 1FECh   | 1FE6h   | 1FE7h   | 1FE8h   | 1FE9h   | 1FEAh   | 1FEBh   |
| **07F8h**      | 1FECh                        | 1FEDh   | 1FEEh   | 1FEFh   | 1FF0h   | 1FF1h   | 1FF2h   | 1FF3h   |
| **0800h**      | 1FF4h                        | 1FF5h   | 1FF6h   | 1FF7h   | 1FF8h   | 1FF9h   | 1FFAh   | 1FFBh   |
| **0808h**      | 1FF3h                        | 1FFDh   | 1FFEh   | 1FFFh   | 2000h   | 2001h   | 2002h   | 2003h   |
| **0810h**      | 2004h                        | 2005h   | 2006h   | 2007h   | 2008h   | 2009h   | 200Ah   | 200Bh   |
| **0818h**      | 200Ch                        | 200 Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202Ah   | 202Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203Ah   | 203Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204Ah   | 204Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205Ah   | 205Bh   |
| **0868h**      | 205Ch                        | 205 Dh   | 205Eh   | 205Fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206Ah   | 206Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207Ah   | 207Bh   |
| **0888h**      | 207Ch                        | 207 Dh   | 207Eh   | 207Fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208Ah   | 208Bh   |
| **0898h**      | 208Ch                        | 208 Dh   | 208Eh   | 208Fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08A0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209 Dh   | 209Eh   | 209Fh   | 20A0h   | 20A1h   | 20A2h   | 20A3h   |
| **08B0h**      | 20A4h                        | 20A5h   | 20A6h   | 20A7h   | 20A8h   | 20A9h   | 20AAh   | 20ABh   |
| **08B8h**      | 20ACh                        | 20ADh   | 20AEh   | 20AFh   | 20B0h   | 20B1h   | 20B2h   | 20B3h   |
| **08C0h**      | 20B4h                        | 20B5h   | 20B6h   | 20B7h   | 20B8h   | 20B9h   | 20BAh   | 20BBh   |
| **08C8h**      | 20BCh                        | 20BDh   | 20BEh   | 20BFh   | 20C0h   | 20C1h   | 20C2h   | 20C3h   |
| **08D0h**      | 20C4h                        | 20C5h   | 20C6h   | 20C7h   | 20C8h   | 20C9h   | 20CAh   | 20CBh   |
| **08D8h**      | 20CCh                        | 20CDh   | 20CEh   | 20CFh   | 20D0h   | 20D1h   | 20D2h   | 20D3h   |
| **08E0h**      | 20D4h                        | 20D5h   | 20D6h   | 20D7h   | 20D8h   | 20D9h   | 20DAh   | 20DBh   |
| **08E8h**      | 20 DCh                        | 20DDh   | 20DEh   | 20DFh   | 20E0h   | 20E1h   | 20E2h   | 20E3h   |
| **08F0h**      | 20E4h                        | 20E5h   | 20E6h   | 20E7h   | 20E8h   | 20E9h   | 20EAh   | 20EBh   |
| **08F8h**      | 20ECh                        | 20EDh   | 20EEh   | 20EFh   | 20F0h   | 20F1h   | 20F2h   | 20F3h   |
| **0900h**      | 20F4h                        | 20F5h   | 20F6h   | 20F7h   | 20F8h   | 20F9h   | 20FAh   | 20FBh   |
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104h                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210Ah   | 210Bh   |
| **0918h**      | 210Ch                        | 210 Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114 ore                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211Ah   | 211Bh   |
| **0928h**      | 211Ch                        | 211 Dh   | 211Eh   | 211Fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124 ore                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212Ah   | 212Bh   |
| **0938h**      | 212Ch                        | 212 Dh   | 212Eh   | 212Fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134 ore                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213Ah   | 213Bh   |
| **0948h**      | 213Ch                        | 213 Dh   | 213Eh   | 213Fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144 ore                        | 2145h   | 2146h   | 2147h   | 2148 ore   | 2149h   | 214Ah   | 214Bh   |
| **0958h**      | 214Ch                        | 214 Dh   | 2132 ore   | 214Fh   | 2150h   | 2151h   | 2152 ore   | 2153 ore   |
| **0960h**      | 2154 ore                        | 2155 ore   | 2156 ore   | 2157h   | 2158 ore   | 2159h   | 215Ah   | 215Bh   |
| **0968h**      | 215Ch                        | 215 Dh   | 215Eh   | 215Fh   | 2160h   | 2161h   | 2162 ore   | 2163 ore   |
| **0970h**      | 2164 ore                        | 2165 ore   | 2166 ore   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0978h**      | 216Ch                        | 216 Dh   | 216Eh   | 216Fh   | 2160h   | 2161h   | 2162 ore   | 2163 ore   |
| **0980h**      | 2164 ore                        | 2165 ore   | 2166 ore   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0988h**      | 216Ch                        | 216 Dh   | 216Eh   | 216Fh   | 2180h   | 2181h   | 2182 ore   | 2183 ore   |
| **0990h**      | 2183 ore                        | FFFFh   | 034Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24BBh                        | 24 BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
| **09A0h**      | 24C3h                        | 24C4h   | 24C5h   | 24C6h   | 24C7h   | 24C8h   | 24C9h   | 24CAh   |
| **09A8h**      | 24CBh                        | 24CCh   | 24CDh   | 24CEh   | 24CFh   | FFFFh   | 0746h   | 2C00h   |
| **09B0h**      | 2C01h                        | 2C02h   | 2C03h   | 2C04h   | 2C05h   | 2C06h   | 2C07h   | 2C08h   |
| **09B8h**      | 2C09h                        | 2C0Ah   | 2C0Bh   | 2C0Ch   | 2C0Dh   | 2C0Eh   | 2C0Fh   | 2C10h   |
| **09C0h**      | 2C11h                        | 2C12h   | 2C13h   | 2C14h   | 2C15h   | 2C16h   | 2C17h   | 2C18h   |
| **09C8h**      | 2C19h                        | 2C1Ah   | 2C1Bh   | 2C1Ch   | 2C1Dh   | 2C1Eh   | 2C1Fh   | 2C20h   |
| **09D0h**      | 2C21h                        | 2C22h   | 2C23h   | 2C24h   | 2C25h   | 2C26h   | 2C27h   | 2C28h   |
| **09D8h**      | 2C29h                        | 2C2Ah   | 2C2Bh   | 2C2Ch   | 2C2Dh   | 2C2Eh   | 2C5Fh   | 2C60h   |
| **09E0h**      | 2C60h                        | 2C62h   | 2C63h   | 2C64h   | 2C65h   | 2C66h   | 2C67h   | 2C67h   |
| **09E8h**      | 2C69h                        | 2C69h   | 2C6Bh   | 2C6Bh   | 2C6Dh   | 2C6Eh   | 2C6Fh   | 2C70h   |
| **09F0h**      | 2C71h                        | 2C72h   | 2C73h   | 2C74h   | 2C75h   | 2C75h   | 2C77h   | 2C78h   |
| **09F8h**      | 2C79h                        | 2C7Ah   | 2C7Bh   | 2C7Ch   | 2C7Dh   | 2C7Eh   | 2C7Fh   | 2C80h   |
| **0A00h**      | 2C80h                        | 2C82h   | 2C82h   | 2C84h   | 2C84h   | 2C86h   | 2C86h   | 2C88h   |
| **0A08h**      | 2C88h                        | 2C8Ah   | 2C8Ah   | 2C8Ch   | 2C8Ch   | 2C8Eh   | 2C8Eh   | 2C90h   |
| **0A10h**      | 2C90h                        | 2C92h   | 2C92h   | 2C94h   | 2C94h   | 2C96h   | 2C96h   | 2C98h   |
| **0A18h**      | 2C98h                        | 2C9Ah   | 2C9Ah   | 2C9Ch   | 2C9Ch   | 2C9Eh   | 2C9Eh   | 2CA0h   |
| **0A20h**      | 2CA0h                        | 2CA2h   | 2CA2h   | 2CA4h   | 2CA4h   | 2CA6h   | 2CA6h   | 2CA8h   |
| **0A28h**      | 2CA8h                        | 2CAAh   | 2CAAh   | 2CACh   | 2CACh   | 2CAEh   | 2CAEh   | 2CB0h   |
| **0A30h**      | 2CB0h                        | 2CB2h   | 2CB2h   | 2CB4h   | 2CB4h   | 2CB6h   | 2CB6h   | 2CB8h   |
| **0A38h**      | 2CB8h                        | 2CBAh   | 2CBAh   | 2CBCh   | 2CBCh   | 2CBEh   | 2CBEh   | 2CC0h   |
| **0A40h**      | 2CC0h                        | 2CC2h   | 2CC2h   | 2CC4h   | 2CC4h   | 2CC6h   | 2CC6h   | 2CC8h   |
| **0A48h**      | 2CC8h                        | 2CCAh   | 2CCAh   | 2CCCh   | 2CCCh   | 2CCEh   | 2CCEh   | 2CD0h   |
| **0A50h**      | 2CD0h                        | 2CD2h   | 2CD2h   | 2CD4h   | 2CD4h   | 2CD6h   | 2CD6h   | 2CD8h   |
| **0A58h**      | 2CD8h                        | 2CDAh   | 2CDAh   | 2CDCh   | 2CDCh   | 2CDEh   | 2CDEh   | 2CE0h   |
| **0A60h**      | 2CE0h                        | 2CE2h   | 2CE2h   | 2CE4h   | 2CE5h   | 2CE6h   | 2CE7h   | 2CE8h   |
| **0A68h**      | 2CE9h                        | 2CEAh   | 2CEBh   | 2CECh   | 2CEDh   | 2CEEh   | 2CEFh   | 2CF0h   |
| **0A70h**      | 2CF1h                        | 2CF2h   | 2CF3h   | 2CF4h   | 2CF5h   | 2CF6h   | 2CF7h   | 2CF8h   |
| **0A78h**      | 2CF9h                        | 2CFAh   | 2CFBh   | 2CFCh   | 2CFDh   | 2CFEh   | 2CFFh   | 10A0h   |
| **0A80h**      | 10A1h                        | 10A2h   | 10A3h   | 10A4h   | 10A5h   | 10A6h   | 10A7h   | 10A8h   |
| **0A88h**      | 10A9h                        | 10AAh   | 10ABh   | 10ACh   | 10ADh   | 10AEh   | 10AFh   | 10B0h   |
| **0A90h**      | 10B1h                        | 10B2h   | 10B3h   | 10B4h   | 10B5h   | 10B6h   | 10B7h   | 10B8h   |
| **0A98h**      | 10B9h                        | 10BAh   | 10BH   | 10 BCh   | 10BDh   | 10BEh   | 10BFh   | 10C0h   |
| **0AA0h**      | 10C1h                        | 10C2h   | 10C3h   | 10C4h   | 10C5h   | FFFFh   | D21Bh   | FF21h   |
| **0AA8h**      | FF22h                        | FF23h   | FF24h   | FF25h   | FF26h   | FF27h   | FF28h   | FF29h   |
| **0AB0h**      | FF2Ah                        | FF2Bh   | FF2Ch   | FF2Dh   | FF2Eh   | FF2Fh   | FF30h   | FF31h   |
| **0AB8h**      | FF32h                        | FF33h   | FF34h   | FF35h   | FF36h   | FF37h   | FF38h   | FF39h   |
| **0AC0h**      | FF3Ah                        | FF5Bh   | FF5Ch   | FF5Dh   | FF5Eh   | FF5Fh   | FF60h   | FF61h   |
| **0AC8h**      | FF62h                        | FF63h   | FF64h   | FF65h   | FF66h   | FF67h   | FF68h   | FF69h   |
| **0AD0h**      | FF6Ah                        | FF6Bh   | FF6Ch   | FF6Dh   | FF6Eh   | FF6Fh   | FF70h   | FF71h   |
| **0AD8h**      | FF72h                        | FF73h   | FF74h   | FF75h   | FF76h   | FF77h   | FF78h   | FF79h   |
| **0AE0h**      | FF7Ah                        | FF7Bh   | FF7Ch   | FF7Dh   | FF7Eh   | FF7Fh   | FF80h   | FF81h   |
| **0AE8h**      | FF82h                        | FF83h   | FF84h   | FF85h   | FF86h   | FF87h   | FF88h   | FF89h   |
| **0AF0h**      | FF8Ah                        | FF8Bh   | FF8Ch   | FF8Dh   | FF8Eh   | FF8Fh   | FF90h   | FF91h   |
| **0AF8h**      | FF92h                        | FF93h   | FF94h   | FF95h   | FF96h   | FF97h   | FF98h   | FF99h   |
| **0B00h**      | FF9Ah                        | FF9Bh   | FF9Ch   | FF9Dh   | FF9Eh   | FF9Fh   | FFA0h   | FFA1h   |
| **0B08h**      | FFA2h                        | FFA3h   | FFA4h   | FFA5h   | FFA6h   | FFA7h   | FFA8h   | FFA9h   |
| **0B10h**      | FFAAh                        | FFABh   | FFACh   | FFADh   | FFAEh   | FFAFh   | FFB0h   | FFB1h   |
| **0B18h**      | FFB2h                        | FFB3h   | FFB4h   | FFB5h   | FFB6h   | FFB7h   | FFB8h   | FFB9h   |
| **0B20h**      | FFBAh                        | FFBBh   | FFBCh   | FFBDh   | FFBEh   | FFBFh   | FFC0h   | FFC1h   |
| **0B28h**      | FFC2h                        | FFC3h   | FFC4h   | FFC5h   | FFC6h   | FFC7h   | FFC8h   | FFC9h   |
| **0B30h**      | FFCAh                        | FFCBh   | FFCCh   | FFCDh   | FFCEh   | FFCFh   | FFD0h   | FFD1h   |
| **0B38h**      | FFD2h                        | FFD3h   | FFD4h   | FFD5h   | FFD6h   | FFD7h   | FFD8h   | FFD9h   |
| **0B40h**      | FFDAh                        | FFDBh   | FFDCh   | FFDDh   | FFDEh   | FFDFh   | FFE0h   | FFE1h   |
| **0B48h**      | FFE2h                        | FFE3h   | FFE4h   | FFE5h   | FFE6h   | FFE7h   | FFE8h   | FFE9h   |
| **0B50h**      | FFEAh                        | FFEBh   | FFECh   | FFEDh   | FFEEh   | FFEFh   | FFF0h   | FFF1h   |
| **0B58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0B60h**      | FFFAh                        | FFFBh   | FFFCh   | FFFDh   | FFFEh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>7.3 Voce di directory dell'etichetta di volume

L'etichetta di volume è una stringa Unicode che consente agli utenti finali di distinguere i volumi di archiviazione. Nella directory exFAT file system l'etichetta di volume esiste come voce di directory primaria critica nella directory radice (vedere [la tabella 26).](#table-26-volume-label-directoryentry-structure) Il numero valido di voci della directory Volume Label è compreso tra 0 e 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tabella 26 Struttura DirectoryEntry dell'etichetta di volume**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#731-entrytype-field">e la sezione 7.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Conteggio caratteri</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#732-charactercount-field">e la sezione 7.3.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Questo campo è obbligatorio <a href="#733-volumelabel-field">e la sezione 7.3.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>7.3.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1).](#631-entrytype-field)

##### <a name="7311-typecode-field"></a>7.3.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.1).](#6311-typecode-field)

Per la voce di directory Volume Label, il valore valido per questo campo è
3.

##### <a name="7312-typeimportance-field"></a>7.3.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.2).](#6312-typeimportance-field)

Per la voce di directory Volume Label, il valore valido per questo campo è
0.

##### <a name="7313-typecategory-field"></a>7.3.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.3).](#6313-typecategory-field)

##### <a name="7314-inuse-field"></a>7.3.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.4).](#6314-inuse-field)

#### <a name="732-charactercount-field"></a>7.3.2 Campo CharacterCount

Il campo CharacterCount deve contenere la lunghezza della stringa Unicode contenuta nel campo VolumeLabel.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 0, il che significa che la stringa Unicode è lunga 0 caratteri (che equivale a nessuna etichetta di volume)

- Al massimo 11, il che significa che la stringa Unicode è lunga 11 caratteri

#### <a name="733-volumelabel-field"></a>7.3.3 Campo VolumeLabel

Il campo VolumeLabel deve contenere una stringa Unicode, ovvero il nome descrittivo del volume. Il campo VolumeLabel ha lo stesso set di caratteri non validi del campo FileName della voce di directory File Name (vedere [la sezione 7.7.3).](#773-filename-field)

### <a name="74-file-directory-entry"></a>7.4 Voce della directory dei file

Le voci della directory file descrivono file e directory. Si tratta di voci di directory primarie critiche e qualsiasi directory può contenere zero o più voci di directory file (vedere [la tabella 27).](#table-27-file-directoryentry) Perché una voce della directory File sia valida, è necessario che almeno una voce della directory Estensione di flusso e almeno una voce di directory Nome file seguano immediatamente la voce della directory File (vedere rispettivamente le sezioni [7.6](#76-stream-extension-directory-entry) e [7.7).](#77-file-name-directory-entry)

<div id="table-27-file-directoryentry" />

**Tabella 27 File DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#741-entrytype-field">e la sezione 7.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#742-secondarycount-field">e la sezione 7.4.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#743-setchecksum-field">e la sezione 7.4.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#744-fileattributes-field">e la sezione 7.4.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="even">
<td>CreateTimestamp</td>
<td>8</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> e la sezione 7.4.5 </
a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">e la sezione 7.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">e la sezione 7.4.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> e la sezione 7.4.5 </
a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">e la sezione 7.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CreateUtcOffset</td>
<td>22</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> e la sezione 7.4.5 </
a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>LastModifiedUtcOffset</td>
<td>23</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">e la sezione 7.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">e la sezione 7.4.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>7.4.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la Sezione 6.3.1).](#631-entrytype-field)

##### <a name="7411-typecode-field"></a>7.4.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la Sezione 6.3.1.1).](#6311-typecode-field)

Per una voce di directory File, il valore valido per questo campo è 5.

##### <a name="7412-typeimportance-field"></a>7.4.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la Sezione 6.3.1.2).](#6312-typeimportance-field)

Per una voce di directory File, il valore valido per questo campo è 0.

##### <a name="7413-typecategory-field"></a>7.4.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la Sezione 6.3.1.3).](#6313-typecategory-field)

##### <a name="7414-inuse-field"></a>7.4.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primaria generica (vedere [la Sezione 6.3.1.4).](#6314-inuse-field)

#### <a name="742-secondarycount-field"></a>7.4.2 Campo SecondaryCount

Il campo SecondaryCount deve essere conforme alla definizione fornita nel modello DirectoryEntry primaria generica (vedere [la Sezione 6.3.2).](#632-secondarycount-field)

#### <a name="743-setchecksum-field"></a>7.4.3 Campo SetChecksum

Il campo SetChecksum deve essere conforme alla definizione fornita nel modello DirectoryEntry primaria generica (vedere [la Sezione 6.3.3).](#633-setchecksum-field)

#### <a name="744-fileattributes-field"></a>7.4.4 Campo FileAttributes

Il campo FileAttributes contiene flag (vedere [la tabella 28).](#table-28-fileattributes-field-structure)

<div id="table-28-fileattributes-field-structure" />

**Tabella 28 Struttura dei campi FileAttributes**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ReadOnly</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio ed è conforme alla definizione MS-DOS.</td>
</tr>
<tr class="even">
<td>Nascosto</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio ed è conforme alla definizione MS-DOS.</td>
</tr>
<tr class="odd">
<td>Sistema</td>
<td>2</td>
<td>1</td>
<td>Questo campo è obbligatorio ed è conforme alla definizione MS-DOS.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>3</td>
<td>1</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="odd">
<td>Directory</td>
<td>4</td>
<td>1</td>
<td>Questo campo è obbligatorio ed è conforme alla definizione MS-DOS.</td>
</tr>
<tr class="even">
<td>Archiviazione</td>
<td>5</td>
<td>1</td>
<td>Questo campo è obbligatorio ed è conforme alla definizione MS-DOS.</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>7.4.5 Campi CreateTimestamp, Create10msIncrement e CreateUtcOffset

In combinazione, i campi CreateTimestamp e CreateTime10msIncrement descrivono la data e l'ora locali in cui è stato creato il file o la directory specificata. Il campo CreateUtcOffset descrive l'offset di data e ora locali rispetto all'ora UTC. Le implementazioni devono impostare questi campi al momento della creazione del set di voci di directory specificato.

Questi campi devono essere conformi alle definizioni dei campi Timestamp, 10msIncrement e UtcOffset (vedere rispettivamente [Section 7.4.8](#748-timestamp-fields), [Section 7.4.9](#749-10msincrement-fields)e [Section 7.4.10).](#7410-utcoffset-fields)

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>7.4.6 Campi LastModifiedTimestamp, LastModified10msIncrement e LastModifiedUtcOffset

In combinazione, i campi LastModifiedTimestamp e LastModifiedTime10msIncrement descrivono la data e l'ora locali dell'ultima modifica del contenuto di uno dei cluster associati alla voce di directory dell'estensione di flusso specificata. Il campo LastModifiedUtcOffset descrive l'offset di data e ora locali rispetto all'ora UTC. Le implementazioni devono aggiornare questi campi:

1. Dopo aver modificato il contenuto di uno dei cluster associati alla voce di directory dell'estensione di flusso specificata (ad eccezione del contenuto che esiste oltre il punto descritto nel campo ValidDataLength)

2. Quando si modificano i valori dei campi ValidDataLength o DataLength

Questi campi devono essere conformi alle definizioni dei campi Timestamp, 10msIncrement e UtcOffset (vedere rispettivamente [Section 7.4.8](#748-timestamp-fields), [Section 7.4.9](#749-10msincrement-fields)e [Section 7.4.10).](#7410-utcoffset-fields)

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>7.4.7 Campi LastAccessedTimestamp e LastAccessedUtcOffset

Il campo LastAccessedTimestamp deve descrivere la data e l'ora dell'ultimo accesso al contenuto di uno dei cluster associati alla voce di directory dell'estensione di flusso specificata. Il campo LastAccessedUtcOffset descrive l'offset di data e ora locali rispetto all'ora UTC.
Le implementazioni devono aggiornare questi campi:

1. Dopo la modifica del contenuto di uno dei cluster associati alla voce di directory dell'estensione di flusso specificata (ad eccezione del contenuto che esiste oltre ValidDataLength)

2. Quando si modificano i valori dei campi ValidDataLength o DataLength

Le implementazioni devono aggiornare questi campi dopo la lettura del contenuto di uno dei cluster associati alla voce di directory dell'estensione di flusso specificata.

Questi campi devono essere conformi alle definizioni dei campi Timestamp e UtcOffset (vedere rispettivamente [Sezione 7.4.8](#748-timestamp-fields) e [Sezione 7.4.10).](#7410-utcoffset-fields)

#### <a name="748-timestamp-fields"></a>7.4.8 Campi timestamp

I campi timestamp descrivono sia la data locale che l'ora, fino a una risoluzione di due secondi (vedere [la tabella 29).](#table-29-timestamp-field-structure)

<div id="table-29-timestamp-field-structure" />

**Tabella 29 Struttura dei campi timestamp**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>Questo campo è obbligatorio <a href="#7481-doubleseconds-field">e la sezione 7.4.8.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Minuto</td>
<td>5</td>
<td>6</td>
<td>Questo campo è obbligatorio <a href="#7482-minute-field">e la sezione 7.4.8.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Ora</td>
<td>11</td>
<td>5</td>
<td>Questo campo è obbligatorio <a href="#7483-hour-field">e la sezione 7.4.8.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Giorno</td>
<td>16</td>
<td>5</td>
<td>Questo campo è obbligatorio <a href="#7484-day-field">e la sezione 7.4.8.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Month</td>
<td>21</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#7485-month-field">e la sezione 7.4.8.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Questo campo è obbligatorio <a href="#7486-year-field">e la sezione 7.4.8.6</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>7.4.8.1 Campo DoubleSeconds

Il campo DoubleSeconds descrive la parte relativa ai secondi del campo Timestamp, in multipli di due secondi.

L'intervallo valido di valori per questo campo deve essere:

- 0, che rappresenta 0 secondi

- 29, che rappresenta 58 secondi

##### <a name="7482-minute-field"></a>Campo 7.4.8.2 Minute

Il campo Minute descrive la parte relativa ai minuti del campo Timestamp.

L'intervallo valido di valori per questo campo deve essere:

- 0, che rappresenta 0 minuti

- 59, che rappresenta 59 minuti

##### <a name="7483-hour-field"></a>Campo 7.4.8.3 Hour

Il campo Ora descrive la parte relativa alle ore del campo Timestamp.

L'intervallo valido di valori per questo campo deve essere:

- 0, che rappresenta le ore 00:00

- 23, che rappresenta le 23:00 ore

##### <a name="7484-day-field"></a>Campo 7.4.8.4 Day

Il campo Giorno descrive la parte relativa al giorno del campo Timestamp.

L'intervallo valido di valori per questo campo deve essere:

- 1, ovvero il primo giorno del mese specificato

- Ultimo giorno del mese specificato (il mese specificato definisce il numero di giorni validi)

##### <a name="7485-month-field"></a>7.4.8.5 Campo Month

Il campo Month deve descrivere la parte relativa al mese del campo Timestamp.

L'intervallo valido di valori per questo campo deve essere:

- Almeno 1, che rappresenta gennaio

- Al massimo 12, che rappresenta dicembre

##### <a name="7486-year-field"></a>Campo 7.4.8.6 Year

Il campo Year deve descrivere la parte relativa all'anno del campo Timestamp, relativa all'anno 1980. Questo campo rappresenta l'anno 1980 con il valore 0 e l'anno 2107 con il valore 127.

Tutti i valori possibili per questo campo sono validi.

#### <a name="749-10msincrement-fields"></a>7.4.9 10msIncrement Fields

I campi 10msIncrement forniscono una risoluzione temporale aggiuntiva ai campi Timestamp corrispondenti in multipli di dieci millisecondi.

L'intervallo valido di valori per questi campi deve essere:

- Almeno 0, che rappresenta 0 millisecondi

- Al massimo 199, che rappresenta 1990 millisecondi

#### <a name="7410-utcoffset-fields"></a>7.4.10 Campi UtcOffset

I campi UtcOffset (vedere la tabella [30)](#table-30-utcoffset-field-structure)descrivono l'offset dall'ora UTC alla data e all'ora locali che descrivono i campi Timestamp e 10msIncrement corrispondenti. L'offset dall'ora UTC alla data e all'ora locali include gli effetti dei fusi orari e di altre modifiche di data e ora, ad esempio l'ora legale e le variazioni dell'ora legale a livello di area.

<div id="table-30-utcoffset-field-structure" />

**Tabella 30 Struttura del campo UtcOffset**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(bit)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(bit)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>Questo campo è obbligatorio <a href="#74101-offsetfromutc-field">e la sezione 7.4.10.1</a>ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#74102-offsetvalid-field">e la sezione 7.4.10.2</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>7.4.10.1 Campo OffsetFromUtc

Il campo OffsetFromUtc descrive l'offset dall'ora UTC della data e dell'ora locali contenute nei campi Timestamp e 10msIncrement correlati.
Questo campo descrive l'offset dall'ora UTC a intervalli di 15 minuti (vedere la tabella 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tabella 31 Significato dei valori del campo OffsetFromUtc**

<table>
<thead>
<tr class="header">
<th><strong>Valore</strong></th>
<th><strong>Equivalente decimale con segno</strong></th>
<th><strong>Descrizione</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3Fh</td>
<td>63</td>
<td>La data e l'ora locali sono UTC + 15:45</td>
</tr>
<tr class="even">
<td>3Eh</td>
<td>62</td>
<td>La data e l'ora locali sono UTC + 15:30</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>01h</td>
<td>1</td>
<td>La data e l'ora locali sono UTC + 00:15</td>
</tr>
<tr class="odd">
<td>00h</td>
<td>0</td>
<td>La data e l'ora locali sono UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>La data e l'ora locali sono UTC - 00:15</td>
</tr>
<tr class="odd">
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
<td><p>.</p>
<p>.</p>
<p>.</p></td>
</tr>
<tr class="even">
<td>41 ore</td>
<td>-63</td>
<td>La data e l'ora locali sono UTC - 15:45</td>
</tr>
<tr class="odd">
<td>40 ore</td>
<td>-64</td>
<td>La data e l'ora locali sono UTC - 16:00</td>
</tr>
</tbody>
</table>

Come indicato nella tabella precedente, tutti i valori possibili per questo campo sono validi. Tuttavia, le implementazioni devono registrare solo il valore 00h per questo campo quando:

1. La data e l'ora locali sono in realtà uguali all'ora UTC, nel qual caso il valore del campo OffsetValid deve essere 1

2. La data e l'ora locali non sono note, nel qual caso il valore del campo OffsetValid deve essere 1 e le implementazioni considerino l'ora UTC come data e ora locali

3. UTC non è noto, nel qual caso il valore del campo OffsetValid deve essere 0

Se la differenza di data e ora locale dall'ora UTC non è un multiplo di intervalli di 15 minuti, le implementazioni registrano 00h nel campo OffsetFromUtc e considerano UTC come data e ora locali.

##### <a name="74102-offsetvalid-field"></a>7.4.10.2 Campo OffsetValid

Il campo OffsetValid deve indicare se il contenuto del campo OffsetFromUtc è valido o meno, come indicato di seguito:

- 0, ovvero il contenuto del campo OffsetFromUtc non è valido
    > e devono essere 00h

- 1, ovvero il contenuto del campo OffsetFromUtc è valido

Le implementazioni devono impostare questo campo sul valore 0 solo quando l'ora UTC non è disponibile per il calcolo del valore del campo OffsetFromUtc. Se questo campo contiene il valore 0, le implementazioni devono considerare i campi Timestamp e 10msIncrement come con lo stesso offset UTC della data e dell'ora locali correnti.

### <a name="75-volume-guid-directory-entry"></a>7.5 Voce di directory GUID volume

La voce di directory GUID volume contiene un GUID che consente alle implementazioni di distinguere i volumi in modo univoco e a livello di codice.
Il GUID del volume esiste come voce di directory primaria non dannosa nella directory radice (vedere [la tabella 32).](#table-32-volume-guid-directoryentry) Il numero valido di voci di directory GUID del volume è compreso tra 0 e 1.

<div id="table-32-volume-guid-directoryentry" />

**Tabella 32 Guid volume DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#751-entrytype-field">e la sezione 7.5.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#752-secondarycount-field">e la sezione 7.5.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#753-setchecksum-field">e la sezione 7.5.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#754-generalprimaryflags-field">e la sezione 7.5.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Questo campo è obbligatorio <a href="#755-volumeguid-field">e la sezione 7.5.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>22</td>
<td>10</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>7.5.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1).](#631-entrytype-field)

##### <a name="7511-typecode-field"></a>7.5.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.1).](#6311-typecode-field)

Per la voce di directory GUID volume, il valore valido per questo campo è
0.

##### <a name="7512-typeimportance-field"></a>7.5.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.2).](#6312-typeimportance-field)

Per la voce di directory GUID volume, il valore valido per questo campo è
1.

##### <a name="7513-typecategory-field"></a>7.5.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.1.3).](#6313-typecategory-field)

##### <a name="7514-inuse-field"></a>7.5.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere [la sezione 6.3.1.4).](#6314-inuse-field)

#### <a name="752-secondarycount-field"></a>7.5.2 Campo SecondaryCount

Il campo SecondaryCount deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.2).](#632-secondarycount-field)

Per la voce di directory GUID volume, il valore valido per questo campo è
0.

#### <a name="753-setchecksum-field"></a>7.5.3 Campo SetChecksum

Il campo SetChecksum deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.3).](#633-setchecksum-field)

#### <a name="754-generalprimaryflags-field"></a>7.5.4 Campo GeneralPrimaryFlags

Il campo GeneralPrimaryFlags deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere la sezione [6.3.4)](#634-generalprimaryflags-field)e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7541-allocationpossible-field"></a>7.5.4.1 Campo AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.4.1).](#6341-allocationpossible-field)

Per la voce di directory GUID volume, il valore valido per questo campo è
0.

##### <a name="7542-nofatchain-field"></a>7.5.4.2 Campo NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello Generic Primary DirectoryEntry (vedere [la sezione 6.3.4.2).](#6342-nofatchain-field)

#### <a name="755-volumeguid-field"></a>7.5.5 Campo VolumeGuid

Il campo VolumeGuid deve contenere un GUID che identifica in modo univoco il volume specificato.

Tutti i valori possibili per questo campo sono validi, ad eccezione del GUID Null, ovvero {00000000-0000-0000-0000-000000000000} .

### <a name="76-stream-extension-directory-entry"></a>7.6 Voce della directory dell'estensione del flusso

La voce di directory Estensione flusso è una voce di directory secondaria critica nei set di voci della directory file [(vedere la tabella 33).](#table-33-stream-extension-directoryentry) Il numero valido di voci di directory dell'estensione di flusso in un set di voci della directory File è 1.
Inoltre, questa voce di directory è valida solo se segue immediatamente la voce della directory File.

<div id="table-33-stream-extension-directoryentry" />

**Tabella 33 Estensione del flusso DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#761-entrytype-field">e la sezione 7.6.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#762-generalsecondaryflags-field">e la sezione 7.6.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#763-namelength-field">e la sezione 7.6.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio <a href="#764-namehash-field">e la sezione 7.6.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="odd">
<td>ValidDataLength</td>
<td>8</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#765-validdatalength-field">e la sezione 7.6.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato3</td>
<td>16</td>
<td>4</td>
<td>Questo campo è obbligatorio e il relativo contenuto è riservato.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#766-firstcluster-field">e la sezione 7.6.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#767-datalength-field">e la sezione 7.6.7</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>7.6.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1).](#641-entrytype-field)

##### <a name="7611-typecode-field"></a>7.6.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.1).](#6411-typecode-field)

Per la voce di directory Estensione flusso, il valore valido per questo campo è 0.

##### <a name="7612-typeimportance-field"></a>7.6.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.2).](#6412-typeimportance-field)

Per la voce di directory Estensione flusso, il valore valido per questo campo è 0.

##### <a name="7613-typecategory-field"></a>7.6.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.3).](#6413-typecategory-field)

##### <a name="7614-inuse-field"></a>7.6.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.4).](#6414-inuse-field)

#### <a name="762-generalsecondaryflags-field"></a>7.6.2 Campo GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere la sezione [6.4.2)](#642-generalsecondaryflags-field)e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7621-allocationpossible-field"></a>7.6.2.1 Campo AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.2.1).](#6421-allocationpossible-field)

Per la voce di directory Estensione flusso, il valore valido per questo campo è 1.

##### <a name="7622-nofatchain-field"></a>7.6.2.2 Campo NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.2.2).](#6422-nofatchain-field)

#### <a name="763-namelength-field"></a>7.6.3 Campo NameLength

Il campo NameLength deve contenere la lunghezza della stringa Unicode contenuta collettivamente nelle voci successive della directory Nome file (vedere la sezione [7.7).](#77-file-name-directory-entry)

L'intervallo valido di valori per questo campo deve essere:

- Almeno 1, ovvero il nome file più breve possibile

- Al massimo 255, ovvero il nome file più lungo possibile

Il valore del campo NameLength influisce anche sul numero di voci di directory nome file (vedere [la sezione 7.7).](#77-file-name-directory-entry)

#### <a name="764-namehash-field"></a>7.6.4 Campo NameHash

Il campo NameHash deve contenere un hash a 2 byte (vedere [la figura 4)](#figure-4-namehash-computation)del nome del file con distinzione tra maiuscole e minuscole. Ciò consente alle implementazioni di eseguire un confronto rapido durante la ricerca di un file in base al nome. È importante notare che NameHash fornisce una verifica sicura di una mancata corrispondenza. Le implementazioni devono verificare tutte le corrispondenze nameHash con un confronto del nome file con distinzione tra maiuscole e minuscole.

<div id="figure-4-namehash-computation" />

**Figura 4 Calcolo NameHash**

```C
UInt16 NameHash
(
    WCHAR * FileName,    // points to an in-memory copy of the up-cased file name
    UCHAR   NameLength
)
{
    UCHAR  * Buffer = (UCHAR *)FileName;
    UInt16   NumberOfBytes = (UInt16)NameLength * 2;
    UInt16   Hash = 0;
    UInt16   Index;

    for (Index = 0; Index < NumberOfBytes; Index++)
    {
        Hash = ((Hash&1) ? 0x8000 : 0) + (Hash>>1) + (UInt16)Buffer[Index];
    }
    return Hash;
}
```

#### <a name="765-validdatalength-field"></a>7.6.5 Campo ValidDataLength

Il campo ValidDataLength deve descrivere quanto sono stati scritti i dati utente del flusso di dati. Le implementazioni aggiorneranno questo campo mentre scrivono i dati nel flusso di dati. Nei supporti di archiviazione i dati compresi tra la lunghezza dei dati valida e la lunghezza del flusso di dati non sono definiti. Le implementazioni restituiranno zeri per le operazioni di lettura oltre la lunghezza dei dati valida.

Se la voce di directory File corrispondente descrive una directory, l'unico valore valido per questo campo è uguale al valore del campo DataLength. In caso contrario, l'intervallo di valori validi per questo campo sarà:

- Almeno 0, ovvero nessun dato utente è stato scritto nel flusso di dati

- Al massimo DataLength, il che significa che i dati utente sono stati scritti per l'intera lunghezza del flusso di dati

#### <a name="766-firstcluster-field"></a>7.6.6 Campo FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.3).](#643-firstcluster-field)

Questo campo deve contenere l'indice del primo cluster del flusso di dati, che ospita i dati utente.

#### <a name="767-datalength-field"></a>7.6.7 Campo DataLength

Il campo DataLength deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.4).](#644-datalength-field)

Se la voce di directory File corrispondente descrive una directory, il valore valido per questo campo corrisponde all'intera dimensione dell'allocazione associata, in byte, che può essere 0. Inoltre, per le directory, il valore massimo per questo campo è 256 MB.

### <a name="77-file-name-directory-entry"></a>7.7 Voce di directory nome file

Le voci della directory Nome file sono voci di directory secondarie critiche nei set di voci della directory file (vedere [la tabella 34).](#table-34-file-name-directoryentry) Il numero valido di voci di directory File Name in un set di voci della directory File è NameLength/ 15, arrotondato per esere all'intero più vicino. Inoltre, le voci di directory Nome file sono valide solo se seguono immediatamente la voce di directory Estensione di flusso come serie consecutive. Le voci della directory Nome file vengono combinate in modo da formare il nome file per il set di voci della directory File.

Tutti gli elementi figlio di una determinata voce di directory devono avere set di voci di directory nome file univoci. Ciò significa che non possono essere presenti nomi di file o directory duplicati dopo l'up-casing all'interno di una directory.

<div id="table-34-file-name-directoryentry" />

**Tabella 34 Nome file DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#771-entrytype-field">e la sezione 7.7.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#772-generalsecondaryflags-field">e la sezione 7.7.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Questo campo è obbligatorio <a href="#773-filename-field">e la sezione 7.7.3</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>7.7.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1).](#641-entrytype-field)

##### <a name="7711-typecode-field"></a>7.7.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.1).](#6411-typecode-field)

Per la voce di directory Estensione di flusso, il valore valido per questo campo è 1.

##### <a name="7712-typeimportance-field"></a>7.7.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la Sezione 6.4.1.2).](#6412-typeimportance-field)

Per la voce di directory Dell'estensione di flusso, il valore valido per questo campo è 0.

##### <a name="7713-typecategory-field"></a>7.7.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la Sezione 6.4.1.3).](#6413-typecategory-field)

##### <a name="7714-inuse-field"></a>7.7.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la Sezione 6.4.1.4).](#6414-inuse-field)

#### <a name="772-generalsecondaryflags-field"></a>7.7.2 Campo GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello Generic Secondary DirectoryEntry (vedere la Sezione [6.4.2)](#642-generalsecondaryflags-field)e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7721-allocationpossible-field"></a>7.7.2.1 AllocationPossible Field

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la Sezione 6.4.2.1).](#6421-allocationpossible-field)

Per la voce di directory Dell'estensione di flusso, il valore valido per questo campo è 0.

##### <a name="7722-nofatchain-field"></a>7.7.2.2 Campo NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la Sezione 6.4.2.2).](#6422-nofatchain-field)

#### <a name="773-filename-field"></a>7.7.3 Campo FileName

Il campo FileName deve contenere una stringa Unicode, ovvero una parte del nome file. Nell'ordine in cui le voci di directory File Name sono presenti in un set di voci di directory File, i campi FileName vengono concatenati per formare il nome file per il set di voci della directory File. Data la lunghezza del campo FileName, 15 caratteri e il numero massimo di voci di directory File Name, 17, la lunghezza massima del nome file concatenato finale è 17.
255.

Il nome file concatenato ha lo stesso set di caratteri non validi degli altri file system basati su FAT (vedere [la tabella 35).](#table-35-invalid-filename-characters) Le implementazioni devono impostare i caratteri inutilizzati dei campi FileName sul valore 0000h.

<div id="table-35-invalid-filename-characters" />

**Tabella 35 Caratteri fileName non validi**

| **Codice carattere** | **Descrizione** | **Codice carattere** | **Descrizione**   | **Codice carattere** | **Descrizione** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | Codice di controllo    | 0001h              | Codice di controllo      | 0002h              | Codice di controllo    |
| 0003h              | Codice di controllo    | 0004h              | Codice di controllo      | 0005h              | Codice di controllo    |
| 0006h              | Codice di controllo    | 0007h              | Codice di controllo      | 0008h              | Codice di controllo    |
| 0009h              | Codice di controllo    | 000Ah              | Codice di controllo      | 000Bh              | Codice di controllo    |
| 000Ch              | Codice di controllo    | 000Dh              | Codice di controllo      | 000Eh              | Codice di controllo    |
| 000Fh              | Codice di controllo    | 0010h              | Codice di controllo      | 0011h              | Codice di controllo    |
| 0012h              | Codice di controllo    | 0013h              | Codice di controllo      | 0014h              | Codice di controllo    |
| 0015h              | Codice di controllo    | 0016h              | Codice di controllo      | 0017h              | Codice di controllo    |
| 0018h              | Codice di controllo    | 0019h              | Codice di controllo      | 001Ah              | Codice di controllo    |
| 001Bh              | Codice di controllo    | 001Ch              | Codice di controllo      | 001Dh              | Codice di controllo    |
| 001Eh              | Codice di controllo    | 001Fh              | Codice di controllo      | 0022h              | Virgoletta  |
| 002Ah              | Asterisco        | 002Fh              | Barra     | 003Ah              | Due punti           |
| 003Ch              | Segno di minore a  | 003Eh              | Segno di maggiore di | 003Fh              | Punto interrogativo   |
| 005Ch              | Barra rovesciata      | 007Ch              | Barra verticale      |                    |                 |

I nomi di file "." e ".." hanno rispettivamente il significato speciale di "questa directory" e "directory contenitore". Le implementazioni non devono registrare uno di questi nomi di file riservati nel campo FileName.
Tuttavia, le implementazioni possono generare questi due nomi di file negli elenchi di directory per fare riferimento alla directory elencata e alla directory contenitore.

Le implementazioni possono voler limitare i nomi di file e directory solo al set di caratteri ASCII. In tal caso, è necessario limitare l'utilizzo dei caratteri all'intervallo di caratteri validi nelle prime 128 voci Unicode. Devono comunque archiviare i nomi di file e directory in Unicode nel volume e convertirsi in/da ASCII/Unicode durante l'interfacciamento con l'utente.

### <a name="78-vendor-extension-directory-entry"></a>7.8 Voce della directory dell'estensione del fornitore

La voce di directory Vendor Extension è una voce di directory secondaria non dannosa nei set di voci della directory File (vedere [la tabella 36).](#table-36-vendor-extension-directoryentry) Un set di voci della directory File può contenere un numero qualsiasi di voci di directory vendor extension, fino al limite di voci di directory secondarie, meno il numero di altre voci di directory secondarie. Inoltre, le voci della directory Vendor Extension sono valide solo se non precedono le voci di directory Stream Extension e File Name obbligatorie.

Le voci della directory Vendor Extension consentono ai fornitori di avere voci di directory univoche specifiche del fornitore nei singoli set di voci della directory File tramite il campo VendorGuid (vedere [la tabella 36).](#table-36-vendor-extension-directoryentry) Le voci di directory univoche consentono ai fornitori di estendere in modo efficace il file system exFAT. I fornitori possono definire il contenuto del campo VendorDefined (Vedere [la tabella 36).](#table-36-vendor-extension-directoryentry) Le implementazioni del fornitore possono mantenere il contenuto del campo VendorDefined e possono fornire funzionalità specifiche del fornitore.

Le implementazioni che non riconoscono il GUID di una voce di directory dell'estensione fornitore devono considerare la voce di directory come qualsiasi altra voce di directory secondaria non riconosciuta non riconosciuta (vedere la sezione [8.2).](#82-implications-of-unrecognized-directory-entries)

<div id="table-36-vendor-extension-directoryentry" />

**Tabella 36 Vendor Extension DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#781-entrytype-field">e la sezione 7.8.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#782-generalsecondaryflags-field">e la sezione 7.8.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Guid fornitore</td>
<td>2</td>
<td>16</td>
<td>Questo campo è obbligatorio <a href="#783-vendorguid-field">e la sezione 7.8.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Definito dal fornitore</td>
<td>18</td>
<td>14</td>
<td>Questo campo è obbligatorio e i fornitori possono definirne il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>7.8.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1).](#641-entrytype-field)

##### <a name="7811-typecode-field"></a>7.8.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.1).](#6411-typecode-field)

Per la voce di directory Vendor Extension il valore valido per questo campo è 0.

##### <a name="7812-typeimportance-field"></a>7.8.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.2).](#6412-typeimportance-field)

Per la voce di directory Vendor Extension il valore valido per questo campo è 1.

##### <a name="7813-typecategory-field"></a>7.8.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.3).](#6413-typecategory-field)

##### <a name="7814-inuse-field"></a>7.8.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.4).](#6414-inuse-field)

#### <a name="782-generalsecondaryflags-field"></a>7.8.2 Campo GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere la sezione [6.4.2)](#642-generalsecondaryflags-field)e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7821-allocationpossible-field"></a>7.8.2.1 Campo AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.2.1).](#6421-allocationpossible-field)

Per la voce di directory Vendor Extension il valore valido per questo campo è 0.

##### <a name="7822-nofatchain-field"></a>7.8.2.2 Campo NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.2.2).](#6422-nofatchain-field)

#### <a name="783-vendorguid-field"></a>7.8.3 Campo VendorGuid

Il campo VendorGuid deve contenere un GUID che identifica in modo univoco l'estensione fornitore specificata.

Tutti i valori possibili per questo campo sono validi, ad eccezione del GUID Null, ovvero {00000000-0000-0000-0000-000000000000} . Tuttavia, i fornitori devono usare uno strumento per la generazione di GUID, ad esempio GuidGen.exe, per selezionare un GUID durante la definizione delle estensioni.

Il valore di questo campo determina la struttura specifica del fornitore del campo VendorDefined.

### <a name="79-vendor-allocation-directory-entry"></a>7.9 Voce della directory di allocazione del fornitore

La voce della directory Vendor Allocation è una voce di directory secondaria non dannosa nei set di voci della directory File (vedere [la tabella 37).](#table-37-vendor-allocation-directoryentry) Un set di voci della directory File può contenere un numero qualsiasi di voci della directory Vendor Allocation, fino al limite di voci di directory secondarie, meno il numero di altre voci di directory secondarie. Inoltre, le voci della directory Vendor Allocation (Allocazione fornitore) sono valide solo se non precedono le voci di directory Relative all'estensione di flusso e al nome file necessarie.

Le voci della directory Vendor Allocation consentono ai fornitori di avere voci di directory univoche specifiche del fornitore nei singoli set di voci della directory File tramite il campo VendorGuid (vedere [la tabella 37).](#table-37-vendor-allocation-directoryentry) Le voci di directory univoche consentono ai fornitori di estendere in modo efficace il file system exFAT. I fornitori possono definire il contenuto dei cluster associati, se presenti. Le implementazioni del fornitore possono mantenere il contenuto dei cluster associati, se presenti, e possono fornire funzionalità specifiche del fornitore.

Le implementazioni che non riconoscono il GUID di una voce di directory Vendor Allocation devono considerare la voce di directory come qualsiasi altra voce di directory secondaria non riconosciuta non riconosciuta (vedere la sezione [8.2).](#82-implications-of-unrecognized-directory-entries)

<div id="table-37-vendor-allocation-directoryentry" />

**Tabella 37 Vendor Allocation DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Entrytype</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#791-entrytype-field">e la sezione 7.9.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio <a href="#792-generalsecondaryflags-field">e la sezione 7.9.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Guid fornitore</td>
<td>2</td>
<td>16</td>
<td>Questo campo è obbligatorio <a href="#793-vendorguid-field">e la sezione 7.9.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Definito dal fornitore</td>
<td>18</td>
<td>2</td>
<td>Questo campo è obbligatorio e i fornitori possono definirne il contenuto.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio <a href="#794-firstcluster-field">e la sezione 7.9.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio <a href="#795-datalength-field">e la sezione 7.9.5</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>7.9.1 Campo EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1).](#641-entrytype-field)

##### <a name="7911-typecode-field"></a>7.9.1.1 Campo TypeCode

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.1).](#6411-typecode-field)

Per la voce della directory Vendor Allocation (Allocazione fornitore), il valore valido per questo campo è 1.

##### <a name="7912-typeimportance-field"></a>7.9.1.2 Campo TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.2).](#6412-typeimportance-field)

Per la voce della directory Vendor Allocation (Allocazione fornitore), il valore valido per questo campo è 1.

##### <a name="7913-typecategory-field"></a>7.9.1.3 Campo TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.3).](#6413-typecategory-field)

##### <a name="7914-inuse-field"></a>7.9.1.4 Campo InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.1.4).](#6414-inuse-field)

#### <a name="792-generalsecondaryflags-field"></a>7.9.2 Campo GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere la sezione [6.4.2)](#642-generalsecondaryflags-field)e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7921-allocationpossible-field"></a>7.9.2.1 Campo AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.2.1).](#6421-allocationpossible-field)

Per la voce della directory Vendor Allocation (Allocazione fornitore), il valore valido per questo campo è 1.

##### <a name="7922-nofatchain-field"></a>7.9.2.2 Campo NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.2.2).](#6422-nofatchain-field)

#### <a name="793-vendorguid-field"></a>7.9.3 Campo VendorGuid

Il campo VendorGuid deve contenere un GUID che identifica in modo univoco l'allocazione del fornitore specificata.

Tutti i valori possibili per questo campo sono validi, ad eccezione del GUID Null, ovvero {00000000-0000-0000-0000-000000000000} . Tuttavia, i fornitori devono usare uno strumento per la generazione di GUID, ad esempio GuidGen.exe, per selezionare un GUID durante la definizione delle estensioni.

Il valore di questo campo determina la struttura specifica del fornitore del contenuto dei cluster associati, se presenti.

#### <a name="794-firstcluster-field"></a>7.9.4 Campo FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.3).](#643-firstcluster-field)

#### <a name="795-datalength-field"></a>7.9.5 Campo DataLength

Il campo DataLength deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere [la sezione 6.4.4).](#644-datalength-field)

### <a name="710-texfat-padding-directory-entry"></a>7.10 Voce della directory padding TexFAT

Questa specifica, exFAT Revision 1.00 File System Basic Specification, non definisce la voce di directory TexFAT Padding. Tuttavia, il codice del tipo è 1 e l'importanza del tipo è 1. Le implementazioni di questa specifica trattano le voci di directory TexFAT Padding come qualsiasi altra voce di directory primaria non riconosciuta, le implementazioni non devono spostare le voci della directory TexFAT Padding.

## <a name="8-implementation-notes"></a>8 Note sull'implementazione

### <a name="81-recommended-write-ordering"></a>8.1 Ordinamento di scrittura consigliato

Le implementazioni devono garantire che il volume sia il più resiliente possibile per gli errori di alimentazione e altri errori inevitabili. Quando si creano nuove voci di directory o si modificano le allocazioni di cluster, le implementazioni devono in genere seguire questo ordine di scrittura:

1. Impostare il valore del campo VolumeDirty su 1

2. Aggiornare il fat attivo, se necessario

3. Aggiornare la bitmap di allocazione attiva

4. Creare o aggiornare la voce di directory, se necessario

5. Cancellare il valore del campo VolumeDirty su 0, se il valore precedente al primo passaggio era 0

Quando si eliminano voci di directory o si liberano allocazioni di cluster, le implementazioni devono seguire questo ordine di scrittura:

1. Impostare il valore del campo VolumeDirty su 1

2. Eliminare o aggiornare la voce di directory, se necessario

3. Aggiornare il fat attivo, se necessario

4. Aggiornare la bitmap di allocazione attiva

5. Cancellare il valore del campo VolumeDirty su 0, se il valore precedente al primo passaggio era 0

### <a name="82-implications-of-unrecognized-directory-entries"></a>8.2 Implicazioni delle voci di directory non riconoscite

Le specifiche exFAT future dello stesso numero di revisione principale, 1 e numero di revisione secondaria maggiore di 0, possono definire nuove voci di directory primarie non dannose, secondarie critiche e secondarie non dannose. Solo le specifiche exFAT di un numero di revisione principale superiore possono definire nuove voci critiche della directory primaria. Le implementazioni di questa specifica, exFAT Revision 1.00 File System Basic Specification, devono essere in grado di montare e accedere a qualsiasi volume exFAT del numero di revisione principale 1 e a qualsiasi numero di revisione secondaria. Vengono presentati scenari in cui un'implementazione può riscontrare voci di directory che non riconosce. Di seguito vengono descritte le implicazioni di questi scenari:

1. La presenza di voci di directory primarie critiche non riconoscite nella directory radice rende il volume non valido. La presenza di qualsiasi voce di directory primaria critica, ad eccezione delle voci della directory File, in qualsiasi directory non radice rende non valida la directory di hosting.

2. Le implementazioni non devono modificare le voci di directory primarie non riconoscite non riconoscite o le allocazioni cluster associate. Tuttavia, quando si elimina una directory e solo quando si elimina una directory, le implementazioni eliminano le voci di directory primarie non riconoscite e liberano tutte le allocazioni cluster associate, se presenti.

3. Le implementazioni non devono modificare le voci di directory secondarie critiche non riconoscite o le allocazioni cluster associate. La presenza di una o più voci di directory secondarie critiche non riconoscite in un set di voci di directory rende non riconosciuto l'intero set di voci di directory. Quando si elimina un set di voci di directory che contiene una o più voci di directory secondarie critiche non riconoscite, le implementazioni liberano tutte le allocazioni cluster, se presenti, associate a voci di directory secondarie critiche non riconoscite.
   Inoltre, se il set di voci di directory descrive una directory, le implementazioni possono:

   - Attraversa nella directory

   - Enumerare le voci di directory in essa contenute

   - Eliminare le voci di directory contenute

   - Spostare le voci di directory contenute in una directory diversa

   Tuttavia, le implementazioni non devono:

   - Modificare le voci di directory contenute, ad eccezione dell'eliminazione, come illustrato

   - Creare nuove voci di directory contenute

   - Aprire le voci di directory contenute, ad eccezione dell'attraversamento e dell'enumerazione, come illustrato

4. Le implementazioni non devono modificare le voci di directory secondarie non riconoscite non riconoscite o le allocazioni cluster associate.
   Le implementazioni devono ignorare le voci di directory secondarie non riconosciizzate. Quando si elimina un set di voci di directory, le implementazioni liberano tutte le eventuali allocazioni di cluster associate a voci di directory secondarie non riconoscite.

## <a name="9-file-system-limits"></a>9 Limiti del file system

### <a name="91-sector-size-limits"></a>9.1 Limiti delle dimensioni del settore

Il campo BytesPerSectorShift definisce i limiti delle dimensioni del settore inferiore e superiore (che restituisce un limite **inferiore: 512 byte; limite superiore: 4.096 byte).**

### <a name="92-cluster-size-limits"></a>9.2 Limiti delle dimensioni del cluster

Il campo SectorPerClusterShift definisce i limiti inferiori e superiori delle dimensioni del cluster ( limite **inferiore: 1 settore; limite superiore: 25 -- Settori BytesPerSectorShift**, che restituisce 32 MB).

### <a name="93-cluster-heap-size-limits"></a>9.3 Limiti delle dimensioni dell'heap del cluster

L'heap del cluster deve contenere almeno spazio sufficiente per ospitare le strutture di file system di base seguenti: la directory radice, tutte le bitmap di allocazione e la tabella up case.

Il limite inferiore per le dimensioni dell'heap del cluster è una funzione del limite inferiore delle dimensioni di ognuna delle strutture di file system di base che risiedono nell'heap del cluster. Anche considerando il cluster più piccolo possibile (512 byte), ognuna delle strutture di base file system non richiede più di un cluster. Di conseguenza, il limite inferiore **è: 2 + NumberOfFats clusters**, che restituisce 3 o 4 cluster, a seconda del valore del campo NumberOfFats.

Il limite superiore per le dimensioni dell'heap del cluster è una semplice funzione del numero massimo possibile di cluster definito dal campo ClusterCount (**limite superiore: 2 <sup>32</sup>- 11 cluster).** Indipendentemente dalle dimensioni del cluster, tale heap del cluster dispone di spazio sufficiente per ospitare almeno le strutture file system base.

### <a name="94-volume-size-limits"></a>9.4 Limiti delle dimensioni del volume

Il campo VolumeLength definisce i limiti inferiori e superiori delle dimensioni del volume (limite inferiore: **<sup>2 settori 2 20/2</sup><sup>BytesPerSectorShift,</sup>** che restituisce 1 MB; **limite superiore: 2 <sup>64</sup>- 1** settore, che, data la dimensione massima possibile del settore, restituisce circa 64ZB). Tuttavia, questa specifica consiglia non più di<sup>2 cluster da 24</sup>a 2 nell'heap del cluster (vedere la [sezione 3.1.9).](#319-clustercount-field) Pertanto, il limite superiore consigliato di un volume è: ClusterHeapOffset +<sup>(2 24</sup>- 2) \* 2<sup>SettoriPerClusterShift</sup>. Data la dimensione massima possibile del cluster, 32 MB e presupponendo che ClusterHeapOffset sia di 96 MB (spazio sufficiente per le aree di avvio principale e di backup e solo la prima FAT), il limite superiore consigliato di un volume restituisce circa 512 TB.

### <a name="95-directory-size-limits"></a>9.5 Limiti delle dimensioni della directory

Il campo DataLength della voce di directory Estensione di flusso definisce i limiti delle dimensioni della directory inferiore e superiore ( limite **inferiore: 0 byte; limite superiore: 256 MB).** Ciò significa che una directory può ospitare fino a 8.388.608 voci di directory (ogni voce di directory utilizza 32 byte). Dato il set di voci di directory File più piccolo possibile, tre voci di directory, una directory può ospitare fino a 2.796.202 file.

## <a name="10-appendix"></a>10 Appendice

### <a name="101-globally-unique-identifiers-guids"></a>10.1 Identificatori univoci globali (GUID)

Un GUID è l'implementazione Microsoft di un identificatore univoco universale. Un GUID è un valore a 128 bit costituito da un gruppo di 8 cifre esadecimali, seguito da tre gruppi di 4 cifre esadecimali e da un gruppo di 12 cifre esadecimali, ad esempio {6B29FC40-CA47-1067-B31D-00D010662DA}, (vedere la tabella [38](#table-38-guid-structure)).

<div id="table-38-guid-structure" />

**Tabella 38 Struttura GUID**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>(byte)</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>(byte)</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
<td>0</td>
<td>4</td>
<td>Questo campo è obbligatorio e contiene i quattro byte del primo gruppo del GUID (6B29FC40h dell'esempio).</td>
</tr>
<tr class="even">
<td>Data2</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio e contiene i due byte del secondo gruppo del GUID (CA47h dell'esempio).</td>
</tr>
<tr class="odd">
<td>Data3</td>
<td>6</td>
<td>2</td>
<td>Questo campo è obbligatorio e contiene i due byte del terzo gruppo del GUID (1067h dall'esempio).</td>
</tr>
<tr class="even">
<td>Data4[0]</td>
<td>8</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il byte più significativo del quarto gruppo del GUID (B3h dell'esempio).</td>
</tr>
<tr class="odd">
<td>Data4[1]</td>
<td>9</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il byte meno significativo del quarto gruppo del GUID (1Dh dall'esempio).</td>
</tr>
<tr class="even">
<td>Data4[2]</td>
<td>10</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il primo byte del quinto gruppo del GUID (00h dall'esempio).</td>
</tr>
<tr class="odd">
<td>Data4[3]</td>
<td>11</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il secondo byte del quinto gruppo del GUID (DDh dell'esempio).</td>
</tr>
<tr class="even">
<td>Data4[4]</td>
<td>12</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il terzo byte del quinto gruppo del GUID (01h dall'esempio).</td>
</tr>
<tr class="odd">
<td>Data4[5]</td>
<td>13</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il quarto byte del quinto gruppo del GUID (06h dall'esempio).</td>
</tr>
<tr class="even">
<td>Data4[6]</td>
<td>14</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il quinto byte del quinto gruppo del GUID (62 ore dall'esempio).</td>
</tr>
<tr class="odd">
<td>Data4[7]</td>
<td>15</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il sesto byte del quinto gruppo del GUID (DAh dell'esempio).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10.2 Tabelle di partizione

Per garantire l'interoperabilità dei volumi exFAT in un ampio set di scenari di utilizzo, le implementazioni devono usare il tipo di partizione 07h per l'archiviazione partizionata MBR e il GUID di partizione {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} per l'archiviazione partizionata GPT.

## <a name="11-documentation-change-history"></a>11 Cronologia delle modifiche della documentazione

La tabella 39 descrive la cronologia delle versioni, le correzioni a, le aggiunte, le rimozioni da e i chiarimenti di questo documento.

<div id="table-39-documentation-change-history" />

**Tabella 39 Cronologia delle modifiche della documentazione**

<table>
<thead>
<tr class="header">
<th><strong>Data</strong></th>
<th><strong>Descrizione di Modifica</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08-Gen-2008</td>
<td><p>Prima versione della specifica di base, che include:</p>
<blockquote>
<p>Sezione 1, Introduzione</p>
<p>Sezione 2,<br />
Struttura del volume</p>
<p>Sezione 3, Aree di avvio principale e di backup</p>
<p>Sezione 4, Area tabella di allocazione file</p>
<p>Sezione 5, Area dati</p>
<p>Sezione 6, Struttura della directory</p>
<p>Sezione 7, Definizioni delle voci di directory</p>
<p>Sezione 8, Note sull'implementazione</p>
<p>Sezione 9, Limiti del file system</p>
<p>Sezione 10, Appendice</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-Jun-2008</td>
<td><p>Seconda versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Aggiunta della sezione 11,<br />
Cronologia delle modifiche della documentazione</p>
<p>Aggiunta delle voci di directory Vendor Extension e Vendor Allocation nelle sezioni 7.8 e 7.9</p>
<p>Aggiunta della tabella up-case consigliata nelle sezioni 7.2.5 e 7.2.5.1</p>
<p>Aggiunta dei campi UtcOffset nella Sezione 7.4 e aggiunta dell'acronimo UTC nella Sezione 1.3</p>
<p>Correzione delle dimensioni del campo CustomDefined nella tabella 19</p>
<p>Correzione dell'intervallo valido di valori NameLength nella sezione 7.6.3</p>
<p>Correzione e chiarimento dei campi Timestamp e 10msIncrement nella Sezione 7.4</p>
<p>Chiarimento della struttura Dei parametri Null nella sezione 3.3</p>
<p>Chiarimento del significato dei valori del campo NoFatChain nella Sezione 6.3.4.2</p>
<p>Chiarimento del significato dei valori del campo DataLength nella Sezione 6.2.3</p>
<p>Chiarimento del campo VolumeDirty nella Sezione 3.1.13.2 e ordinamento di scrittura consigliato nella sezione 8.1</p>
<p>Chiarimento del campo MediaFailure nella Sezione 3.1.13.3</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01-Oct-2008</td>
<td><p>Terza versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Aggiunta di SHALL, SHOULD e MAY alle spiegazioni dei campi</p>
<p>Aggiunta della definizione UTC nella tabella 2 Sezione 1.3</p>
<p>È stata modificata la sezione 1.5 per garantire l'allineamento con il documento di specifica TexFAT.</p>
<p>È stata chiarita la restrizione che solo Microsoft può definire il layout delle voci di directory nella sezione 6.2</p>
<p>Aggiunta del chiarimento che FirstCluster Field deve essere zero se DataLength è zero e NoFatChain è impostato su Section 6.3.5 e Section 6.4.3</p>
<p>Chiarimento dei requisiti per le voci di directory di file valide nella sezione 7.4</p>
<p>Aggiunta del requisito per i nomi univoci di file e directory alla sezione 7.7</p>
<p>Aggiunta della nota di implementazione per ASCII alla fine della sezione 7.7.3</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-Jan-2009</td>
<td><p>Quarta versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Rimozione dei riferimenti alle Windows CE di controllo di accesso</p>
<p>Aggiunta di chiarimenti alla sezione 7.2.5.1 per richiedere in modo esplicito una tabella up-case completa</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02 set-2009</td>
<td><p>Quinta versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Modifiche alla formattazione dei documenti per consentire una migliore conversione pdf</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24 febbraio 2010</td>
<td><p>Sesta versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Istruzione errata corretta: "FirstCluster Field shall be zero if the DataLength is zero and NoFatChain is set" in Section 6.3.5 and Section 6.4.3 to "If the NoFatChain bit is 1 then FirstCluster must point to a valid cluster in the cluster heap" (Se il bit NoFatChain è 1, FirstCluster deve puntare a un cluster valido nell'heap del cluster) per chiarire che deve essere presente un'allocazione valida se il bit NoFatChain è impostato.</p>
<p>Aggiunta di "Se il bit NoFatChain è 1, DataLength non deve essere zero. Se il campo FirstCluster è zero, anche DataLength deve essere zero" in Section 6.3.6 e Section 6.4.4 per chiarire che deve essere presente un'allocazione valida se è impostato il bit NoFatChain.</p>
<p>Aggiornamento delle informazioni sul copyright al 2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26 ago 2019</td>
<td><p>Settima versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Note legali aggiornate relative alla specifica, tra cui:</p>
<p>Rimozione delle comunicazioni riservate Microsoft</p>
<p>Rimozione della sezione Microsoft Corporation contratto di licenza per la documentazione tecnica</p>
<p>Aggiornamento delle informazioni sul copyright al 2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
