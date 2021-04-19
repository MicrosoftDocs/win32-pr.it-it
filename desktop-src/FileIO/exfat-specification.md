---
description: Specifica del file system exFat.
title: Specifica file system exFAT
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: c23a1f0c7aa9f0ad4752ce83cb734e753094c2cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317805"
---
# <a name="exfat-file-system-specification"></a>Specifica file system exFAT

## <a name="1-introduction"></a>1 Introduzione

Il file system exFAT è il successore di FAT32 nella famiglia di file system FAT. Questa specifica descrive la file system exFAT e fornisce tutte le informazioni necessarie per l'implementazione del file system exFAT.

### <a name="11-design-goals"></a>1,1 obiettivi di progettazione

Il file system exFAT presenta tre obiettivi di progettazione centrali (vedere l'elenco riportato di seguito).

1. *Mantenere la semplicità dei file System basati su FAT.*

   > Due dei punti di forza dei file System basati su FAT sono la semplicità relativa e la semplicità di implementazione. Nello spirito dei suoi predecessori, i responsabili dell'implementazione dovrebbero trovare exFAT relativamente semplici e facili da implementare.

2. *Abilitare file e dispositivi di archiviazione di grandi dimensioni.*

   > Il file system exFAT utilizza 64 bit per descrivere le dimensioni del file, abilitando in questo modo le applicazioni che dipendono da file di grandi dimensioni. Il file system exFAT consente inoltre i cluster di dimensioni maggiori di 32 MB, abilitando efficacemente dispositivi di archiviazione di grandi dimensioni.

3. *Incorporare l'estendibilità per un'innovazione futura.*

   > Il exFAT file system incorpora l'estendibilità nella progettazione, consentendo al file system di rimanere al passo con le innovazioni di archiviazione e le modifiche all'utilizzo.

### <a name="12-specific-terminology"></a>1,2 terminologia specifica

Nel contesto di questa specifica, determinati termini (vedere la [tabella 1](#table-1-definition-of-terms-which-carry-very-specific-meaning)) presentano un significato specifico per la progettazione e l'implementazione del file system exFAT.

<div id="table-1-definition-of-terms-which-carry-very-specific-meaning" />

**Tabella 1 definizione dei termini che contengono un significato molto specifico**

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
<td>Questa specifica USA il termine "shall" per descrivere un comportamento obbligatorio.</td>
</tr>
<tr class="even">
<td>Dovrebbe</td>
<td>Questa specifica USA il termine "should" per descrivere un comportamento consigliato, ma non rende obbligatorio.</td>
</tr>
<tr class="odd">
<td>Mag</td>
<td>Questa specifica USA il termine "May" per descrivere un comportamento facoltativo.</td>
</tr>
<tr class="even">
<td>Obbligatorio</td>
<td>Questo termine descrive un campo o una struttura che un'implementazione deve modificare e interpretare come descritto in questa specifica.</td>
</tr>
<tr class="odd">
<td>Facoltativo</td>
<td>Questo termine descrive un campo o una struttura che un'implementazione può o meno supportare. Se un'implementazione supporta una determinata struttura o un campo facoltativo, deve modificare e interpretare il campo o la struttura come descritto in questa specifica.</td>
</tr>
<tr class="even">
<td>Non definito</td>
<td>Questo termine descrive il contenuto di un campo o di una struttura che può essere modificato in base alle esigenze, ad esempio da Clear a zero quando si impostano i campi o le strutture circostanti, e non deve interpretare per mantenere un significato specifico.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td><p>Questo termine descrive il contenuto del campo o della struttura che implementa:</p>
<ol type="1">
<li><p>Deve essere inizializzato su zero e non deve essere usato per alcuno scopo</p></li>
<li><p>Non deve interpretare, tranne quando si calcolano i checksum</p></li>
<li><p>Deve mantenere tra le operazioni che modificano i campi o le strutture circostanti</p></li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="13-full-text-of-common-acronyms"></a>1,3 testo completo degli acronimi comuni

Questa specifica USA gli acronimi in uso comune nel settore personal computer (vedere la [tabella 2](#table-2-full-text-of-common-acronyms)).

<div id="table-2-full-text-of-common-acronyms" />

**Tabella 2 testo completo degli acronimi comuni**

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
| GUID        | Identificatore univoco globale (vedere la [sezione 10,1](#101-globally-unique-identifiers-guids))      |
| INT         | Interrompere                                          |
| MBR         | record di avvio principale                                 |
| texFAT      | ExFAT indipendente dalle transazioni                             |
| UTC         | Ora UTC (Coordinated Universal Time)                         |

### <a name="14-default-field-and-structure-qualifiers"></a>1,4 qualificatori di campo e struttura predefiniti

I campi e le strutture in questa specifica hanno i qualificatori seguenti (vedere l'elenco riportato di seguito), a meno che non venga annotata diversamente dalla specifica.

1. Non firmato

2. Usare la notazione decimale per descrivere i valori, laddove non diversamente specificato; Questa specifica USA la lettera "h" post-correzione per indicare i numeri esadecimali e racchiude i GUID tra parentesi graffe

3. Sono in formato little-endian

4. Non richiede un carattere di terminazione null per le stringhe

### <a name="15-windows-ce-and-texfat"></a>1,5 Windows CE e TexFAT

TexFAT è un'estensione di exFAT che aggiunge una semantica operativa indipendente dalle transazioni nella parte superiore del file system di base. TexFAT viene usato da Windows CE.
TexFAT richiede l'utilizzo dei due grassi e delle bitmap di allocazione da utilizzare nelle transazioni. Definisce inoltre diverse strutture aggiuntive, tra cui descrittori di riempimento e descrittori di sicurezza.

## <a name="2-volume-structure"></a>2 struttura del volume

Un volume è il set di tutte le strutture file system e lo spazio dati necessario per archiviare e recuperare i dati utente. Tutti i volumi exFAT contengono quattro aree (vedere la [tabella 3](#table-3-volume-structure)).

<div id="table-3-volume-structure" />

**Tabella 3 struttura del volume**

<table>
<thead>
<tr class="header">
<th><strong>Nome dell'area secondaria</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>settore</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>settori</strong></p></th>
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
<td>Questa area secondaria è obbligatoria e la <a href="#31-main-and-backup-boot-sector-sub-regions">sezione 3,1</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Principali settori di avvio esteso</td>
<td>1</td>
<td>8</td>
<td>Questa area secondaria è obbligatoria e la <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">sezione 3,2</a>) ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Parametri OEM principali</td>
<td>9</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e la <a href="#33-main-and-backup-oem-parameters-sub-regions">sezione 3,3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Principale riservato</td>
<td>10</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e i relativi contenuti sono riservati.</td>
</tr>
<tr class="even">
<td>Checksum di avvio principale</td>
<td>11</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e la <a href="#34-main-and-backup-boot-checksum-sub-regions">sezione 3,4</a> ne definisce il contenuto.</td>
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
<td>Questa area secondaria è obbligatoria e la <a href="#31-main-and-backup-boot-sector-sub-regions">sezione 3,1</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Backup dei settori di avvio esteso</td>
<td>13</td>
<td>8</td>
<td>Questa area secondaria è obbligatoria e la <a href="#32-main-and-backup-extended-boot-sectors-sub-regions">sezione 3,2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Parametri OEM di backup</td>
<td>21</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e la <a href="#33-main-and-backup-oem-parameters-sub-regions">sezione 3,3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Backup riservato</td>
<td>22</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e i relativi contenuti sono riservati.</td>
</tr>
<tr class="even">
<td>Checksum di avvio di backup</td>
<td>23</td>
<td>1</td>
<td>Questa area secondaria è obbligatoria e la <a href="#34-main-and-backup-boot-checksum-sub-regions">sezione 3,4</a> ne definisce il contenuto.</td>
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
<td>FatOffset-24</td>
<td><p>Questa area secondaria è obbligatoria e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo FatOffset.</p></td>
</tr>
<tr class="odd">
<td>Primo FAT</td>
<td>FatOffset</td>
<td>FatLength</td>
<td><p>Questa area secondaria è obbligatoria e la <a href="#41-first-and-second-fat-sub-regions">sezione 4,1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi FatOffset e FatLength.</p></td>
</tr>
<tr class="even">
<td>Secondo FAT</td>
<td>FatOffset + FatLength</td>
<td>FatLength * (NumberOfFats-1)</td>
<td><p>Questa area secondaria è obbligatoria e la <a href="#41-first-and-second-fat-sub-regions">sezione 4,1</a> ne definisce il contenuto, se disponibile.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi FatOffset, FatLength e NumberOfFats. Il campo NumberOfFats può conservare solo i valori 1 e 2.</p></td>
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
<td>ClusterHeapOffset-(FatOffset + FatLength * NumberOfFats)</td>
<td><p>Questa area secondaria è obbligatoria e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi FatOffset, FatLength, NumberOfFats e ClusterHeapOffset. I valori validi del campo NumberOfFats sono 1 e 2.</p></td>
</tr>
<tr class="odd">
<td>Heap cluster</td>
<td>ClusterHeapOffset</td>
<td>Clustercount-* 2<sup>SectorsPerClusterShift</sup></td>
<td><p>Questa area secondaria è obbligatoria e la <a href="#51-cluster-heap-sub-region">sezione 5,1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi ClusterHeapOffset, Clustercount-e SectorsPerClusterShift.</p></td>
</tr>
<tr class="even">
<td>Spazio in eccesso</td>
<td>ClusterHeapOffset + Clustercount-* 2<sup>SectorsPerClusterShift</sup></td>
<td>VolumeLength – (ClusterHeapOffset + Clustercount-* 2<sup>SectorsPerClusterShift</sup>)</td>
<td><p>Questa area secondaria è obbligatoria e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi ClusterHeapOffset, Clustercount-, SectorsPerClusterShift e VolumeLength.</p></td>
</tr>
</tbody>
</table>

## <a name="3-main-and-backup-boot-regions"></a>3 aree di avvio principali e di backup

L'area di avvio principale fornisce tutte le istruzioni necessarie per l'avvio, le informazioni di identificazione e i parametri di file system per consentire a un'implementazione di eseguire le operazioni seguenti:

1. Eseguire il Boot-strap di un sistema di computer da un volume exFAT.

2. Identificare il file system nel volume come exFAT.

3. Individuare il percorso delle strutture di file system exFAT.

L'area di avvio del backup è un backup dell'area di avvio principale. Aiuta il ripristino del volume exFAT nel caso in cui l'area di avvio principale sia in uno stato incoerente. Tranne che in circostanze non frequenti, ad esempio l'aggiornamento delle istruzioni di strappo, le implementazioni non devono modificare il contenuto dell'area di avvio del backup.

### <a name="31-main-and-backup-boot-sector-sub-regions"></a>3,1 aree secondarie del settore di avvio principale e di backup

Il settore di avvio principale contiene il codice per la reggiatura da un volume exFAT e i parametri di exFAT fondamentali che descrivono la struttura del volume (vedere la [tabella 4](#table-4-main-and-backup-boot-sector-structure)). Gli agenti BIOS, MBR o di terze parti possono ispezionare questo settore e possono caricare ed eseguire tutte le istruzioni di strappo in esso contenute.

Il settore di avvio del backup è un backup del settore di avvio principale e ha la stessa struttura (vedere la [tabella 4](#table-4-main-and-backup-boot-sector-structure)). Il settore di avvio del backup può facilitare le operazioni di ripristino; Tuttavia, le implementazioni devono trattare il contenuto dei campi VolumeFlags e PercentInUse come obsoleto.

Prima di usare il contenuto del principale o del settore di avvio di backup, le implementazioni ne verificheranno il contenuto convalidando il rispettivo checksum di avvio e assicurando che tutti i relativi campi siano compresi nell'intervallo di valori validi.

Mentre l'operazione di formattazione iniziale Inizializza il contenuto dei settori di avvio principale e di backup, le implementazioni possono aggiornare questi settori (e aggiornare anche il rispettivo checksum di avvio) in base alle esigenze. Tuttavia, le implementazioni possono aggiornare i campi VolumeFlags o PercentInUse senza aggiornare il rispettivo checksum di avvio (il checksum esclude in modo specifico questi due campi).

<div id="table-4-main-and-backup-boot-sector-structure" />

**Tabella 4 struttura del settore di avvio principale e di backup**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JumpBoot</td>
<td>0</td>
<td>3</td>
<td>Questo campo è obbligatorio e la <a href="#311-jumpboot-field">sezione 3.1.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FileSystemName</td>
<td>3</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#312-filesystemname-field">sezione 3.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>MustBeZero</td>
<td>11</td>
<td>53</td>
<td>Questo campo è obbligatorio e la <a href="#313-mustbezero-field">sezione 3.1.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>PartitionOffset</td>
<td>64</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#314-partitionoffset-field">sezione 3.1.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeLength</td>
<td>72</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#315-volumelength-field">sezione 3.1.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FatOffset</td>
<td>80</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#316-fatoffset-field">sezione 3.1.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>FatLength</td>
<td>84</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#317-fatlength-field">sezione 3.1.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>ClusterHeapOffset</td>
<td>88</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#318-clusterheapoffset-field">sezione 3.1.8</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Clustercount-</td>
<td>92</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#319-clustercount-field">sezione 3.1.9</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FirstClusterOfRootDirectory</td>
<td>96</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3110-firstclusterofrootdirectory-field">sezione 3.1.10</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeSerialNumber</td>
<td>100</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3111-volumeserialnumber-field">sezione 3.1.11</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FileSystemRevision</td>
<td>104</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#3112-filesystemrevision-field">sezione 3.1.12</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeFlags</td>
<td>106</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#3113-volumeflags-field">sezione 3.1.13</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>BytesPerSectorShift</td>
<td>108</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#3114-bytespersectorshift-field">sezione 3.1.14</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SectorsPerClusterShift</td>
<td>109</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#3115-sectorsperclustershift-field">sezione 3.1.15</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>NumberOfFats</td>
<td>110</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#3116-numberoffats-field">sezione 3.1.16</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>DriveSelect</td>
<td>111</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#3117-driveselect-field">sezione 3.1.17</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>PercentInUse</td>
<td>112</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#3118-percentinuse-field">sezione 3.1.18</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>113</td>
<td>7</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="even">
<td>BootCode</td>
<td>120</td>
<td>390</td>
<td>Questo campo è obbligatorio e la <a href="#3119-bootcode-field">sezione 3.1.19</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>BootSignature</td>
<td>510</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#3120-bootsignature-field">sezione 3.1.20</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>512</td>
<td>2<sup>BytesPerSectorShift</sup> -512</td>
<td><p>Questo campo è obbligatorio e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="311-jumpboot-field"></a>3.1.1 campo JumpBoot

Il campo JumpBoot deve contenere l'istruzione Jump per le CPU comuni nei personal computer, che, quando viene eseguita, "salta" la CPU per eseguire le istruzioni di strappo nel campo BootCode.

Il valore valido per questo campo è (in ordine di byte di ordine inferiore al byte più significativo) EBh 76H 90h.

#### <a name="312-filesystemname-field"></a>3.1.2 campo FileSystemName

Il campo FileSystemName deve contenere il nome del file system nel volume.

Il valore valido per questo campo è, in caratteri ASCII, "EXFAT", che include tre spazi vuoti finali.

#### <a name="313-mustbezero-field"></a>Campo MustBeZero 3.1.3

Il campo MustBeZero deve corrispondere direttamente all'intervallo di byte utilizzato dal blocco di parametri BIOS compresso sui volumi FAT12/16/32.

Il valore valido per questo campo è 0, che consente di impedire alle implementazioni FAT12/16/32 di montare erroneamente un volume exFAT.

#### <a name="314-partitionoffset-field"></a>Campo 3.1.4 PartitionOffset

Il campo PartitionOffset descrivono l'offset del settore relativo ai supporti della partizione che ospita il volume exFAT specificato. Questo campo facilita l'avvio del volume usando INT 13h esteso nei personal computer.

Tutti i valori possibili per questo campo sono validi. Tuttavia, il valore 0 indica che le implementazioni devono ignorare questo campo.

#### <a name="315-volumelength-field"></a>Campo 3.1.5 VolumeLength

Il campo VolumeLength descrivono le dimensioni del volume exFAT specificato nei settori.

L'intervallo valido di valori per questo campo sarà:

- Almeno 2<sup>20</sup>/2<sup>BytesPerSectorShift</sup>, che garantisce che il volume minimo sia inferiore a 1 MB

- Al massimo 2<sup>64</sup>-1, il valore più grande che questo campo può descrivere

Tuttavia, se le dimensioni dell'area secondaria dello spazio in eccesso sono pari a 0, il valore di questo campo è ClusterHeapOffset + (2<sup>32</sup>-11) \* 2<sup>SectorsPerClusterShift</sup>.

#### <a name="316-fatoffset-field"></a>Campo 3.1.6 FatOffset

Il campo FatOffset descrivono l'offset di settore relativo al volume del primo FAT. Questo campo consente alle implementazioni di allineare il primo FAT alle caratteristiche del supporto di archiviazione sottostante.

L'intervallo valido di valori per questo campo sarà:

- Almeno 24, che rappresenta i settori utilizzati dalle aree di avvio principale e di avvio del backup

- Al massimo ClusterHeapOffset-(FatLength \* NumberOfFats), che rappresenta i settori utilizzati dall'heap del cluster

#### <a name="317-fatlength-field"></a>Campo 3.1.7 FatLength

Il campo FatLength descrivono la lunghezza, in settori, di ogni tabella FAT (il volume può contenere un massimo di due grassi).

L'intervallo valido di valori per questo campo sarà:

- Almeno (Clustercount-+ 2) \* 2<sup>2</sup>/2<sup>BytesPerSectorShift</sup>arrotondato per eccesso al numero intero più vicino, che garantisce che ogni Fat disponga di spazio sufficiente per la descrizione di tutti i cluster nell'heap del cluster

- Al massimo (ClusterHeapOffset-FatOffset)/NumberOfFats arrotondato per difetto al numero intero più vicino, che garantisce che i grassi esistano prima dell'heap del cluster

Questo campo può contenere un valore superiore al limite inferiore (come descritto in precedenza) per abilitare il secondo FAT, se presente, in modo da essere allineato anche alle caratteristiche del supporto di archiviazione sottostante. Il contenuto dello spazio che supera il contenuto del grasso necessario, se presente, non è definito.

#### <a name="318-clusterheapoffset-field"></a>Campo 3.1.8 ClusterHeapOffset

Il campo ClusterHeapOffset descrivono l'offset del settore relativo al volume dell'heap del cluster. Questo campo consente alle implementazioni di allineare l'heap del cluster alle caratteristiche del supporto di archiviazione sottostante.

L'intervallo valido di valori per questo campo sarà:

- Almeno FatOffset + FatLength \* NumberOfFats, per tenere conto dei settori utilizzati da tutte le aree precedenti

- Al massimo 2<sup>32</sup>-1 o VolumeLength-(Clustercount- \* 2<sup>SectorsPerClusterShift</sup>), a seconda del calcolo minore

#### <a name="319-clustercount-field"></a>Campo 3.1.9 Clustercount-

Il campo Clustercount-descrive il numero di cluster contenuti nell'heap del cluster.

Il valore valido per questo campo sarà il minore dei seguenti:

- (VolumeLength-ClusterHeapOffset)/2<sup>SectorsPerClusterShift</sup>arrotondato per difetto all'intero più vicino, che corrisponde esattamente al numero di cluster che è possibile inserire tra l'inizio dell'heap del cluster e la fine del volume

- 2<sup>32</sup>-11, ovvero il numero massimo di cluster che possono essere descritti da un fat

Il valore del campo Clustercount-determina la dimensione minima di un FAT. Per evitare grassi estremamente grandi, le implementazioni possono controllare il numero di cluster nell'heap del cluster aumentando le dimensioni del cluster (tramite il campo SectorsPerClusterShift). Questa specifica consiglia non più di 2 cluster<sup>24</sup>-2 nell'heap del cluster. Tuttavia, le implementazioni saranno in grado di gestire i volumi con un massimo di 2 cluster<sup>32</sup>-11 nell'heap del cluster.

#### <a name="3110-firstclusterofrootdirectory-field"></a>Campo 3.1.10 FirstClusterOfRootDirectory

Il campo FirstClusterOfRootDirectory deve contenere l'indice del cluster del primo cluster della directory radice. Le implementazioni devono eseguire ogni sforzo per collocare il primo cluster della directory radice nel primo cluster non danneggiato dopo che i cluster hanno utilizzato la bitmap di allocazione e la tabella del case.

L'intervallo valido di valori per questo campo sarà:

- Almeno 2, l'indice del primo cluster nell'heap del cluster

- Al massimo Clustercount-+ 1, l'indice dell'ultimo cluster nell'heap del cluster

#### <a name="3111-volumeserialnumber-field"></a>Campo 3.1.11 VolumeSerialNumber

Il campo VolumeSerialNumber deve contenere un numero di serie univoco. In questo modo, le implementazioni consentono di distinguere tra volumi exFAT diversi.
Le implementazioni devono generare il numero di serie combinando la data e l'ora di formattazione del volume exFAT. Il meccanismo per combinare data e ora per formare un numero di serie è specifico dell'implementazione.

Tutti i valori possibili per questo campo sono validi.

#### <a name="3112-filesystemrevision-field"></a>Campo 3.1.12 FileSystemRevision

Il campo FileSystemRevision descrivono i numeri di revisione principale e secondaria delle strutture exFAT nel volume specificato.

Il byte più significativo è il numero di revisione principale e il byte di ordine inferiore è il numero di revisione minore. Ad esempio, se il byte più significativo contiene il valore 01h e se il byte di ordine inferiore contiene il valore 05h, il campo FileSystemRevision descrive il numero di revisione 1,05.
Analogamente, se il byte di ordine superiore contiene il valore 0Ah e se il byte di ordine inferiore contiene il valore 0Fh, il campo FileSystemRevision descrive il numero di revisione 10,15.

L'intervallo valido di valori per questo campo sarà:

- Almeno 0 per il byte di ordine inferiore e 1 per il byte di ordine superiore

- Al massimo 99 per il byte di ordine inferiore e 99 per il byte più significativo

Il numero di revisione di exFAT descritta in questa specifica è 1,00.
Le implementazioni di questa specifica devono montare un volume exFAT con la revisione principale 1 e non devono montare alcun volume exFAT con altri numeri di revisione principali. Le implementazioni devono rispettare il numero di revisione secondaria e non devono eseguire operazioni né creare alcuna struttura di file system non descritta nella specifica corrispondente del numero di revisione secondaria specificato.

#### <a name="3113-volumeflags-field"></a>Campo 3.1.13 VolumeFlags

Il campo VolumeFlags deve contenere flag che indicano lo stato di varie strutture di file system nel volume exFAT (vedere la [tabella 5](#table-5-volumeflags-field-structure)).

Le implementazioni non includono questo campo durante il calcolo del rispettivo checksum principale dell'area di avvio o di backup. Quando si fa riferimento al settore di avvio del backup, le implementazioni devono considerare questo campo come non aggiornato.

<div id="table-5-volumeflags-field-structure" />

**Tabella 5 struttura del campo VolumeFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ActiveFat</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#31131-activefat-field">sezione 3.1.13.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>VolumeDirty</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#31132-volumedirty-field">sezione 3.1.13.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>MediaFailure</td>
<td>2</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#31133-mediafailure-field">sezione 3.1.13.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>ClearToZero</td>
<td>3</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#31134-cleartozero-field">sezione 3.1.13.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>4</td>
<td>12</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

##### <a name="31131-activefat-field"></a>Campo 3.1.13.1 ActiveFat

Il campo ActiveFat descrivono quali bitmap di allocazione e FAT sono attive (e le implementazioni utilizzeranno), come indicato di seguito:

- 0, che indica che la prima bitmap di allocazione e FAT è attiva

- 1, che indica che la seconda bitmap di allocazione FAT e Second è attiva ed è possibile solo quando il campo NumberOfFats contiene il valore 2

Le implementazioni prendono in considerazione la bitmap di allocazione e FAT inattiva come obsoleto. Solo le implementazioni compatibili con TexFAT devono cambiare le bitmap di allocazione e FAT attive (vedere la [sezione 7,1](#71-allocation-bitmap-directory-entry)).

##### <a name="31132-volumedirty-field"></a>Campo 3.1.13.2 VolumeDirty

Il campo VolumeDirty indica se il volume è modificato o meno, come indicato di seguito:

- 0, che indica che il volume è probabilmente in uno stato coerente

- 1, il che significa che il volume è probabilmente in uno stato incoerente

Le implementazioni devono impostare il valore di questo campo su 1 quando si verificano file system incoerenze dei metadati che non vengono risolte. Se, dopo il montaggio di un volume, il valore di questo campo è 1, solo le implementazioni che risolvono file system le incoerenze dei metadati potrebbero cancellare il valore di questo campo su 0. Tali implementazioni elimineranno solo il valore di questo campo su 0 dopo aver verificato che il file system sia in uno stato coerente.

Se, dopo il montaggio di un volume, il valore di questo campo è 0, le implementazioni devono impostare questo campo su 1 prima di aggiornare i metadati di file system e deselezionare il campo su 0 in seguito, in modo analogo all'ordine di scrittura consigliato descritto nella [sezione 8,1](#81-recommended-write-ordering).

##### <a name="31133-mediafailure-field"></a>Campo 3.1.13.3 MediaFailure

Il campo MediaFailure descrive se un'implementazione ha rilevato o meno errori dei supporti, come indicato di seguito:

- 0, il che significa che i supporti di hosting non hanno segnalato errori o che eventuali errori noti sono già registrati nel FAT come cluster "danneggiati"

- 1, ovvero i supporti di hosting hanno segnalato errori, ovvero le operazioni di lettura o scrittura non sono riuscite.

Un'implementazione di deve impostare questo campo su 1 quando:

1. Il supporto di hosting non riesce a eseguire tentativi di accesso a qualsiasi area del volume

2. L'implementazione ha esaurito gli algoritmi di tentativi di accesso, se presenti

Se, dopo il montaggio di un volume, il valore di questo campo è 1, le implementazioni che analizzano l'intero volume per gli errori dei supporti e registrano tutti gli errori come cluster "non corretti" nel FAT (o in caso contrario risoluzione degli errori dei supporti) potrebbero cancellare il valore di questo campo su 0.

##### <a name="31134-cleartozero-field"></a>Campo 3.1.13.4 ClearToZero

Il campo ClearToZero non ha un significato significativo in questa specifica.

I valori validi per questo campo sono:

- 0, che non ha un significato particolare

- 1, che indica che le implementazioni devono cancellare questo campo su 0 prima di modificare eventuali strutture, directory o file file system

#### <a name="3114-bytespersectorshift-field"></a>Campo 3.1.14 BytesPerSectorShift

Il campo BytesPerSectorShift descrivono i byte per settore espresso come log<sub>2</sub>(N), dove N è il numero di byte per settore. Ad esempio, per 512 byte per settore, il valore di questo campo è 9.

L'intervallo valido di valori per questo campo sarà:

- Almeno 9 (dimensioni di settore di 512 byte), ovvero il settore più piccolo possibile per un volume exFAT

- Al massimo 12 (dimensioni di settore di 4096 byte), ovvero le dimensioni della pagina di memoria delle CPU comuni nei personal computer

#### <a name="3115-sectorsperclustershift-field"></a>Campo 3.1.15 SectorsPerClusterShift

Il campo SectorsPerClusterShift descrive i settori per ogni cluster espresso come log<sub>2</sub>(n), dove N è il numero di settori per cluster. Ad esempio, per 8 settori per cluster, il valore di questo campo è 3.

L'intervallo valido di valori per questo campo sarà:

- Almeno 0 (1 settore per cluster), che è il cluster più piccolo possibile

- Al massimo 25-BytesPerSectorShift, che restituisce una dimensione del cluster di 32 MB

#### <a name="3116-numberoffats-field"></a>Campo 3.1.16 NumberOfFats

Il campo NumberOfFats descrive il numero di grassi e le bitmap di allocazione contenuti nel volume.

L'intervallo valido di valori per questo campo sarà:

- 1, che indica che il volume contiene solo la prima bitmap di allocazione FAT e FAT

- 2, che indica che il volume contiene il primo bitmap FAT, Second FAT, First allocation e la seconda bitmap di allocazione; Questo valore è valido solo per i volumi TexFAT

#### <a name="3117-driveselect-field"></a>Campo 3.1.17 DriveSelect

Il campo DriveSelect deve contenere il numero di unità 13h esteso INT, che facilita l'avvio da questo volume usando Extended INT 13h nei personal computer.

Tutti i valori possibili per questo campo sono validi. I campi simili nei file System precedenti basati su FAT contengono spesso il valore 80H.

#### <a name="3118-percentinuse-field"></a>Campo 3.1.18 PercentInUse

Il campo PercentInUse descrive la percentuale di cluster nell'heap del cluster allocati.

L'intervallo valido di valori per questo campo sarà:

- Compreso tra 0 e 100, ovvero la percentuale di cluster allocati nell'heap del cluster, arrotondati per difetto all'intero più vicino

- Esattamente FFh, che indica la percentuale di cluster allocati nell'heap del cluster non disponibile

Le implementazioni devono modificare il valore di questo campo in modo da riflettere le modifiche nell'allocazione dei cluster nell'heap del cluster o modificarlo in FFh.

Le implementazioni non includono questo campo durante il calcolo del rispettivo checksum principale dell'area di avvio o di backup. Quando si fa riferimento al settore di avvio del backup, le implementazioni devono considerare questo campo come non aggiornato.

#### <a name="3119-bootcode-field"></a>Campo 3.1.19 BootCode

Il campo BootCode deve contenere istruzioni di strappo di avvio.
Le implementazioni possono popolare questo campo con le istruzioni della CPU necessarie per l'avvio di un sistema di computer. Le implementazioni che non forniscono istruzioni di strappo di avvio devono inizializzare ogni byte in questo campo su F4h (l'istruzione Halt per le CPU comuni nei personal computer) come parte dell'operazione di formattazione.

#### <a name="3120-bootsignature-field"></a>Campo 3.1.20 BootSignature

Il campo BootSignature descrivono se lo scopo di un determinato settore è quello di essere un settore di avvio.

Il valore valido per questo campo è AA55h. Qualsiasi altro valore in questo campo invalida il rispettivo settore di avvio. Le implementazioni devono verificare il contenuto di questo campo prima di a seconda di qualsiasi altro campo nel rispettivo settore di avvio.

### <a name="32-main-and-backup-extended-boot-sectors-sub-regions"></a>3,2 settori di avvio esteso principale e di backup per aree secondarie

Ogni settore dei principali settori di avvio esteso ha la stessa struttura; Tuttavia, in ogni settore possono essere contenute istruzioni di strappo di avvio separate (vedere la tabella 6). Gli agenti di strappo, ad esempio le istruzioni di strappo nel settore di avvio principale, le implementazioni BIOS alternative o il firmware di un sistema incorporato, possono caricare questi settori ed eseguire le istruzioni che contengono.

I settori di avvio esteso di backup sono un backup dei principali settori di avvio esteso e hanno la stessa struttura (vedere la [tabella 6](#table-6-extended-boot-sector-structure)).

Prima di eseguire le istruzioni dei settori principale o di avvio esteso di backup, le implementazioni devono verificare il contenuto assicurando che il campo ExtendedBootSignature di ogni settore contenga il valore previsto.

Mentre l'operazione di formattazione iniziale Inizializza il contenuto dei settori principale e di avvio esteso di backup, le implementazioni possono aggiornare questi settori (e aggiornare anche il rispettivo checksum di avvio) in base alle esigenze.

<div id="table-6-extended-boot-sector-structure" />

**Tabella 6 struttura del settore di avvio esteso**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ExtendedBootCode</td>
<td>0</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td><p>Questo campo è obbligatorio e la <a href="#321-extendedbootcode-field">sezione 3.2.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
<tr class="even">
<td>ExtendedBootSignature</td>
<td>2<sup>BytesPerSectorShift</sup> – 4</td>
<td>4</td>
<td><p>Questo campo è obbligatorio e la <a href="#322-extendedbootsignature-field">sezione 3.2.2</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="321-extendedbootcode-field"></a>3.2.1 campo ExtendedBootCode

Il campo ExtendedBootCode deve contenere istruzioni di strappo di avvio.
Le implementazioni possono popolare questo campo con le istruzioni della CPU necessarie per l'avvio di un sistema di computer. Le implementazioni che non forniscono istruzioni di strappo di avvio devono inizializzare ogni byte in questo campo su 00h come parte dell'operazione di formattazione.

#### <a name="322-extendedbootsignature-field"></a>3.2.2 campo ExtendedBootSignature

Il campo ExtendedBootSignature descrive se lo scopo del settore specificato è quello di essere un settore di avvio esteso o meno.

Il valore valido per questo campo è AA550000h. Qualsiasi altro valore in questo campo invalida il rispettivo settore di avvio esteso principale o di backup.
Le implementazioni devono verificare il contenuto di questo campo prima di a seconda di qualsiasi altro campo nel rispettivo settore di avvio esteso.

### <a name="33-main-and-backup-oem-parameters-sub-regions"></a>3,3 parametri OEM principali e di backup per le aree secondarie

L'area secondaria dei parametri OEM principale contiene dieci strutture di parametri che possono contenere informazioni specifiche del produttore (vedere la [tabella 7](#table-7-oem-parameters-structure)). Ognuna delle dieci strutture di parametri deriva dal modello di parametri generici (vedere la [sezione 3.3.2](#332-generic-parameters-template)). I produttori possono derivare le proprie strutture di parametri personalizzati dal modello di parametri generici. Questa specifica definisce due strutture di parametri: parametri null (vedere la [sezione 3.3.3](#333-null-parameters)) e parametri flash (vedere la [sezione 3.3.4](#334-flash-parameters)).

I parametri OEM di backup sono un backup dei principali parametri OEM e hanno la stessa struttura (vedere la [tabella 7](#table-7-oem-parameters-structure)).

Prima di usare il contenuto dei parametri principali o OEM di backup, le implementazioni ne verificheranno il contenuto convalidando il rispettivo checksum di avvio.

I produttori devono popolare i parametri OEM principale e di backup con strutture di parametri personalizzate, se presenti, e qualsiasi altra struttura di parametri. Le operazioni di formato successive mantengono il contenuto dei parametri OEM principale e di backup.

Le implementazioni possono aggiornare i parametri OEM principale e di backup in base alle esigenze (e aggiornare anche il rispettivo checksum di avvio).

<div id="table-7-oem-parameters-structure" />

**Tabella 7 struttura dei parametri OEM**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Parametri [0]</td>
<td>0</td>
<td>48</td>
<td>Questo campo è obbligatorio e la <a href="#331-parameters0--parameters9">sezione 3.3.1</a> ne definisce il contenuto.</td>
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
<td>Parametri [9]</td>
<td>432</td>
<td>48</td>
<td>Questo campo è obbligatorio e la <a href="#331-parameters0--parameters9">sezione 3.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>480</td>
<td>2<sup>BytesPerSectorShift</sup> -480</td>
<td><p>Questo campo è obbligatorio e i relativi contenuti sono riservati.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="331-parameters0--parameters9"></a>3.3.1 parametri \[ 0 \] ... Parametri \[ 9\]

Ogni campo di parametri in questa matrice contiene una struttura di parametri, che deriva dal modello di parametri generici (vedere la [sezione 3.3.2](#332-generic-parameters-template)).
Qualsiasi campo dei parametri non usati deve essere descritto come contenente una struttura di parametri null (vedere la [sezione 3.3.3](#333-null-parameters)).

#### <a name="332-generic-parameters-template"></a>3.3.2 modello di parametri generici

Il modello di parametri generici fornisce la definizione di base di una struttura di parametri (vedere la [tabella 8](#table-8-generic-parameters-template)). Tutte le strutture Parameters derivano da questo modello. Il supporto per questo modello di parametri generici è obbligatorio.

<div id="table-8-generic-parameters-template" />

**Tabella 8 modello di parametri generici**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Questo campo è obbligatorio e la <a href="#3321-parametersguid-field">sezione 3.3.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>CustomDefined</td>
<td>16</td>
<td>32</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello ne definiscono il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="3321-parametersguid-field"></a>Campo 3.3.2.1 ParametersGuid

Il campo ParametersGuid descrivono un GUID, che determina il layout del resto della struttura dei parametri specificata.

Tutti i valori possibili per questo campo sono validi. Tuttavia, i costruttori devono usare uno strumento di generazione GUID, ad esempio GuidGen.exe, per selezionare un GUID quando si derivano le strutture di parametri personalizzati da questo modello.

#### <a name="333-null-parameters"></a>3.3.3 parametri null

La struttura di parametri null deriva dal modello di parametri generici (vedere la [sezione 3.3.2](#332-generic-parameters-template)) e descrivono un campo di parametri non usati (vedere la [tabella 9](#table-9-null-parameters-structure)). Quando si crea o si aggiorna la struttura dei parametri OEM, le implementazioni devono popolare i campi dei parametri non utilizzati con la struttura dei parametri null. Inoltre, quando si crea o si aggiorna la struttura dei parametri OEM, le implementazioni devono consolidare le strutture di parametri null alla fine della matrice, lasciando in tal modo tutte le altre strutture di parametri all'inizio della struttura dei parametri OEM.

Il supporto per la struttura di parametri null è obbligatorio.

<div id="table-9-null-parameters-structure" />

**Struttura di parametri null della tabella 9**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Questo campo è obbligatorio e la <a href="#3331-parametersguid-field">sezione 3.3.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>16</td>
<td>32</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

##### <a name="3331-parametersguid-field"></a>Campo 3.3.3.1 ParametersGuid

Il campo ParametersGuid deve essere conforme alla definizione fornita dal modello di parametri generici (vedere la [sezione 3.3.2.1](#3321-parametersguid-field)).

Il valore valido per questo campo, nella notazione GUID, è {00000000-0000-0000-0000-000000000000} .

#### <a name="334-flash-parameters"></a>Parametri flash 3.3.4

La struttura del parametro Flash deriva dal modello di parametri generici (vedere la [sezione 3.3.2](#332-generic-parameters-template)) e contiene i parametri per i supporti Flash (vedere la [tabella 10](#table-10-flash-parameters-structure)). I produttori di dispositivi di archiviazione basati su Flash possono popolare un campo parametri (preferibilmente il \[ campo parametri 0 \] ) con questa struttura di parametri. Le implementazioni possono usare le informazioni nella struttura dei parametri flash per ottimizzare le operazioni di accesso durante le operazioni di lettura/scrittura e per l'allineamento delle strutture file system Durning la formattazione dei supporti.

Il supporto per la struttura dei parametri flash è facoltativo.

<div id="table-10-flash-parameters-structure" />

**Tabella 10 struttura dei parametri flash**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ParametersGuid</td>
<td>0</td>
<td>16</td>
<td>Questo campo è obbligatorio e la <a href="#3341-parametersguid-field">sezione 3.3.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>EraseBlockSize</td>
<td>16</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3342-eraseblocksize-field">sezione 3.3.4.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>PageSize</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3343-pagesize-field">sezione 3.3.4.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SpareSectors</td>
<td>24</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3344-sparesectors-field">sezione 3.3.4.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>RandomAccessTime</td>
<td>28</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3345-randomaccesstime-field">sezione 3.3.4.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>ProgrammingTime</td>
<td>32</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3346-programmingtime-field">sezione 3.3.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>ReadCycle</td>
<td>36</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3347-readcycle-field">sezione 3.3.4.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>WriteCycle</td>
<td>40</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#3348-writecycle-field">sezione 3.3.4.8</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>44</td>
<td>4</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

Tutti i valori possibili per tutti i campi dei parametri flash, ad eccezione del campo ParametersGuid, sono validi. Tuttavia, il valore 0 indica che il campo è effettivamente privo di significato (le implementazioni ignoreranno il campo specificato).

##### <a name="3341-parametersguid-field"></a>Campo 3.3.4.1 ParametersGuid

Il campo ParametersGuid deve essere conforme alla definizione fornita nel modello di parametri generici (vedere la [sezione 3.3.2.1](#3321-parametersguid-field)).

Il valore valido per questo campo, nella notazione GUID, è {0A0C7E46-3399-4021-90C8-FA6D389C4BA2}.

##### <a name="3342-eraseblocksize-field"></a>Campo 3.3.4.2 EraseBlockSize

Il campo EraseBlockSize descrive le dimensioni, in byte, del blocco Erase del supporto Flash.

##### <a name="3343-pagesize-field"></a>3.3.4.3 campo PageSize

Il campo PageSize descrive le dimensioni, in byte, della pagina del supporto Flash.

##### <a name="3344-sparesectors-field"></a>Campo 3.3.4.4 SpareSectors

Il campo SpareSectors descrive il numero di settori che i supporti flash sono disponibili per le operazioni di disuguaglianza interne.

##### <a name="3345-randomaccesstime-field"></a>Campo 3.3.4.5 RandomAccessTime

Il campo RandomAccessTime descrive il tempo medio di accesso casuale dei supporti flash, in nanosecondi.

##### <a name="3346-programmingtime-field"></a>Campo 3.3.4.6 ProgrammingTime

Il campo ProgrammingTime descrive il tempo medio di programmazione dei supporti flash, in nanosecondi.

##### <a name="3347-readcycle-field"></a>Campo 3.3.4.7 ReadCycle

Il campo ReadCycle descrive il tempo medio di lettura del flash media, in nanosecondi.

##### <a name="3348-writecycle-field"></a>Campo 3.3.4.8 WriteCycle

Il campo WriteCycle descrive la durata media del ciclo di scrittura, in nanosecondi.

### <a name="34-main-and-backup-boot-checksum-sub-regions"></a>3,4 sottoaree di checksum di avvio principale e backup

I checksum di avvio principale e di backup contengono ciascuno un modello ripetuto del checksum di quattro byte del contenuto di tutte le altre aree secondarie nelle rispettive aree di avvio. Il calcolo del checksum non deve includere i campi VolumeFlags e PercentInUse nel rispettivo settore di avvio (vedere la [Figura 1](#figure-1-boot-checksum-computation)). Il modello ripetuto del checksum a quattro byte riempie la rispettiva area secondaria di checksum di avvio dall'inizio alla fine dell'area secondaria.

Prima di usare il contenuto di una delle altre aree secondarie nelle aree principale o di avvio di backup, le implementazioni ne verificheranno il contenuto convalidando il rispettivo checksum di avvio.

Mentre l'operazione di formattazione iniziale compilerà sia i checksum di avvio principale che quelli di backup con il modello di checksum ripetuto, le implementazioni dovranno aggiornare questi settori come il contenuto degli altri settori nelle rispettive aree di avvio cambiano.

<div id="figure-1-boot-checksum-computation" />

**Figura 1 calcolo del checksum di avvio**

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

## <a name="4-file-allocation-table-region"></a>4 area tabella di allocazione file

L'area della tabella di allocazione file (FAT) può contenere fino a due grassi, una nella prima area secondaria FAT e un'altra nella seconda area FAT.
Il campo NumberOfFats descrive il numero di grassi contenuti in questa area. I valori validi per il campo NumberOfFats sono 1 e 2. Pertanto, la prima area secondaria FAT contiene sempre un valore FAT. Se il campo NumberOfFats è due, la seconda area secondaria FAT contiene anche un valore FAT.

Il campo ActiveFat del campo VolumeFlags descrive il FAT attivo. Solo il campo VolumeFlags nel settore di avvio principale è corrente.
Le implementazioni devono trattare il FAT, che non è attivo come obsoleto. L'utilizzo del grasso inattivo e il cambio tra i grassi sono specifici dell'implementazione.

### <a name="41-first-and-second-fat-sub-regions"></a>4,1 prime e seconde aree secondarie FAT

Un FAT descriva le catene del cluster nell'heap del cluster (vedere la [tabella 11](#table-11-file-allocation-table-structure)).
Una catena di cluster è una serie di cluster che fornisce spazio per la registrazione del contenuto di file, directory e altre strutture di file system. Un FAT rappresenta una catena di cluster come un elenco collegato singolarmente di indici cluster. Fatta eccezione per le prime due voci, ogni voce di un valore FAT rappresenta esattamente un cluster.

<div id="table-11-file-allocation-table-structure" />

**Tabella 11 struttura della tabella di allocazione file**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FatEntry [0]</td>
<td>0</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#412-fatentry1-field">sezione 4.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FatEntry [1]</td>
<td>4</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#412-fatentry1-field">sezione 4.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>FatEntry [2]</td>
<td>8</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#413-fatentry2--fatentryclustercount1-fields">sezione 4.1.3</a> ne definisce il contenuto.</td>
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
<td>FatEntry [Clustercount-+ 1]</td>
<td>(Clustercount-+ 1) * 4</td>
<td>4</td>
<td><p>Questo campo è obbligatorio e la <a href="#413-fatentry2--fatentryclustercount1-fields">sezione 4.1.3</a> ne definisce il contenuto.</p>
<p>Clustercount-+ 1 non può mai superare FFFFFFF6h.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo Clustercount-.</p></td>
</tr>
<tr class="even">
<td>ExcessSpace</td>
<td>(Clustercount-+ 2) * 4</td>
<td>(FatLength * 2<sup>BytesPerSectorShift</sup>) – ((clustercount-+ 2) * 4)</td>
<td><p>Questo campo è obbligatorio e il relativo contenuto, se presente, non è definito.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi Clustercount-, FatLength e BytesPerSectorShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="411-fatentry0-field"></a>4.1.1 FatEntry \[ \] campo 0

Il \[ campo FatEntry 0 \] descrive il tipo di supporto nel primo byte (il byte di ordine più basso) e deve contenere FFH nei tre byte rimanenti.

Il tipo di supporto (il primo byte) dovrebbe essere F8h.

#### <a name="412-fatentry1-field"></a>4.1.2 \[ campo FatEntry 1 \]

Il \[ campo FatEntry 1 \] esiste solo a causa della precedenza cronologica e non descrive alcunché di interesse.

Il valore valido per questo campo è FFFFFFFFh. Le implementazioni devono inizializzare questo campo sul valore prescritto e non devono utilizzare questo campo per alcuno scopo. Le implementazioni non devono interpretare questo campo e conservarne il contenuto tra le operazioni che modificano i campi circostanti.

#### <a name="413-fatentry2--fatentryclustercount1-fields"></a>4.1.3 FatEntry \[ 2 \] ... \[Campi FatEntry clustercount-+ 1 \]

Ogni campo FatEntry in questa matrice deve rappresentare un cluster nell'heap del cluster. FatEntry \[ 2 \] rappresenta il primo cluster nell'heap del cluster e FatEntry \[ clustercount-+ 1 \] rappresenta l'ultimo cluster nell'heap del cluster.

L'intervallo valido di valori per questi campi deve essere:

- Compreso tra 2 e Clustercount-+ 1, incluso, che punta al FatEntry successivo nella catena del cluster specificata; il FatEntry specificato non deve puntare a nessun FatEntry che lo precede nella catena di cluster specificata

- Esattamente FFFFFFF7h, che contrassegna il cluster corrispondente del FatEntry specificato come "non valido"

- Esattamente FFFFFFFFh, che contrassegna il cluster corrispondente del FatEntry specificato come ultimo cluster di una catena di cluster. Questo è l'unico valore valido per l'ultimo FatEntry di una determinata catena di cluster

## <a name="5-data-region"></a>5 area dati

L'area dati contiene l'heap del cluster, che fornisce lo spazio gestito per le strutture, le directory e i file di file system.

### <a name="51-cluster-heap-sub-region"></a>area secondaria heap cluster 5,1

La struttura dell'heap del cluster è molto semplice (vedere la [tabella 12](#table-12-cluster-heap-structure)); ogni serie consecutiva di settori descrive un cluster, come definito dal campo SectorsPerClusterShift. In particolare, il primo cluster dell'heap del cluster ha l'indice Two, che corrisponde direttamente all'indice di FatEntry \[ 2 \] .

In un volume exFAT, una bitmap di allocazione (vedere la [sezione 7.1.5](#715-allocation-bitmap)) mantiene il record dello stato di allocazione di tutti i cluster. Si tratta di una differenza significativa rispetto ai predecessori di exFAT (FAT12, FAT16 e FAT32), in cui un FAT ha mantenuto un record dello stato di allocazione di tutti i cluster nell'heap del cluster.

<div id="table-12-cluster-heap-structure" />

**Tabella 12 struttura dell'heap del cluster**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>settore</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>settori</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cluster [2]</td>
<td>ClusterHeapOffset</td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Questo campo è obbligatorio e la <a href="#511-cluster2--clusterclustercount1-fields">sezione 5.1.1</a> ne definisce il contenuto.</p>
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
<td>Cluster [Clustercount-+ 1]</td>
<td>ClusterHeapOffset + (Clustercount--1) * 2<sup>SectorsPerClusterShift</sup></td>
<td>2<sup>SectorsPerClusterShift</sup></td>
<td><p>Questo campo è obbligatorio e la <a href="#511-cluster2--clusterclustercount1-fields">sezione 5.1.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi i campi Clustercount-, ClusterHeapOffset e SectorsPerClusterShift.</p></td>
</tr>
</tbody>
</table>

#### <a name="511-cluster2--clusterclustercount1-fields"></a>5.1.1 cluster \[ 2 \] ... Campi del cluster \[ clustercount-+ 1 \]

Ogni campo del cluster in questa matrice è costituito da una serie di settori contigui, le cui dimensioni sono definite dal campo SectorsPerClusterShift.

## <a name="6-directory-structure"></a>6 struttura di directory

Il file system exFAT usa un approccio ad albero di directory per gestire le strutture file system e i file presenti nell'heap del cluster. Le directory hanno una relazione uno-a-molti tra padre e figlio nell'albero di directory.

La directory a cui si riferisce il campo FirstClusterOfRootDirectory è la radice dell'albero di directory. Tutte le altre directory discendono dalla directory radice in un modo collegato singolarmente.

Ogni directory è costituita da una serie di voci di directory (vedere la [tabella 13](#table-13-directory-structure)).

Una o più voci di directory vengono combinate in un set di voci di directory che descrive un elemento interessante, ad esempio una struttura file system, una sottodirectory o un file.

<div id="table-13-directory-structure" />

**Tabella 13 struttura di directory**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DirectoryEntry [0]</td>
<td>0</td>
<td>32</td>
<td>Questo campo è obbligatorio e la <a href="#61-directoryentry0--directoryentryn--1">sezione 6,1</a> ne definisce il contenuto.</td>
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
<td>DirectoryEntry [N-1]</td>
<td>(N-1) * 32</td>
<td>32</td>
<td><p>Questo campo è obbligatorio e la <a href="#61-directoryentry0--directoryentryn--1">sezione 6,1</a> ne definisce il contenuto.</p>
<p>N, il numero di campi DirectoryEntry è la dimensione, in byte, della catena di cluster che contiene la directory specificata, divisa per la dimensione di un campo DirectoryEntry, 32 byte.</p></td>
</tr>
</tbody>
</table>

### <a name="61-directoryentry0--directoryentryn--1"></a>6,1 DirectoryEntry \[ 0 \] ... DirectoryEntry \[ N--1\]

Ogni campo DirectoryEntry in questa matrice deriva dal modello generico DirectoryEntry (vedere la [sezione 6,2](#62-generic-directoryentry-template)).

### <a name="62-generic-directoryentry-template"></a>6,2 modello DirectoryEntry generico

Il modello generico DirectoryEntry fornisce la definizione di base per le voci di directory (vedere la [tabella 14](#table-14-generic-directoryentry-template)). Tutte le strutture di immissione di directory derivano da questo modello e sono valide solo le strutture di immissione di directory definite da Microsoft (exFAT non contiene disposizioni per le strutture di immissione di directory definite dal produttore, tranne come definito nella [sezione 7,8](#78-vendor-extension-directory-entry) e [7,9](#79-vendor-allocation-directory-entry)). La possibilità di interpretare il modello generico DirectoryEntry è obbligatoria.

<div id="table-14-generic-directoryentry-template" />

**Tabella 14 modello di DirectoryEntry generico**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#621-entrytype-field">sezione 6.2.1</a> ne definisce il contenuto.</td>
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
<td>Questo campo è obbligatorio e la <a href="#622-firstcluster-field">sezione 6.2.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#623-datalength-field">sezione 6.2.3</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="621-entrytype-field"></a>6.2.1 campo EntryType

Il campo EntryType dispone di tre modalità di utilizzo che definiscono il valore del campo (vedere l'elenco riportato di seguito).

- 00h, ovvero un marcatore di fine directory e si applicano le condizioni seguenti:

  - Tutti gli altri campi nel determinato DirectoryEntry sono effettivamente riservati

  - Anche tutte le voci di directory successive nella directory specificata sono marcatori di fine directory

  - I marcatori di fine directory sono validi solo all'esterno dei set di voci di directory

  - Le implementazioni possono sovrascrivere i marcatori di fine directory se necessario

- Compreso tra 01h e 7Fh, ovvero un marcatore di voce di directory inutilizzata e si applicano le condizioni seguenti:

  - Tutti gli altri campi nell'oggetto DirectoryEntry specificato non sono effettivamente definiti

  - Le voci di directory inutilizzate sono valide solo all'esterno dei set di voci di directory

  - Le implementazioni possono sovrascrivere le voci di directory inutilizzate se necessario

  - Questo intervallo di valori corrisponde al campo InUse (vedere la [sezione 6.2.1.4](#6214-inuse-field)) che contiene il valore 0

- Compreso tra 81h e FFh, ovvero una voce di directory normale e si applicano le condizioni seguenti:

  - Il contenuto del campo EntryType (vedere la [tabella 15](#table-15-generic-entrytype-field-structure)) determina il layout della parte restante della struttura DirectoryEntry

  - Questo intervallo di valori e solo questo intervallo di valori sono validi all'interno di un set di voci di directory

  - Questo intervallo di valori corrisponde direttamente al campo InUse (vedere la [sezione 6.2.1.4](#6214-inuse-field)) che contiene il valore 1

Per evitare modifiche al campo InUse (vedere la [sezione 6.2.1.4](#6214-inuse-field)) che causa erroneamente un marcatore di fine directory, il valore 80H non è valido.

<div id="table-15-generic-entrytype-field-structure" />

**Tabella 15 struttura di campo EntryType generica**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TypeCode</td>
<td>0</td>
<td>5</td>
<td>Questo campo è obbligatorio e la <a href="#6211-typecode-field">sezione 6.2.1.1</a> ne definisce il contenuto.</td>
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
<td>Questo campo è obbligatorio e la <a href="#6213-typecategory-field">sezione 6.2.1.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>InUse</td>
<td>7</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#6214-inuse-field">sezione 6.2.1.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="6211-typecode-field"></a>Campo TypeCode 6.2.1.1

Il campo TypeCode descrive parzialmente il tipo specifico della voce di directory specificata. Questo campo, più i campi TypeImportance e TypeCategory (vedere rispettivamente la [sezione 6.2.1.2](#6212-typeimportance-field) e la [sezione 6.2.1.3](#6213-typecategory-field)) identificano in modo univoco il tipo della voce di directory specificata.

Tutti i valori possibili di questo campo sono validi, a meno che i campi TypeImportance e TypeCategory contengano entrambi il valore 0; in tal caso, il valore 0 non è valido per questo campo.

##### <a name="6212-typeimportance-field"></a>Campo 6.2.1.2 TypeImportance

Il campo TypeImportance descrivono l'importanza della voce di directory specificata.

I valori validi per questo campo saranno:

- 0, che indica che la voce di directory specificata è critica (vedere la [sezione 6.3.1.2.1](#63121-critical-primary-directory-entries) e la [sezione 6.4.1.2.1](#64121-critical-secondary-directory-entries) per le voci di directory secondarie critiche e primarie, rispettivamente)

- 1, il che significa che la voce di directory specificata è benigna (vedere la [sezione 6.3.1.2.2](#63122-benign-primary-directory-entries) e la [sezione 6.4.1.2.2](#64122-benign-secondary-directory-entries) rispettivamente per le voci di directory secondarie benigne e secondarie benigne)

##### <a name="6213-typecategory-field"></a>Campo 6.2.1.3 TypeCategory

Il campo TypeCategory descrivono la categoria della voce di directory specificata.

I valori validi per questo campo saranno:

- 0, che indica che la voce di directory specificata è primaria (vedere la [sezione 6,3](#63-generic-primary-directoryentry-template))

- 1, che indica che la voce di directory specificata è secondaria (vedere la [sezione 6,4](#64-generic-secondary-directoryentry-template))

##### <a name="6214-inuse-field"></a>Campo 6.2.1.4 InUse

Il campo InUse descrive se la voce di directory specificata è in uso o meno.

I valori validi per questo campo saranno:

- 0, che indica che la voce di directory specificata non è in uso. Ciò significa che la struttura specificata è effettivamente una voce di directory inutilizzata

- 1, che indica che la voce di directory specificata è in uso. Ciò significa che la struttura specificata è una voce di directory normale

#### <a name="622-firstcluster-field"></a>6.2.2 campo FirstCluster

Il campo FirstCluster deve contenere l'indice del primo cluster di un'allocazione nell'heap del cluster associato alla voce di directory specificata.

L'intervallo valido di valori per questo campo sarà:

- Esattamente 0, che significa che non esiste alcuna allocazione cluster

- Compreso tra 2 e Clustercount-+ 1, ovvero l'intervallo di indici cluster validi

Le strutture che derivano da questo modello possono ridefinire i campi FirstCluster e DATALENGTH se un'allocazione del cluster non è compatibile con la struttura derivata.

#### <a name="623-datalength-field"></a>6.2.3-campo DataLength

Il campo DATALENGTH descrive le dimensioni, in byte, dei dati contenuti nell'allocazione cluster associata.

L'intervallo valido di valori per questo campo è:

- Almeno 0; Se il campo FirstCluster contiene il valore 0, l'unico valore valido di questo campo è 0

- Al massimo Clustercount- \* 2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>

Le strutture che derivano da questo modello possono ridefinire i campi FirstCluster e DATALENGTH, se non è possibile allocare un cluster per la struttura derivata.

### <a name="63-generic-primary-directoryentry-template"></a>6,3 modello DirectoryEntry primario generico

La prima voce di directory in un set di voci di directory deve essere una voce di directory primaria. Tutte le eventuali voci di directory successive nel set di voci di directory saranno voci di directory secondarie (vedere la [sezione 6,4](#64-generic-secondary-directoryentry-template)).

La possibilità di interpretare il modello DirectoryEntry primario generico è obbligatoria.

Tutte le strutture di immissione di directory primarie derivano dal modello DirectoryEntry primario generico (vedere la [tabella 16](#table-16-generic-primary-directoryentry-template)), che deriva dal modello generico DirectoryEntry (vedere la [sezione 6,2](#62-generic-directoryentry-template)).

<div id="table-16-generic-primary-directoryentry-template" />

**Tabella 16 modello DirectoryEntry primario generico**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#631-entrytype-field">sezione 6.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#632-secondarycount-field">sezione 6.3.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#633-setchecksum-field">sezione 6.3.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#634-generalprimaryflags-field">sezione 6.3.4</a> ne definisce il contenuto.</td>
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
<td>Questo campo è obbligatorio e la <a href="#635-firstcluster-field">sezione 6.3.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#636-datalength-field">sezione 6.3.6</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="631-entrytype-field"></a>Campo 6.3.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1](#621-entrytype-field)).

##### <a name="6311-typecode-field"></a>Campo TypeCode 6.3.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.1](#6211-typecode-field)).

##### <a name="6312-typeimportance-field"></a>Campo 6.3.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.2](#6212-typeimportance-field)).

###### <a name="63121-critical-primary-directory-entries"></a>6.3.1.2.1 le voci di directory primarie critiche

Le voci di directory primarie critiche contengono informazioni cruciali per la corretta gestione di un volume exFAT. Solo la directory radice contiene voci di directory primarie critiche (le voci della directory di file sono un'eccezione, vedere la [sezione 7,4](#74-file-directory-entry)).

La definizione delle voci di directory primarie critiche è correlata al numero di revisione principale di exFAT. Le implementazioni devono supportare tutte le voci di directory primarie critiche e devono registrare solo le strutture di voci di directory primarie critiche definite da questa specifica.

###### <a name="63122-benign-primary-directory-entries"></a>6.3.1.2.2 le voci di directory primarie benigne

Le voci di directory primarie benigne contengono informazioni aggiuntive che possono essere utili per la gestione di un volume exFAT. Qualsiasi directory può contenere voci di directory primarie benigne.

La definizione di voci di directory primarie benigne è correlata al numero di revisione exFAT secondario. Supporto per qualsiasi voce di directory primaria benigna questa specifica, o qualsiasi specifica successiva, definisce è facoltativa. Una voce di directory primaria benigna non riconosciuta esegue il rendering dell'intero set di voci di directory come non riconosciuto (oltre alla definizione dei modelli di immissione di directory applicabili).

##### <a name="6313-typecategory-field"></a>Campo 6.3.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.3](#6213-typecategory-field)).

Per questo modello, il valore valido per questo campo sarà 0.

##### <a name="6314-inuse-field"></a>Campo 6.3.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.4](#6214-inuse-field)).

#### <a name="632-secondarycount-field"></a>Campo 6.3.2 SecondaryCount

Il campo SecondaryCount descrive il numero di voci della directory secondaria che seguono immediatamente la voce della directory primaria specificata. Queste voci della directory secondaria, insieme alla voce di directory primaria specificata, costituiscono il set di voci di directory.

L'intervallo valido di valori per questo campo sarà:

- Almeno 0, che indica che questa voce di directory primaria è l'unica voce nel set di voci di directory

- Al massimo 255, che indica le successive voci di directory 255 e questa voce di directory primaria comprende il set di voci di directory

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire i campi SecondaryCount e sechequer.

#### <a name="633-setchecksum-field"></a>6.3.3 (campo di controllo)

Il campo del controllo di accesso deve contenere il checksum di tutte le voci di directory nel set di voci di directory specificato. Tuttavia, il checksum esclude questo campo (vedere la [Figura 2](#figure-2-entrysetchecksum-computation)). Le implementazioni devono verificare che il contenuto di questo campo sia valido prima di utilizzare qualsiasi altra voce di directory nel set di voci di directory specificato.

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire i campi SecondaryCount e sechequer.

<div id="figure-2-entrysetchecksum-computation" />

**Figura 2 calcolo di EntrySetChecksum**

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

#### <a name="634-generalprimaryflags-field"></a>Campo 6.3.4 GeneralPrimaryFlags

Il campo GeneralPrimaryFlags contiene flag (vedere la [tabella 17](#table-17-generic-generalprimaryflags-field-structure)).

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire questo campo.

<div id="table-17-generic-generalprimaryflags-field-structure" />

**Tabella 17 struttura di campo GeneralPrimaryFlags generica**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#6341-allocationpossible-field">sezione 6.3.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#6342-nofatchain-field">sezione 6.3.4.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>14</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello possono definire questo campo.</td>
</tr>
</tbody>
</table>

##### <a name="6341-allocationpossible-field"></a>Campo 6.3.4.1 AllocationPossible

Il campo AllocationPossible deve indicare se è possibile o meno un'allocazione nell'heap del cluster per la voce di directory specificata.

I valori validi per questo campo saranno:

- 0, ovvero un'allocazione associata di cluster non è possibile e i campi FirstCluster e DATALENGTH sono effettivamente non definiti (le strutture che derivano da questo modello possono ridefinire tali campi)

- 1, il che significa che è possibile allocare un cluster associato e che i campi FirstCluster e DATALENGTH sono definiti

##### <a name="6342-nofatchain-field"></a>Campo 6.3.4.2 NoFatChain

Il campo NoFatChain indicherà se il FAT attivo descrive la catena di cluster dell'allocazione specificata.

I valori validi per questo campo saranno:

- 0, che indica che le voci FAT corrispondenti per la catena di cluster dell'allocazione sono valide e le implementazioni devono interpretarle; Se il campo AllocationPossible contiene il valore 0 oppure se il campo AllocationPossible contiene il valore 1 e il campo FirstCluster contiene il valore 0, il valore valido di questo campo è 0

- 1, il che significa che l'allocazione associata è una serie contigua di cluster. le voci FAT corrispondenti per i cluster non sono valide e le implementazioni non le interpretano; le implementazioni possono usare l'equazione seguente per calcolare le dimensioni dell'allocazione associata: DataLength/(2<sup>SectorsPerClusterShift</sup> \* 2<sup>BytesPerSectorShift</sup>) arrotondate per eccesso al numero intero più vicino

Se le strutture di voci di directory primarie critiche che derivano da questo modello ridefiniscono il campo GeneralPrimaryFlags, le voci FAT corrispondenti per la catena di cluster di allocazione associata sono valide.

#### <a name="635-firstcluster-field"></a>Campo 6.3.5 FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.2](#622-firstcluster-field)).

Se il bit NoFatChain è 1, FirstCluster deve puntare a un cluster valido nell'heap del cluster.

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire i campi FirstCluster e DATALENGTH. Altre strutture che derivano da questo modello possono ridefinire i campi FirstCluster e DATALENGTH solo se il campo AllocationPossible contiene il valore 0.

#### <a name="636-datalength-field"></a>6.3.6-campo DataLength

Il campo DATALENGTH deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.3](#623-datalength-field)).

Se il bit NoFatChain è 1, DATALENGTH non deve essere zero. Se il campo FirstCluster è zero, anche DATALENGTH deve essere zero.

Le strutture di voci di directory primarie critiche che derivano da questo modello possono ridefinire i campi FirstCluster e DATALENGTH. Altre strutture che derivano da questo modello possono ridefinire i campi FirstCluster e DATALENGTH solo se il campo AllocationPossible contiene il valore 0.

### <a name="64-generic-secondary-directoryentry-template"></a>6,4 modello DirectoryEntry secondario generico

Lo scopo principale delle voci della directory secondaria è fornire informazioni aggiuntive su un set di voci di directory. La possibilità di interpretare il modello DirectoryEntry secondario generico è obbligatoria.

La definizione di voci di directory secondarie critiche e benigne è correlata al numero di revisione exFAT secondario. Supporto per qualsiasi voce di directory secondaria critica o benigna questa specifica o le specifiche successive, definisce è facoltativa.

Tutte le strutture di voci di directory secondarie derivano dal modello di DirectoryEntry secondario generico (vedere la [tabella 18](#table-18-generic-secondary-directoryentry-template)), che deriva dal modello generico DirectoryEntry (vedere la [sezione 6,2](#62-generic-directoryentry-template)).

<div id="table-18-generic-secondary-directoryentry-template" />

**Tabella 18 modello DirectoryEntry secondario generico**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#641-entrytype-field">sezione 6.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#642-generalsecondaryflags-field">sezione 6.4.2</a> ne definisce il contenuto.</td>
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
<td>Questo campo è obbligatorio e la <a href="#643-firstcluster-field">sezione 6.4.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#644-datalength-field">sezione 6.4.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="641-entrytype-field"></a>Campo 6.4.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1](#621-entrytype-field))

##### <a name="6411-typecode-field"></a>Campo TypeCode 6.4.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.1](#6211-typecode-field)).

##### <a name="6412-typeimportance-field"></a>Campo 6.4.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.2](#6212-typeimportance-field)).

###### <a name="64121-critical-secondary-directory-entries"></a>6.4.1.2.1 voci di directory secondarie critiche

Le voci di directory secondarie critiche contengono informazioni cruciali per la corretta gestione del set di voci di directory che lo contiene.
Sebbene il supporto per una voce di directory secondaria critica specifica sia facoltativo, una voce di directory critica non riconosciuta esegue il rendering dell'intero set di voci di directory come non riconosciuto (oltre alla definizione dei modelli di immissione di directory applicabili).

Tuttavia, se un set di voci di directory contiene almeno una voce di directory secondaria critica che non viene riconosciuta da un'implementazione, l'implementazione deve interpretare al massimo i modelli delle voci di directory nel set di voci della directory e non i dati di allocazione associata a una voce di directory nel set di voci di directory contiene (le voci della directory di file sono un'eccezione, vedere la [sezione 7,4](#74-file-directory-entry)

###### <a name="64122-benign-secondary-directory-entries"></a>6.4.1.2.2 le voci di directory secondarie benigne

Le voci di directory secondarie benigne contengono informazioni aggiuntive che possono essere utili per la gestione del set di voci di directory che lo contiene. Il supporto per qualsiasi voce di directory secondaria benigna specifica è facoltativo.
Le voci di directory secondarie benigne non riconosciute non eseguono il rendering dell'intero set di voci di directory come non riconosciuto.

Le implementazioni possono ignorare qualsiasi voce secondaria benigna che non riconosce.

##### <a name="6413-typecategory-field"></a>Campo 6.4.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.3](#6213-typecategory-field)).

Per questo modello, il valore valido per questo campo è 1.

##### <a name="6414-inuse-field"></a>Campo 6.4.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.1.4](#6214-inuse-field)).

#### <a name="642-generalsecondaryflags-field"></a>Campo 6.4.2 GeneralSecondaryFlags

Il campo GeneralSecondaryFlags contiene flag (vedere la [tabella 19](#table-19-generic-generalsecondaryflags-field-structure)).

<div id="table-19-generic-generalsecondaryflags-field-structure" />

**Tabella 19 struttura di campo GeneralSecondaryFlags generica**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllocationPossible</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#6421-allocationpossible-field">sezione 6.4.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>NoFatChain</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#6422-nofatchain-field">sezione 6.4.2.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CustomDefined</td>
<td>2</td>
<td>6</td>
<td>Questo campo è obbligatorio e le strutture che derivano da questo modello possono definire questo campo.</td>
</tr>
</tbody>
</table>

##### <a name="6421-allocationpossible-field"></a>Campo 6.4.2.1 AllocationPossible

Il campo AllocationPossible deve avere la stessa definizione del campo con lo stesso nome nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.4.1](#6341-allocationpossible-field).

##### <a name="6422-nofatchain-field"></a>Campo 6.4.2.2 NoFatChain

Il campo NoFatChain deve avere la stessa definizione del campo con lo stesso nome nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.4.2](#6342-nofatchain-field).

#### <a name="643-firstcluster-field"></a>Campo 6.4.3 FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.2](#622-firstcluster-field)).

Se il bit NoFatChain è 1, FirstCluster deve puntare a un cluster valido nell'heap del cluster.

#### <a name="644-datalength-field"></a>6.4.4-campo DataLength

Il campo DATALENGTH deve essere conforme alla definizione fornita nel modello generico DirectoryEntry (vedere la [sezione 6.2.3](#623-datalength-field)).

Se il bit NoFatChain è 1, DATALENGTH non deve essere zero. Se il campo FirstCluster è zero, anche DATALENGTH deve essere zero.

## <a name="7-directory-entry-definitions"></a>7 definizioni voce di directory

La revisione 1,00 della file system exFAT definisce le voci di directory seguenti:

- Primario critico

  - Bitmap di allocazione ([sezione 7,1](#71-allocation-bitmap-directory-entry))

  - Tabella del case ([sezione 7,2](#72-up-case-table-directory-entry))

  - Etichetta volume ([sezione 7,3](#73-volume-label-directory-entry))

  - File ([sezione 7,4](#74-file-directory-entry))

- Primario benigno

  - GUID volume ([sezione 7,5](#75-volume-guid-directory-entry))

  - Riempimento TexFAT ([sezione 7,10](#710-texfat-padding-directory-entry))

<!-- -->

- Secondario critico

  - Estensione di flusso ([sezione 7,6](#76-stream-extension-directory-entry))

  - Nome file ([sezione 7,7](#77-file-name-directory-entry))

- Secondario benigno

  - Estensione fornitore ([sezione 7,8](#78-vendor-extension-directory-entry))

  - Allocazione fornitore ([sezione 7,9](#79-vendor-allocation-directory-entry))

### <a name="71-allocation-bitmap-directory-entry"></a>7,1 voce di directory bitmap di allocazione

Nel file system exFAT, un FAT non descrive lo stato di allocazione dei cluster. piuttosto, una bitmap di allocazione. Le bitmap di allocazione sono disponibili nell'heap del cluster (vedere la [sezione 7.1.5](#715-allocation-bitmap)) e hanno voci di directory primarie critiche corrispondenti nella directory radice (vedere la [tabella 20](#table-20-allocation-bitmap-directoryentry-structure)).

Il campo NumberOfFats determina il numero di voci della directory bitmap di allocazione valide nella directory radice. Se il campo NumberOfFats contiene il valore 1, l'unico numero valido di voci della directory bitmap di allocazione è 1. Inoltre, la voce della directory di una bitmap di allocazione è valida solo se descrive la prima bitmap di allocazione (vedere la [sezione 7.1.2.1](#7121-bitmapidentifier-field)). Se il campo NumberOfFats contiene il valore 2, l'unico numero valido di voci della directory bitmap di allocazione è 2.
Inoltre, le due voci della directory bitmap di allocazione sono valide solo se una descrive la prima bitmap di allocazione e l'altra descrive la seconda bitmap di allocazione.

<div id="table-20-allocation-bitmap-directoryentry-structure" />

**Tabella 20 allocazione bitmap struttura DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#711-entrytype-field">sezione 7.1.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>BitmapFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#712-bitmapflags-field">sezione 7.1.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Riservato</td>
<td>2</td>
<td>18</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="even">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#713-firstcluster-field">sezione 7.1.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#714-datalength-field">sezione 7.1.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="711-entrytype-field"></a>Campo EntryType 7.1.1

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1](#631-entrytype-field).

##### <a name="7111-typecode-field"></a>Campo TypeCode 7.1.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.1](#6311-typecode-field).

Per una voce di directory bitmap di allocazione, il valore valido per questo campo è 1.

##### <a name="7112-typeimportance-field"></a>Campo 7.1.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.2](#6312-typeimportance-field).

Per una voce di directory bitmap di allocazione, il valore valido per questo campo è 0.

##### <a name="7113-typecategory-field"></a>Campo 7.1.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.3](#6313-typecategory-field).

##### <a name="7114-inuse-field"></a>Campo 7.1.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.4](#6314-inuse-field).

#### <a name="712-bitmapflags-field"></a>Campo 7.1.2 BitmapFlags

Il campo BitmapFlags contiene flag (vedere la [tabella 21](#table-21-bitmapflags-field-structure)).

<div id="table-21-bitmapflags-field-structure" />

**Tabella 21 struttura di campo BitmapFlags**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapIdentifier</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#7121-bitmapidentifier-field">sezione 7.1.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>1</td>
<td>7</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

##### <a name="7121-bitmapidentifier-field"></a>Campo 7.1.2.1 BitmapIdentifier

Il campo BitmapIdentifier indicherà la bitmap di allocazione descritta dalla voce di directory specificata. Le implementazioni utilizzeranno la prima bitmap di allocazione insieme al primo FAT e utilizzeranno la seconda bitmap di allocazione insieme al secondo FAT. Il campo ActiveFat descrive quali bitmap di allocazione e FAT sono attive.

I valori validi per questo campo saranno:

- 0, che indica che la voce di directory specificata descrive la prima bitmap di allocazione

- 1, che indica che la voce di directory specificata descrive la seconda bitmap di allocazione ed è possibile solo quando NumberOfFats contiene il valore 2

#### <a name="713-firstcluster-field"></a>Campo 7.1.3 FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.5](#635-firstcluster-field).

Questo campo contiene l'indice del primo cluster della catena del cluster, come descritto dal FAT, che ospita la bitmap di allocazione.

#### <a name="714-datalength-field"></a>7.1.4-campo DataLength

Il campo datacluster deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.6](#636-datalength-field).

#### <a name="715-allocation-bitmap"></a>Bitmap di allocazione 7.1.5

Una bitmap di allocazione registra lo stato di allocazione dei cluster nell'heap del cluster. Ogni bit in una bitmap di allocazione indica se il cluster corrispondente è disponibile o meno per l'allocazione.

Una bitmap di allocazione rappresenta i cluster dall'indice più basso a quello più alto (vedere la [tabella 22](#table-22-allocation-bitmap-structure)). Per motivi cronologici, il primo cluster dispone dell'indice 2.
Nota: il primo bit della bitmap è il bit di ordine più basso del primo byte.

<div id="table-22-allocation-bitmap-structure" />

**Tabella 22 struttura bitmap di allocazione**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>BitmapEntry [2]</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">sezione 7.1.5.1</a> ne definisce il contenuto.</td>
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
<td>BitmapEntry [Clustercount-+ 1]</td>
<td>Clustercount--1</td>
<td>1</td>
<td><p>Questo campo è obbligatorio e la <a href="#7151-bitmapentry2--bitmapentryclustercount1-fields">sezione 7.1.5.1</a> ne definisce il contenuto.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo Clustercount-.</p></td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>Clustercount-</td>
<td>(DATALENGTH * 8) – Clustercount-</td>
<td><p>Questo campo è obbligatorio e il relativo contenuto, se presente, è riservato.</p>
<p>Nota: i settori di avvio principale e di backup contengono entrambi il campo Clustercount-.</p></td>
</tr>
</tbody>
</table>

##### <a name="7151-bitmapentry2--bitmapentryclustercount1-fields"></a>7.1.5.1 BitmapEntry \[ 2 \] ... \[Campi BitmapEntry clustercount-+ 1 \]

Ogni campo BitmapEntry in questa matrice rappresenta un cluster nell'heap del cluster. BitmapEntry \[ 2 \] rappresenta il primo cluster nell'heap del cluster e BitmapEntry \[ clustercount-+ 1 \] rappresenta l'ultimo cluster nell'heap del cluster.

I valori validi per questi campi saranno:

- 0, che descrive il cluster corrispondente come disponibile per l'allocazione

- 1, che descrive il cluster corrispondente come non disponibile per l'allocazione (un'allocazione cluster può già usare il cluster corrispondente o il FAT attivo può descrivere il cluster corrispondente come danneggiato)

### <a name="72-up-case-table-directory-entry"></a>7,2 voce di directory della tabella del case

La tabella del case del case definisce la conversione da caratteri minuscoli a caratteri maiuscoli. Questo aspetto è importante a causa della voce di directory del nome file (vedere la sezione 7,7) che usa i caratteri Unicode e exFAT file system l'indistinzione tra maiuscole e minuscole e la conservazione del case. La tabella del case è presente nell'heap del cluster (vedere la [sezione 7.2.5](#725-up-case-table)) e include una voce di directory primaria critica corrispondente nella directory radice (vedere la [tabella 23](#table-23-up-case-table-directoryentry-structure)). Il numero valido di voci della directory della tabella dei case è 1.

A causa della relazione tra la tabella del case e i nomi file, le implementazioni non devono modificare la tabella del case, ad eccezione di come risultato delle operazioni di formattazione.

<div id="table-23-up-case-table-directoryentry-structure" />

**Tabella 23 tabella del case in maiuscolo, struttura DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#721-entrytype-field">sezione 7.2.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>1</td>
<td>3</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="odd">
<td>TableChecksum</td>
<td>4</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#722-tablechecksum-field">sezione 7.2.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>8</td>
<td>12</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#723-firstcluster-field">sezione 7.2.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#724-datalength-field">sezione 7.2.4</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="721-entrytype-field"></a>Campo 7.2.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1](#631-entrytype-field).

##### <a name="7211-typecode-field"></a>Campo TypeCode 7.2.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.1](#6311-typecode-field).

Per la voce della directory della tabella dei casi, il valore valido per questo campo è
2.

##### <a name="7212-typeimportance-field"></a>Campo 7.2.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.2](#6312-typeimportance-field).

Per la voce della directory della tabella dei casi, il valore valido per questo campo è
0.

##### <a name="7213-typecategory-field"></a>Campo 7.2.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.3](#6313-typecategory-field).

##### <a name="7214-inuse-field"></a>Campo 7.2.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.4](#6314-inuse-field).

#### <a name="722-tablechecksum-field"></a>Campo 7.2.2 TableChecksum

Il campo TableChecksum contiene il checksum della tabella del case che descrive i campi FirstCluster e DATALENGTH. Le implementazioni devono verificare che il contenuto di questo campo sia valido prima di utilizzare la tabella del case.

<div id="figure-3-tablechecksum-computation" />

**Figura 3 calcolo di TableChecksum**

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

#### <a name="723-firstcluster-field"></a>Campo 7.2.3 FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.5](#635-firstcluster-field).

Questo campo contiene l'indice del primo cluster della catena del cluster, come descritto dal FAT, che ospita la tabella del case.

#### <a name="724-datalength-field"></a>7.2.4-campo DataLength

Il campo datacluster deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.6](#636-datalength-field).

#### <a name="725-up-case-table"></a>7.2.5-tabella del case

Una tabella del case è una serie di mapping di caratteri Unicode. Un mapping di caratteri è costituito da un campo a 2 byte, con l'indice del campo nella tabella del case che rappresenta il carattere Unicode per cui deve essere eseguita la combinazione di maiuscole e minuscole e il campo a 2 byte che rappresenta il carattere Unicode in maiuscolo.

I primi 128 caratteri Unicode hanno mapping obbligatori (vedere la [tabella 24](#table-24-mandatory-first-128-up-case-table-entries)).
Una tabella del case con qualsiasi altro mapping di caratteri per uno dei primi 128 caratteri Unicode non è valida.

Le implementazioni che supportano solo i caratteri dell'intervallo di mapping obbligatorio potrebbero ignorare i mapping del resto della tabella del case. Tali implementazioni utilizzeranno solo i caratteri dell'intervallo di mapping obbligatorio durante la creazione o la ridenominazione dei file (tramite la voce di directory del nome file, vedere la [sezione 7,7](#77-file-name-directory-entry)). Quando si esegue il decompressione di nomi di file esistenti, tali implementazioni non devono essere presenti nell'intervallo di mapping non obbligatorio, ma devono essere manomesse nel nome del file in maiuscolo e minuscolo risultante. si tratta di una maiuscola parziale. Quando si confrontano i nomi di file, tali implementazioni tratteranno i nomi di file che differiscono dal nome sotto il confronto solo per i caratteri Unicode dall'intervallo di mapping non obbligatorio come equivalente. Sebbene tali nomi di file siano potenzialmente equivalenti, tali implementazioni non possono garantire che il nome del file con il nome completo non entri in conflitto con il nome sotto il confronto.

<div id="table-24-mandatory-first-128-up-case-table-entries" />

**Tabella 24 voci della tabella iniziale obbligatoria prima 128**

| **Indice tabella** | **Voci di tabella** |           |           |           |           |           |           |           |
|-----------------|-------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
|                 | **+ 0**           | **+ 1**   | **+ 2**   | **+ 3**   | **+ 4**   | **+ 5**   | **+ 6**   | **+ 7**   |
| **0000h**       | 0000h             | 0001H     | 0002H     | 0003h     | 0004h     | 0005h     | 0006h     | 0007h     |
| **0008h**       | 0008h             | 0009h     | 000Ah     | 000Bh     | 000Ch     | 000Dh     | 000Eh     | 000Fh     |
| **0010h**       | 0010h             | 0011h     | 0012h     | 0013h     | 0014h     | 0015h     | 0016h     | 0017h     |
| **0018h**       | 0018h             | 0019h     | 001Ah     | 001Bh     | 001Ch     | 001Dh     | 001Eh     | 001Fh     |
| **0020h**       | 0020h             | 0021h     | 0022h     | 0023h     | 0024h     | 0025h     | 0026h     | 0027h     |
| **0028h**       | 0028h             | 0029h     | 002Ah     | 002Bh     | 002Ch     | 002Dh     | 002Eh     | 002Fh     |
| **0030h**       | 0030h             | 0031h     | 0032h     | 0033h     | 0034h     | 0035h     | 0036h     | 0037h     |
| **0038h**       | 0038h             | 0039h     | 003Ah     | 003Bh     | 003Ch     | 003Dh     | 003Eh     | 003Fh     |
| **0040H**       | 0040H             | 0041h     | 0042h     | 0043h     | 0044h     | 0045h     | 0046h     | 0047h     |
| **0048h**       | 0048h             | 0049h     | 004Ah     | 004Bh     | 004Ch     | 004Dh     | 004Eh     | 004Fh     |
| **0050h**       | 0050h             | 0051h     | 0052h     | 0053h     | 0054h     | 0055h     | 0056h     | 0057h     |
| **0058h**       | 0058h             | 0059h     | 005Ah     | 005Bh     | 005Ch     | 005Dh     | 005Eh     | 005Fh     |
| **0060h**       | 0060h             | **0041h** | **0042h** | **0043h** | **0044h** | **0045h** | **0046h** | **0047h** |
| **0068h**       | **0048h**         | **0049h** | **004Ah** | **004Bh** | **004Ch** | **004Dh** | **004Eh** | **004Fh** |
| **0070h**       | **0050h**         | **0051h** | **0052h** | **0053h** | **0054h** | **0055h** | **0056h** | **0057h** |
| **0078h**       | **0058h**         | **0059h** | **005Ah** | 007Bh     | 007Ch     | 007Dh     | 007Eh     | 007Fh     |

**Nota: le voci con mapping dei case non di identità sono in grassetto.**

Quando si formatta un volume, le implementazioni possono generare una tabella del case in un formato compresso usando la compressione del mapping delle identità, poiché una parte grande dello spazio dei caratteri Unicode non ha alcun concetto di caso (ovvero i caratteri "minuscole" e "maiuscole" sono equivalenti).
Le implementazioni comprimeno una tabella del case, rappresentando una serie di mapping di identità con il valore FFFFh seguito dal numero di mapping di identità.

Un'implementazione, ad esempio, può rappresentare i primi mapping di caratteri 100 (64H) con le otto voci seguenti di una tabella del case in formato compresso:

> FFFFh, 0061h, 0041h, 0042h, 0043h

Le prime due voci indicano che i primi 97 caratteri (61H) (da 0000h a 0060h) hanno mapping di identità. I caratteri successivi, 0061h tramite 0063h, vengono mappati ai caratteri rispettivamente 0041h tramite 0043h.

La possibilità di fornire una tabella del case in formato compresso alla formattazione di un volume è facoltativa. Tuttavia, la possibilità di interpretare sia una tabella del case non compressa che una tabella del case compressa è obbligatoria. Il valore del campo TableChecksum è sempre conforme al modo in cui esiste la tabella del case nel volume, che può essere in formato compresso o non compresso.

##### <a name="7251-recommended-up-case-table"></a>7.2.5.1-tabella del case consigliata

Quando si formatta un volume, le implementazioni devono registrare la tabella del caso non consigliata in formato compresso (vedere la [tabella 25](#table-25-recommended-up-case-table-in-compressed-format)), per la quale il valore del campo TableChecksum è E619D30Dh.

Se un'implementazione definisce la propria tabella del case, compressa o non compressa, la tabella coprirà l'intervallo di caratteri Unicode completo (dai codici carattere 0000h a FFFFh inclusivo).

<div id="table-25-recommended-up-case-table-in-compressed-format" />

**Tabella 25 consigliata tabella del case nel formato compresso**

| **Offset non elaborato** | **Voci di tabella compresse** |         |         |         |         |         |         |         |
|----------------|------------------------------|---------|---------|---------|---------|---------|---------|---------|
|                | **+ 0**                      | **+ 1** | **+ 2** | **+ 3** | **+ 4** | **+ 5** | **+ 6** | **+ 7** |
| **0000h**      | 0000h                        | 0001H   | 0002H   | 0003h   | 0004h   | 0005h   | 0006h   | 0007h   |
| **0008h**      | 0008h                        | 0009h   | 000Ah   | 000Bh   | 000Ch   | 000Dh   | 000Eh   | 000Fh   |
| **0010h**      | 0010h                        | 0011h   | 0012h   | 0013h   | 0014h   | 0015h   | 0016h   | 0017h   |
| **0018h**      | 0018h                        | 0019h   | 001Ah   | 001Bh   | 001Ch   | 001Dh   | 001Eh   | 001Fh   |
| **0020h**      | 0020h                        | 0021h   | 0022h   | 0023h   | 0024h   | 0025h   | 0026h   | 0027h   |
| **0028h**      | 0028h                        | 0029h   | 002Ah   | 002Bh   | 002Ch   | 002Dh   | 002Eh   | 002Fh   |
| **0030h**      | 0030h                        | 0031h   | 0032h   | 0033h   | 0034h   | 0035h   | 0036h   | 0037h   |
| **0038h**      | 0038h                        | 0039h   | 003Ah   | 003Bh   | 003Ch   | 003Dh   | 003Eh   | 003Fh   |
| **0040H**      | 0040H                        | 0041h   | 0042h   | 0043h   | 0044h   | 0045h   | 0046h   | 0047h   |
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
| **0098h**      | 0098h                        | 0099h   | 009Ah   | 009Bh   | 009Ch   | 009Dh   | 009Eh   | 009Fh   |
| **00A0h**      | 00A0h                        | 00A1h   | 00A2h   | 00A3h   | 00A4h   | 00A5h   | 00A6h   | 00A7h   |
| **00A8h**      | 00A8h                        | 00A9h   | 00AAh   | 00ABh   | 00ACh   | 00ADh   | 00AEh   | 00AFh   |
| **00B0h**      | 00B0h                        | 00B1h   | 00B2h   | 00B3h   | 00B4h   | 00B5h   | 00B6h   | 00B7h   |
| **00B8h**      | 00B8h                        | 00B9h   | 00BAh   | 00BBh   | 00BCh   | 00BDh   | 00BEh   | 00BFh   |
| **00C0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00C8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00D0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00D7h   |
| **00D8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 00DFh   |
| **00E0h**      | 00C0h                        | 00C1h   | 00C2h   | 00C3h   | 00C4h   | 00C5h   | 00C6h   | 00C7h   |
| **00E8h**      | 00C8h                        | 00C9h   | 00CAh   | 00CBh   | 00CCh   | 00CDh   | 00CEh   | 00CFh   |
| **00F0h**      | 00D0h                        | 00D1h   | 00D2h   | 00D3h   | 00D4h   | 00D5h   | 00D6h   | 00F7h   |
| **00F8h**      | 00D8h                        | 00D9h   | 00DAh   | 00DBh   | 00DCh   | 00DDh   | 00DEh   | 0178h   |
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
| **03D8h**      | 03D8h                        | 03D8h   | 03DAh   | 03DAh   | 03DCh   | 03DCh   | 03DEh   | 03DEh   |
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
| **0588h**      | 17F6h                        | 2C63h   | 1D7Eh   | 1D7Fh   | 1D80h   | 1D81h   | 1D82h   | 1D83h   |
| **0590h**      | 1D84h                        | 1D85h   | 1D86h   | 1D87h   | 1D88h   | 1D89h   | 1D8Ah   | 1D8Bh   |
| **0598h**      | 1D8Ch                        | 1D8Dh   | 1D8Eh   | 1D8Fh   | 1D90h   | 1D91h   | 1D92h   | 1D93h   |
| **05A0h**      | 1D94h                        | 1D95h   | 1D96h   | 1D97h   | 1D98h   | 1D99h   | 1D9Ah   | 1D9Bh   |
| **05A8h**      | 1D9Ch                        | 1D9Dh   | 1D9Eh   | 1D9Fh   | 1DA0h   | 1DA1h   | 1DA2h   | 1DA3h   |
| **05B0h**      | 1DA4h                        | 1DA5h   | 1DA6h   | 1DA7h   | 1DA8h   | 1DA9h   | 1DAAh   | 1DABh   |
| **05B8h**      | 1DACh                        | 1DADh   | 1DAEh   | 1DAFh   | 1DB0h   | 1DB1h   | 1DB2h   | 1DB3h   |
| **05C0h**      | 1DB4h                        | 1DB5h   | 1DB6h   | 1DB7h   | 1DB8h   | 1DB9h   | 1DBAh   | 1DBBh   |
| **05C8h**      | 1DBCh                        | 1DBDh   | 1DBEh   | 1DBFh   | 1DC0h   | 1DC1h   | 1DC2h   | 1DC3h   |
| **05D0h**      | 1DC4h                        | 1DC5h   | 1DC6h   | 1DC7h   | 1DC8h   | 1DC9h   | 1DCAh   | 1DCBh   |
| **05D8h**      | 1DCCh                        | 1DCDh   | 1DCEh   | 1DCFh   | 1DD0h   | 1DD1h   | 1DD2h   | 1DD3h   |
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
| **06B8h**      | 1EACh                        | 1EACh   | 1EAEh   | 1EAEh   | 1EB0h   | 1EB0h   | 1EB2h   | 1EB2h   |
| **06C0h**      | 1EB4h                        | 1EB4h   | 1EB6h   | 1EB6h   | 1EB8h   | 1EB8h   | 1EBAh   | 1EBAh   |
| **06C8h**      | 1EBCh                        | 1EBCh   | 1EBEh   | 1EBEh   | 1EC0h   | 1EC0h   | 1EC2h   | 1EC2h   |
| **06D0h**      | 1EC4h                        | 1EC4h   | 1EC6h   | 1EC6h   | 1EC8h   | 1EC8h   | 1ECAh   | 1ECAh   |
| **06D8h**      | 1ECCh                        | 1ECCh   | 1ECEh   | 1ECEh   | 1ED0h   | 1ED0h   | 1ED2h   | 1ED2h   |
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
| **0818h**      | 200Ch                        | 200Dh   | 200Eh   | 200Fh   | 2010h   | 2011h   | 2012h   | 2013h   |
| **0820h**      | 2014h                        | 2015h   | 2016h   | 2017h   | 2018h   | 2019h   | 201Ah   | 201Bh   |
| **0828h**      | 201Ch                        | 201Dh   | 201Eh   | 201Fh   | 2020h   | 2021h   | 2022h   | 2023h   |
| **0830h**      | 2024h                        | 2025h   | 2026h   | 2027h   | 2028h   | 2029h   | 202Ah   | 202Bh   |
| **0838h**      | 202Ch                        | 202Dh   | 202Eh   | 202Fh   | 2030h   | 2031h   | 2032h   | 2033h   |
| **0840h**      | 2034h                        | 2035h   | 2036h   | 2037h   | 2038h   | 2039h   | 203Ah   | 203Bh   |
| **0848h**      | 203Ch                        | 203Dh   | 203Eh   | 203Fh   | 2040h   | 2041h   | 2042h   | 2043h   |
| **0850h**      | 2044h                        | 2045h   | 2046h   | 2047h   | 2048h   | 2049h   | 204Ah   | 204Bh   |
| **0858h**      | 204Ch                        | 204Dh   | 204Eh   | 204Fh   | 2050h   | 2051h   | 2052h   | 2053h   |
| **0860h**      | 2054h                        | 2055h   | 2056h   | 2057h   | 2058h   | 2059h   | 205Ah   | 205Bh   |
| **0868h**      | 205Ch                        | 205Dh   | 205Eh   | 205Fh   | 2060h   | 2061h   | 2062h   | 2063h   |
| **0870h**      | 2064h                        | 2065h   | 2066h   | 2067h   | 2068h   | 2069h   | 206Ah   | 206Bh   |
| **0878h**      | 206Ch                        | 206Dh   | 206Eh   | 206Fh   | 2070h   | 2071h   | 2072h   | 2073h   |
| **0880h**      | 2074h                        | 2075h   | 2076h   | 2077h   | 2078h   | 2079h   | 207Ah   | 207Bh   |
| **0888h**      | 207Ch                        | 207Dh   | 207Eh   | 207Fh   | 2080h   | 2081h   | 2082h   | 2083h   |
| **0890h**      | 2084h                        | 2085h   | 2086h   | 2087h   | 2088h   | 2089h   | 208Ah   | 208Bh   |
| **0898h**      | 208Ch                        | 208Dh   | 208Eh   | 208Fh   | 2090h   | 2091h   | 2092h   | 2093h   |
| **08A0h**      | 2094h                        | 2095h   | 2096h   | 2097h   | 2098h   | 2099h   | 209Ah   | 209Bh   |
| **08A8h**      | 209Ch                        | 209Dh   | 209Eh   | 209Fh   | 20A0h   | 20A1h   | 20A2h   | 20A3h   |
| **08B0h**      | 20A4h                        | 20A5h   | 20A6h   | 20A7h   | 20A8h   | 20A9h   | 20AAh   | 20ABh   |
| **08B8h**      | 20ACh                        | 20ADh   | 20AEh   | 20AFh   | 20B0h   | 20B1h   | 20B2h   | 20B3h   |
| **08C0h**      | 20B4h                        | 20B5h   | 20B6h   | 20B7h   | 20B8h   | 20B9h   | 20BAh   | 20BBh   |
| **08C8h**      | 20BCh                        | 20BDh   | 20BEh   | 20BFh   | 20C0h   | 20C1h   | 20C2h   | 20C3h   |
| **08D0h**      | 20C4h                        | 20C5h   | 20C6h   | 20C7h   | 20C8h   | 20C9h   | 20CAh   | 20CBh   |
| **08D8h**      | 20CCh                        | 20CDh   | 20CEh   | 20CFh   | 20D0h   | 20D1h   | 20D2h   | 20D3h   |
| **08E0h**      | 20D4h                        | 20D5h   | 20D6h   | 20D7h   | 20D8h   | 20D9h   | 20DAh   | 20DBh   |
| **08E8h**      | 20DCh                        | 20DDh   | 20DEh   | 20DFh   | 20E0h   | 20E1h   | 20E2h   | 20E3h   |
| **08F0h**      | 20E4h                        | 20E5h   | 20E6h   | 20E7h   | 20E8h   | 20E9h   | 20EAh   | 20EBh   |
| **08F8h**      | 20ECh                        | 20EDh   | 20EEh   | 20EFh   | 20F0h   | 20F1h   | 20F2h   | 20F3h   |
| **0900h**      | 20F4h                        | 20F5h   | 20F6h   | 20F7h   | 20F8h   | 20F9h   | 20FAh   | 20FBh   |
| **0908h**      | 20FCh                        | 20FDh   | 20FEh   | 20FFh   | 2100h   | 2101h   | 2102h   | 2103h   |
| **0910h**      | 2104h                        | 2105h   | 2106h   | 2107h   | 2108h   | 2109h   | 210Ah   | 210Bh   |
| **0918h**      | 210Ch                        | 210Dh   | 210Eh   | 210Fh   | 2110h   | 2111h   | 2112h   | 2113h   |
| **0920h**      | 2114h                        | 2115h   | 2116h   | 2117h   | 2118h   | 2119h   | 211Ah   | 211Bh   |
| **0928h**      | 211Ch                        | 211Dh   | 211Eh   | 211Fh   | 2120h   | 2121h   | 2122h   | 2123h   |
| **0930h**      | 2124h                        | 2125h   | 2126h   | 2127h   | 2128h   | 2129h   | 212Ah   | 212Bh   |
| **0938h**      | 212Ch                        | 212Dh   | 212Eh   | 212Fh   | 2130h   | 2131h   | 2132h   | 2133h   |
| **0940h**      | 2134h                        | 2135h   | 2136h   | 2137h   | 2138h   | 2139h   | 213Ah   | 213Bh   |
| **0948h**      | 213Ch                        | 213Dh   | 213Eh   | 213Fh   | 2140h   | 2141h   | 2142h   | 2143h   |
| **0950h**      | 2144h                        | 2145h   | 2146h   | 2147h   | 2148h   | 2149h   | 214Ah   | 214Bh   |
| **0958h**      | 214Ch                        | 214Dh   | 2132h   | 214Fh   | 2150h   | 2151h   | 2152h   | 2153h   |
| **0960h**      | 2154h                        | 2155h   | 2156h   | 2157h   | 2158h   | 2159h   | 215Ah   | 215Bh   |
| **0968h**      | 215Ch                        | 215Dh   | 215Eh   | 215Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0970h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0978h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2160h   | 2161h   | 2162h   | 2163h   |
| **0980h**      | 2164h                        | 2165h   | 2166h   | 2167h   | 2168h   | 2169h   | 216Ah   | 216Bh   |
| **0988h**      | 216Ch                        | 216Dh   | 216Eh   | 216Fh   | 2180h   | 2181h   | 2182h   | 2183h   |
| **0990h**      | 2183h                        | FFFFh   | 034Bh   | 24B6h   | 24B7h   | 24B8h   | 24B9h   | 24BAh   |
| **0998h**      | 24BBh                        | 24BCh   | 24BDh   | 24BEh   | 24BFh   | 24C0h   | 24C1h   | 24C2h   |
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
| **0A98h**      | 10B9h                        | 10BAh   | 10BBh   | 10BCh   | 10BDh   | 10BEh   | 10BFh   | 10C0h   |
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
| **0B50h**      | FFEAh                        | FFEBh   | FFECh   | FFEDh   | Su FFEEh   | FFEFh   | FFF0h   | FFF1h   |
| **0B58h**      | FFF2h                        | FFF3h   | FFF4h   | FFF5h   | FFF6h   | FFF7h   | FFF8h   | FFF9h   |
| **0B60h**      | FFFAh                        | FFFBh   | FFFCh   | FFFDh   | FFFEh   | FFFFh   |         |         |

### <a name="73-volume-label-directory-entry"></a>Voce di directory dell'etichetta del volume 7,3

L'etichetta del volume è una stringa Unicode che consente agli utenti finali di distinguere i volumi di archiviazione. Nel file system exFAT l'etichetta del volume esiste come voce di directory primaria critica nella directory radice (vedere la [tabella 26](#table-26-volume-label-directoryentry-structure)). Il numero di voci di directory dell'etichetta volume valido è compreso tra 0 e 1.

<div id="table-26-volume-label-directoryentry-structure" />

**Tabella 26 etichetta del volume DirectoryEntry Structure**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#731-entrytype-field">sezione 7.3.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>CharacterCount</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#732-charactercount-field">sezione 7.3.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeLabel</td>
<td>2</td>
<td>22</td>
<td>Questo campo è obbligatorio e la <a href="#733-volumelabel-field">sezione 7.3.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

#### <a name="731-entrytype-field"></a>Campo 7.3.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1](#631-entrytype-field).

##### <a name="7311-typecode-field"></a>Campo TypeCode 7.3.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.1](#6311-typecode-field).

Per la voce di directory label volume, il valore valido per questo campo è
3.

##### <a name="7312-typeimportance-field"></a>Campo 7.3.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.2](#6312-typeimportance-field).

Per la voce di directory label volume, il valore valido per questo campo è
0.

##### <a name="7313-typecategory-field"></a>Campo 7.3.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.3](#6313-typecategory-field).

##### <a name="7314-inuse-field"></a>Campo 7.3.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.4](#6314-inuse-field).

#### <a name="732-charactercount-field"></a>Campo 7.3.2 CharacterCount

Il campo CharacterCount conterrà la lunghezza della stringa Unicode in cui è contenuto il campo VolumeLabel.

L'intervallo valido di valori per questo campo sarà:

- Almeno 0, che indica che la stringa Unicode ha una lunghezza pari a 0 caratteri (che equivale a nessuna etichetta del volume)

- Al massimo 11, che significa che la stringa Unicode ha una lunghezza di 11 caratteri

#### <a name="733-volumelabel-field"></a>Campo 7.3.3 VolumeLabel

Il campo VolumeLabel deve contenere una stringa Unicode, ovvero il nome descrittivo del volume. Il campo VolumeLabel contiene lo stesso set di caratteri non validi del campo FileName della voce di directory nome file (vedere la [sezione 7.7.3](#773-filename-field)).

### <a name="74-file-directory-entry"></a>7,4 voce directory file

Le voci della directory di file descrivono file e directory. Si tratta di voci di directory primarie critiche e qualsiasi directory può contenere zero o più voci di directory di file (vedere la [tabella 27](#table-27-file-directoryentry)). Affinché una voce di directory di file sia valida, una voce di directory di estensione del flusso e almeno una voce di directory di nome file deve seguire immediatamente la voce della directory di file (vedere rispettivamente la [sezione 7,6](#76-stream-extension-directory-entry) e la [sezione 7,7](#77-file-name-directory-entry)).

<div id="table-27-file-directoryentry" />

**Tabella 27 file DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#741-entrytype-field">sezione 7.4.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#742-secondarycount-field">sezione 7.4.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#743-setchecksum-field">sezione 7.4.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>FileAttributes</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#744-fileattributes-field">sezione 7.4.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>6</td>
<td>2</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="even">
<td>CreateTimestamp</td>
<td>8</td>
<td>4</td>
<td>Questo campo è obbligatorio e <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la sezione 7.4.5 </
a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>LastModifiedTimestamp</td>
<td>12</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">sezione 7.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>LastAccessedTimestamp</td>
<td>16</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">sezione 7.4.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Create10msIncrement</td>
<td>20</td>
<td>1</td>
<td>Questo campo è obbligatorio e <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la sezione 7.4.5 </
a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>LastModified10msIncrement</td>
<td>21</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">sezione 7.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>CreateUtcOffset</td>
<td>22</td>
<td>1</td>
<td>Questo campo è obbligatorio e <a href="#745-createtimestamp-create10msincrement-and-createutcoffset-fields"> la sezione 7.4.5 </
a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>LastModifiedUtcOffset</td>
<td>23</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields">sezione 7.4.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>LastAccessedUtcOffset</td>
<td>24</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields">sezione 7.4.7</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>25</td>
<td>7</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

#### <a name="741-entrytype-field"></a>Campo 7.4.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1](#631-entrytype-field).

##### <a name="7411-typecode-field"></a>Campo TypeCode 7.4.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.1](#6311-typecode-field).

Per una voce di directory di file, il valore valido per questo campo è 5.

##### <a name="7412-typeimportance-field"></a>Campo 7.4.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.2](#6312-typeimportance-field).

Per una voce di directory di file, il valore valido per questo campo è 0.

##### <a name="7413-typecategory-field"></a>Campo 7.4.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.3](#6313-typecategory-field).

##### <a name="7414-inuse-field"></a>Campo 7.4.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.4](#6314-inuse-field).

#### <a name="742-secondarycount-field"></a>Campo 7.4.2 SecondaryCount

Il campo SecondaryCount deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.2](#632-secondarycount-field).

#### <a name="743-setchecksum-field"></a>7.4.3 (campo di controllo)

Il campo del controllo di digitazione deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.3](#633-setchecksum-field).

#### <a name="744-fileattributes-field"></a>Campo 7.4.4 FileAttributes

Il campo FileAttributes contiene flag (vedere la [tabella 28](#table-28-fileattributes-field-structure)).

<div id="table-28-fileattributes-field-structure" />

**Tabella 28 struttura del campo FileAttributes**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ReadOnly</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e deve essere conforme alla definizione di MS-DOS.</td>
</tr>
<tr class="even">
<td>Nascosto</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e deve essere conforme alla definizione di MS-DOS.</td>
</tr>
<tr class="odd">
<td>Sistema</td>
<td>2</td>
<td>1</td>
<td>Questo campo è obbligatorio e deve essere conforme alla definizione di MS-DOS.</td>
</tr>
<tr class="even">
<td>Reserved1</td>
<td>3</td>
<td>1</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="odd">
<td>Directory</td>
<td>4</td>
<td>1</td>
<td>Questo campo è obbligatorio e deve essere conforme alla definizione di MS-DOS.</td>
</tr>
<tr class="even">
<td>Archiviazione</td>
<td>5</td>
<td>1</td>
<td>Questo campo è obbligatorio e deve essere conforme alla definizione di MS-DOS.</td>
</tr>
<tr class="odd">
<td>Reserved2</td>
<td>6</td>
<td>10</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

#### <a name="745-createtimestamp-create10msincrement-and-createutcoffset-fields"></a>Campi 7.4.5 CreateTimestamp, Create10msIncrement e CreateUtcOffset

In combinazione, i campi CreateTimestamp e CreateTime10msIncrement descrivono la data e l'ora locali in cui è stata creata la directory o il file specificato. Il campo CreateUtcOffset descrive l'offset della data e dell'ora locali dall'ora UTC. Le implementazioni devono impostare questi campi al momento della creazione del set di voci di directory specificato.

Questi campi devono essere conformi alle definizioni dei campi timestamp, 10msIncrement e UtcOffset (vedere rispettivamente la sezione [7.4.8](#748-timestamp-fields), la [sezione 7.4.9](#749-10msincrement-fields)e la [sezione 7.4.10](#7410-utcoffset-fields)).

#### <a name="746-lastmodifiedtimestamp-lastmodified10msincrement-and-lastmodifiedutcoffset-fields"></a>Campi 7.4.6 LastModifiedTimestamp, LastModified10msIncrement e LastModifiedUtcOffset

In combinazione, i campi LastModifiedTimestamp e LastModifiedTime10msIncrement descrivono la data e l'ora locali in cui è stato modificato l'ultima modifica del contenuto di tutti i cluster associati alla voce di directory dell'estensione di flusso specificata. Il campo LastModifiedUtcOffset descrive l'offset della data e dell'ora locali dall'ora UTC. Le implementazioni devono aggiornare i campi seguenti:

1. Dopo aver modificato il contenuto di uno dei cluster associati alla voce di directory dell'estensione di flusso specificata (ad eccezione dei contenuti presenti oltre il punto in cui viene descritto il campo ValidDataLength)

2. Quando si modificano i valori dei campi ValidDataLength o DataLength

Questi campi devono essere conformi alle definizioni dei campi timestamp, 10msIncrement e UtcOffset (vedere rispettivamente la sezione [7.4.8](#748-timestamp-fields), la [sezione 7.4.9](#749-10msincrement-fields)e la [sezione 7.4.10](#7410-utcoffset-fields)).

#### <a name="747-lastaccessedtimestamp-and-lastaccessedutcoffset-fields"></a>Campi 7.4.7 LastAccessedTimestamp e LastAccessedUtcOffset

Il campo LastAccessedTimestamp descrivono la data e l'ora locali in cui è stato eseguito l'ultimo accesso al contenuto di uno dei cluster associati alla voce di directory dell'estensione di flusso specificata. Il campo LastAccessedUtcOffset descrive l'offset della data e dell'ora locali dall'ora UTC.
Le implementazioni devono aggiornare i campi seguenti:

1. Dopo aver modificato il contenuto di tutti i cluster associati alla voce di directory dell'estensione di flusso specificata (ad eccezione dei contenuti presenti oltre il ValidDataLength)

2. Quando si modificano i valori dei campi ValidDataLength o DataLength

Le implementazioni devono aggiornare questi campi dopo la lettura del contenuto di tutti i cluster associati alla voce di directory dell'estensione di flusso specificata.

Questi campi devono essere conformi alle definizioni dei campi timestamp e UtcOffset (vedere rispettivamente la [sezione 7.4.8](#748-timestamp-fields) e la [sezione 7.4.10](#7410-utcoffset-fields)).

#### <a name="748-timestamp-fields"></a>Campi timestamp 7.4.8

I campi timestamp descrivono la data e l'ora locali, fino a una risoluzione di due secondi (vedere la [tabella 29](#table-29-timestamp-field-structure)).

<div id="table-29-timestamp-field-structure" />

**Tabella 29 struttura del campo timestamp**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DoubleSeconds</td>
<td>0</td>
<td>5</td>
<td>Questo campo è obbligatorio e la <a href="#7481-doubleseconds-field">sezione 7.4.8.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Minuto</td>
<td>5</td>
<td>6</td>
<td>Questo campo è obbligatorio e la <a href="#7482-minute-field">sezione 7.4.8.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Ora</td>
<td>11</td>
<td>5</td>
<td>Questo campo è obbligatorio e la <a href="#7483-hour-field">sezione 7.4.8.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Giorno</td>
<td>16</td>
<td>5</td>
<td>Questo campo è obbligatorio e la <a href="#7484-day-field">sezione 7.4.8.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Month</td>
<td>21</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#7485-month-field">sezione 7.4.8.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Year</td>
<td>25</td>
<td>7</td>
<td>Questo campo è obbligatorio e la <a href="#7486-year-field">sezione 7.4.8.6</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="7481-doubleseconds-field"></a>Campo 7.4.8.1 DoubleSeconds

Il campo DoubleSeconds descrive la parte relativa ai secondi del campo timestamp, in multipli di due secondi.

L'intervallo valido di valori per questo campo sarà:

- 0, che rappresenta 0 secondi

- 29, che rappresenta 58 secondi

##### <a name="7482-minute-field"></a>Campo 7.4.8.2 minuti

Il campo minuti descrivono la parte relativa ai minuti del campo timestamp.

L'intervallo valido di valori per questo campo sarà:

- 0, che rappresenta 0 minuti

- 59, che rappresenta 59 minuti

##### <a name="7483-hour-field"></a>Campo 7.4.8.3 hour

Il campo hour descriva la parte hours del campo timestamp.

L'intervallo valido di valori per questo campo sarà:

- 0, che rappresenta 00:00 ore

- 23, che rappresenta 23:00 ore

##### <a name="7484-day-field"></a>Campo 7.4.8.4 Day

Il campo Day descrivono la parte relativa al giorno del campo timestamp.

L'intervallo valido di valori per questo campo sarà:

- 1, ovvero il primo giorno del mese specificato

- Ultimo giorno del mese specificato (il mese specificato definisce il numero di giorni validi)

##### <a name="7485-month-field"></a>Campo 7.4.8.5 month

Il campo month descriva la porzione month del campo timestamp.

L'intervallo valido di valori per questo campo sarà:

- Almeno 1, che rappresenta il gennaio

- Al massimo 12, che rappresenta dicembre

##### <a name="7486-year-field"></a>Campo 7.4.8.6 year

Il campo Year descriva la parte relativa all'anno del campo timestamp rispetto all'anno 1980. Questo campo rappresenta l'anno 1980 con il valore 0 e l'anno 2107 con il valore 127.

Tutti i valori possibili per questo campo sono validi.

#### <a name="749-10msincrement-fields"></a>Campi 10msIncrement di 7.4.9

i campi 10msIncrement forniscono ulteriore risoluzione del tempo ai campi timestamp corrispondenti nei multipli di dieci millisecondi.

L'intervallo valido di valori per questi campi deve essere:

- Almeno 0, che rappresenta 0 millisecondi

- Al massimo 199, che rappresenta 1990 millisecondi

#### <a name="7410-utcoffset-fields"></a>Campi UtcOffset di 7.4.10

I campi UtcOffset (vedere la [tabella 30](#table-30-utcoffset-field-structure)) descrivono l'offset dall'ora UTC alla data e all'ora locali in cui vengono descritti i campi timestamp e 10msIncrement corrispondenti. L'offset dall'ora UTC alla data e all'ora locali include gli effetti dei fusi orari e altre rettifiche di data e ora, ad esempio le modifiche all'ora legale e all'ora dell'ora legale.

<div id="table-30-utcoffset-field-structure" />

**Tabella 30 struttura del campo UtcOffset**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>po'</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>bit</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OffsetFromUtc</td>
<td>0</td>
<td>7</td>
<td>Questo campo è obbligatorio e la <a href="#74101-offsetfromutc-field">sezione 7.4.10.1</a>ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>OffsetValid</td>
<td>7</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#74102-offsetvalid-field">sezione 7.4.10.2</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

##### <a name="74101-offsetfromutc-field"></a>Campo 7.4.10.1 OffsetFromUtc

Il campo OffsetFromUtc descrivono l'offset rispetto all'ora UTC della data e dell'ora locali in cui sono contenuti i campi timestamp e 10msIncrement correlati.
Questo campo descrive l'offset dall'ora UTC a intervalli di 15 minuti (vedere la tabella 31).

<div id="table-31-meaning-of-the-values-of-the-offsetfromutc-field" />

**Tabella 31 significato dei valori del campo OffsetFromUtc**

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
<td>le 17:00</td>
<td>0</td>
<td>La data e l'ora locali sono UTC</td>
</tr>
<tr class="even">
<td>7Fh</td>
<td>-1</td>
<td>La data e l'ora locali sono UTC – 00:15</td>
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
<td>41h</td>
<td>-63</td>
<td>La data e l'ora locali sono UTC – 15:45</td>
</tr>
<tr class="odd">
<td>40h</td>
<td>-64</td>
<td>La data e l'ora locali sono UTC – 16:00</td>
</tr>
</tbody>
</table>

Come indicato nella tabella precedente, tutti i valori possibili per questo campo sono validi. Tuttavia, le implementazioni devono registrare il valore 00h solo per questo campo quando:

1. La data e l'ora locali sono in realtà identiche all'ora UTC, nel qual caso il valore del campo OffsetValid sarà 1

2. La data e l'ora locali non sono note, nel qual caso il valore del campo OffsetValid sarà 1 e le implementazioni considereranno UTC come data e ora locali

3. L'ora UTC non è nota, nel qual caso il valore del campo OffsetValid sarà 0

Se l'offset di data e ora locale rispetto all'ora UTC non è un multiplo di intervalli di 15 minuti, le implementazioni registreranno 00h nel campo OffsetFromUtc e considereranno UTC come data e ora locali.

##### <a name="74102-offsetvalid-field"></a>Campo 7.4.10.2 OffsetValid

Il campo OffsetValid indica se il contenuto del campo OffsetFromUtc è valido o meno, come indicato di seguito:

- 0, che indica che il contenuto del campo OffsetFromUtc non è valido
    > e sarà 00h

- 1, che indica che il contenuto del campo OffsetFromUtc è valido

Le implementazioni devono impostare questo campo solo sul valore 0 quando l'ora UTC non è disponibile per il calcolo del valore del campo OffsetFromUtc. Se questo campo contiene il valore 0, le implementazioni devono considerare i campi timestamp e 10msIncrement come aventi lo stesso offset UTC della data e dell'ora locali correnti.

### <a name="75-volume-guid-directory-entry"></a>7,5 voce directory GUID volume

La voce della directory GUID del volume contiene un GUID che consente alle implementazioni di distinguere i volumi in modo univoco e a livello di codice.
Il GUID del volume esiste come voce di directory primaria benigna nella directory radice (vedere la [tabella 32](#table-32-volume-guid-directoryentry)). Il numero di voci della directory GUID del volume valido è compreso tra 0 e 1.

<div id="table-32-volume-guid-directoryentry" />

**Tabella 32 GUID volume DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#751-entrytype-field">sezione 7.5.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>SecondaryCount</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#752-secondarycount-field">sezione 7.5.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>SetChecksum</td>
<td>2</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#753-setchecksum-field">sezione 7.5.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralPrimaryFlags</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#754-generalprimaryflags-field">sezione 7.5.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VolumeGuid</td>
<td>6</td>
<td>16</td>
<td>Questo campo è obbligatorio e la <a href="#755-volumeguid-field">sezione 7.5.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Riservato</td>
<td>22</td>
<td>10</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
</tbody>
</table>

#### <a name="751-entrytype-field"></a>Campo 7.5.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1](#631-entrytype-field).

##### <a name="7511-typecode-field"></a>Campo TypeCode 7.5.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.1](#6311-typecode-field).

Per la voce della directory GUID del volume, il valore valido per questo campo è
0.

##### <a name="7512-typeimportance-field"></a>Campo 7.5.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.2](#6312-typeimportance-field).

Per la voce della directory GUID del volume, il valore valido per questo campo è
1.

##### <a name="7513-typecategory-field"></a>Campo 7.5.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.3](#6313-typecategory-field).

##### <a name="7514-inuse-field"></a>Campo 7.5.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.1.4](#6314-inuse-field).

#### <a name="752-secondarycount-field"></a>Campo 7.5.2 SecondaryCount

Il campo SecondaryCount deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.2](#632-secondarycount-field).

Per la voce della directory GUID del volume, il valore valido per questo campo è
0.

#### <a name="753-setchecksum-field"></a>7.5.3 (campo di controllo)

Il campo del controllo di digitazione deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.3](#633-setchecksum-field).

#### <a name="754-generalprimaryflags-field"></a>Campo 7.5.4 GeneralPrimaryFlags

Il campo GeneralPrimaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico (vedere la [sezione 6.3.4](#634-generalprimaryflags-field)) e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7541-allocationpossible-field"></a>Campo 7.5.4.1 AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.4.1](#6341-allocationpossible-field).

Per la voce della directory GUID del volume, il valore valido per questo campo è
0.

##### <a name="7542-nofatchain-field"></a>Campo 7.5.4.2 NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry primario generico. vedere la [sezione 6.3.4.2](#6342-nofatchain-field).

#### <a name="755-volumeguid-field"></a>Campo 7.5.5 VolumeGuid

Il campo VolumeGuid deve contenere un GUID che identifica in modo univoco il volume specificato.

Tutti i valori possibili per questo campo sono validi, ad eccezione del GUID null, ovvero {00000000-0000-0000-0000-000000000000} .

### <a name="76-stream-extension-directory-entry"></a>Voce di directory dell'estensione di flusso 7,6

La voce della directory dell'estensione del flusso è una voce di directory secondaria critica nei set di voci di directory di file (vedere la [tabella 33](#table-33-stream-extension-directoryentry)). Il numero valido di voci di directory di estensione del flusso in un set di voci della directory di file è 1.
Inoltre, questa voce di directory è valida solo se segue immediatamente la voce della directory di file.

<div id="table-33-stream-extension-directoryentry" />

**Tabella 33 estensione di flusso DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#761-entrytype-field">sezione 7.6.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#762-generalsecondaryflags-field">sezione 7.6.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>Reserved1</td>
<td>2</td>
<td>1</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="even">
<td>NameLength</td>
<td>3</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#763-namelength-field">sezione 7.6.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>NameHash</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio e la <a href="#764-namehash-field">sezione 7.6.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved2</td>
<td>6</td>
<td>2</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="odd">
<td>ValidDataLength</td>
<td>8</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#765-validdatalength-field">sezione 7.6.5</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Reserved3</td>
<td>16</td>
<td>4</td>
<td>Questo campo è obbligatorio e i relativi contenuti sono riservati.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#766-firstcluster-field">sezione 7.6.6</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#767-datalength-field">sezione 7.6.7</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="761-entrytype-field"></a>Campo 7.6.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1](#641-entrytype-field).

##### <a name="7611-typecode-field"></a>Campo TypeCode 7.6.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.1](#6411-typecode-field).

Per la voce della directory dell'estensione del flusso, il valore valido per questo campo è 0.

##### <a name="7612-typeimportance-field"></a>Campo 7.6.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.2](#6412-typeimportance-field).

Per la voce della directory dell'estensione del flusso, il valore valido per questo campo è 0.

##### <a name="7613-typecategory-field"></a>Campo 7.6.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.3](#6413-typecategory-field).

##### <a name="7614-inuse-field"></a>Campo 7.6.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.4](#6414-inuse-field).

#### <a name="762-generalsecondaryflags-field"></a>Campo 7.6.2 GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere la [sezione 6.4.2](#642-generalsecondaryflags-field)) e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7621-allocationpossible-field"></a>Campo 7.6.2.1 AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.1](#6421-allocationpossible-field).

Per la voce della directory dell'estensione del flusso, il valore valido per questo campo è 1.

##### <a name="7622-nofatchain-field"></a>Campo 7.6.2.2 NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.2](#6422-nofatchain-field).

#### <a name="763-namelength-field"></a>Campo 7.6.3 NameLength

Il campo NameLength conterrà la lunghezza della stringa Unicode in cui sono contenute le voci di directory del nome file successive (vedere la [sezione 7,7](#77-file-name-directory-entry)) collettivamente.

L'intervallo valido di valori per questo campo sarà:

- Almeno 1, ovvero il nome file più breve possibile

- Al massimo 255, che è il nome file più lungo possibile

Il valore del campo NameLength influiscono anche sulle voci di directory del nome del file numerico (vedere la [sezione 7,7](#77-file-name-directory-entry)).

#### <a name="764-namehash-field"></a>Campo 7.6.4 NameHash

Il campo NameHash conterrà un hash a 2 byte (vedere la [Figura 4](#figure-4-namehash-computation)) del nome del file con maiuscole/minuscole. Questo consente alle implementazioni di eseguire un confronto rapido quando si cerca un file in base al nome. Un aspetto importante è che il NameHash fornisce una verifica della mancata corrispondenza. Le implementazioni devono verificare che tutte le corrispondenze di NameHash con un confronto tra il nome del file in questione.

<div id="figure-4-namehash-computation" />

**Figura 4 calcolo NameHash**

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

#### <a name="765-validdatalength-field"></a>Campo 7.6.5 ValidDataLength

Il campo ValidDataLength descrive la distanza di scrittura dei dati utente del flusso di dati. Le implementazioni devono aggiornare questo campo Man mano che scrivono i dati nel flusso di dati. Sul supporto di archiviazione i dati tra la lunghezza dei dati valida e la lunghezza dei dati del flusso di dati non sono definiti. Le implementazioni devono restituire zeri per le operazioni di lettura oltre la lunghezza dei dati valida.

Se la voce della directory di file corrispondente descrive una directory, l'unico valore valido per questo campo è uguale al valore del campo DATALENGTH. In caso contrario, l'intervallo di valori validi per questo campo sarà:

- Almeno 0, che indica che nessun dato utente è stato scritto nel flusso di dati

- Al massimo DATALENGTH, che indica che i dati utente sono stati scritti nell'intera lunghezza del flusso di dati

#### <a name="766-firstcluster-field"></a>Campo 7.6.6 FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.3](#643-firstcluster-field).

Questo campo deve contenere l'indice del primo cluster del flusso di dati che ospita i dati utente.

#### <a name="767-datalength-field"></a>7.6.7-campo DataLength

Il campo DATALENGTH deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.4](#644-datalength-field).

Se la voce della directory di file corrispondente descrive una directory, il valore valido per questo campo è l'intera dimensione dell'allocazione associata, in byte, che può essere 0. Per le directory, inoltre, il valore massimo per questo campo è 256 MB.

### <a name="77-file-name-directory-entry"></a>7,7 voce directory nome file

Le voci di directory del nome file sono voci di directory secondarie critiche nei set di voci di directory di file (vedere la [tabella 34](#table-34-file-name-directoryentry)). Il numero valido di voci della directory dei nomi di file in un set di voci della directory di file è NameLength/15, arrotondato per eccesso al numero intero più vicino. Inoltre, le voci di directory dei nomi di file sono valide solo se seguono immediatamente la voce della directory dell'estensione di flusso come serie consecutiva. Le voci di directory del nome file si combinano per formare il nome file per il set di voci della directory di file.

Tutti gli elementi figlio di una determinata voce di directory avranno set di voci di directory di nomi file univoci. In altre parole, è possibile che non esistano nomi di file o directory duplicati dopo l'uso di maiuscole e minuscole in una directory.

<div id="table-34-file-name-directoryentry" />

**Tabella 34 nome file DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#771-entrytype-field">sezione 7.7.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#772-generalsecondaryflags-field">sezione 7.7.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>FileName</td>
<td>2</td>
<td>30</td>
<td>Questo campo è obbligatorio e la <a href="#773-filename-field">sezione 7.7.3</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="771-entrytype-field"></a>Campo 7.7.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1](#641-entrytype-field).

##### <a name="7711-typecode-field"></a>Campo TypeCode 7.7.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.1](#6411-typecode-field).

Per la voce della directory dell'estensione del flusso, il valore valido per questo campo è 1.

##### <a name="7712-typeimportance-field"></a>Campo 7.7.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.2](#6412-typeimportance-field).

Per la voce della directory dell'estensione del flusso, il valore valido per questo campo è 0.

##### <a name="7713-typecategory-field"></a>Campo 7.7.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.3](#6413-typecategory-field).

##### <a name="7714-inuse-field"></a>Campo 7.7.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.4](#6414-inuse-field).

#### <a name="772-generalsecondaryflags-field"></a>Campo 7.7.2 GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere la [sezione 6.4.2](#642-generalsecondaryflags-field)) e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7721-allocationpossible-field"></a>Campo 7.7.2.1 AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.1](#6421-allocationpossible-field).

Per la voce della directory dell'estensione del flusso, il valore valido per questo campo è 0.

##### <a name="7722-nofatchain-field"></a>Campo 7.7.2.2 NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.2](#6422-nofatchain-field).

#### <a name="773-filename-field"></a>Campo 7.7.3 FileName

Il campo FileName deve contenere una stringa Unicode, che è una parte del nome file. Nelle voci di directory del nome del file dell'ordine esistono in un set di voci di directory di file, i campi FileName vengono concatenati per formare il nome file per il set di voci della directory di file. Data la lunghezza del campo FileName, 15 caratteri e il numero massimo di voci di directory dei nomi file, 17, la lunghezza massima del nome file concatenato finale è
255.

Il nome del file concatenato ha lo stesso set di caratteri non validi di altri file System basati su FAT (vedere la [tabella 35](#table-35-invalid-filename-characters)). Le implementazioni devono impostare i caratteri inutilizzati dei campi FileName sul valore 0000h.

<div id="table-35-invalid-filename-characters" />

**Tabella 35 caratteri di nome file non validi**

| **Codice carattere** | **Descrizione** | **Codice carattere** | **Descrizione**   | **Codice carattere** | **Descrizione** |
|--------------------|-----------------|--------------------|-------------------|--------------------|-----------------|
| 0000h              | Codice di controllo    | 0001H              | Codice di controllo      | 0002H              | Codice di controllo    |
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

I nomi file "." e ".." hanno il significato speciale "questa directory" e "directory contenitore", rispettivamente. Le implementazioni non devono registrare uno di questi nomi di file riservati nel campo FileName.
Tuttavia, le implementazioni possono generare questi due nomi file nelle visualizzazioni directory per fare riferimento alla directory elencata e alla directory che lo contiene.

Le implementazioni possono voler limitare i nomi di file e directory solo al set di caratteri ASCII. In tal caso, è necessario limitare l'utilizzo di caratteri all'intervallo di caratteri validi nelle prime 128 voci Unicode. Devono comunque archiviare i nomi di file e directory in Unicode nel volume e tradurli in/da ASCII/Unicode in caso di interazione con l'utente.

### <a name="78-vendor-extension-directory-entry"></a>Voce di directory dell'estensione del fornitore 7,8

La voce della directory di estensione del fornitore è una voce di directory secondaria benigna nei set di voci di directory di file (vedere la [tabella 36](#table-36-vendor-extension-directoryentry)). Un set di voci di directory di file può contenere un numero qualsiasi di voci di directory di estensione del fornitore, fino al limite di voci di directory secondarie, meno il numero di altre voci della directory secondaria. Inoltre, le voci di directory di estensione del fornitore sono valide solo se non precedono le voci della directory di estensione del flusso e dei nomi file richieste.

Le voci di directory di estensione del fornitore consentono ai fornitori di avere voci di directory specifiche del fornitore univoche nei singoli set di voci di directory di file tramite il campo VendorGuid (vedere la [tabella 36](#table-36-vendor-extension-directoryentry)). Le voci di directory univoche consentono ai fornitori di estendere il file system di exFAT. I fornitori possono definire il contenuto del campo VendorDefined (vedere la [tabella 36](#table-36-vendor-extension-directoryentry)). Le implementazioni dei fornitori possono mantenere il contenuto del campo VendorDefined e possono fornire funzionalità specifiche del fornitore.

Le implementazioni che non riconoscono il GUID di una voce di directory dell'estensione del fornitore considereranno la voce della directory uguale a qualsiasi altra voce di directory secondaria benigna non riconosciuta (vedere la [sezione 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-36-vendor-extension-directoryentry" />

**Tabella 36 estensione fornitore DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#781-entrytype-field">sezione 7.8.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#782-generalsecondaryflags-field">sezione 7.8.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Questo campo è obbligatorio e la <a href="#783-vendorguid-field">sezione 7.8.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>14</td>
<td>Questo campo è obbligatorio e i fornitori possono definirne il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="781-entrytype-field"></a>Campo 7.8.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1](#641-entrytype-field).

##### <a name="7811-typecode-field"></a>Campo TypeCode 7.8.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.1](#6411-typecode-field).

Per la voce della directory dell'estensione del fornitore, il valore valido per questo campo è 0.

##### <a name="7812-typeimportance-field"></a>Campo 7.8.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.2](#6412-typeimportance-field).

Per la voce della directory dell'estensione del fornitore, il valore valido per questo campo è 1.

##### <a name="7813-typecategory-field"></a>Campo 7.8.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.3](#6413-typecategory-field).

##### <a name="7814-inuse-field"></a>Campo 7.8.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.4](#6414-inuse-field).

#### <a name="782-generalsecondaryflags-field"></a>Campo 7.8.2 GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere la [sezione 6.4.2](#642-generalsecondaryflags-field)) e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7821-allocationpossible-field"></a>Campo 7.8.2.1 AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.1](#6421-allocationpossible-field).

Per la voce della directory dell'estensione del fornitore, il valore valido per questo campo è 0.

##### <a name="7822-nofatchain-field"></a>Campo 7.8.2.2 NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.2](#6422-nofatchain-field).

#### <a name="783-vendorguid-field"></a>Campo 7.8.3 VendorGuid

Il campo VendorGuid deve contenere un GUID che identifica in modo univoco l'estensione del fornitore specificata.

Tutti i valori possibili per questo campo sono validi, ad eccezione del GUID null, ovvero {00000000-0000-0000-0000-000000000000} . Tuttavia, i fornitori devono usare uno strumento di generazione GUID, ad esempio GuidGen.exe, per selezionare un GUID durante la definizione delle estensioni.

Il valore di questo campo determina la struttura specifica del fornitore del campo VendorDefined.

### <a name="79-vendor-allocation-directory-entry"></a>7,9 voce di directory di allocazione fornitore

La voce della directory di allocazione del fornitore è una voce di directory secondaria benigna nei set di voci di directory di file (vedere la [tabella 37](#table-37-vendor-allocation-directoryentry)). Un set di voci della directory di file può contenere un numero qualsiasi di voci di directory di allocazione del fornitore, fino al limite di voci della directory secondaria, minore il numero di altre voci della directory secondaria. Inoltre, le voci di directory di allocazione del fornitore sono valide solo se non precedono le voci della directory di estensione del flusso e dei nomi file richieste.

Le voci di directory di allocazione del fornitore consentono ai fornitori di avere voci di directory specifiche del fornitore univoche nei singoli set di voci di directory di file tramite il campo VendorGuid (vedere la [tabella 37](#table-37-vendor-allocation-directoryentry)). Le voci di directory univoche consentono ai fornitori di estendere il file system di exFAT. I fornitori possono definire il contenuto dei cluster associati, se presenti. Le implementazioni del fornitore possono mantenere il contenuto dei cluster associati, se presente, e possono fornire funzionalità specifiche del fornitore.

Le implementazioni che non riconoscono il GUID di una voce di directory di allocazione del fornitore devono considerare la voce di directory come qualsiasi altra voce di directory secondaria benigna non riconosciuta (vedere la [sezione 8,2](#82-implications-of-unrecognized-directory-entries)).

<div id="table-37-vendor-allocation-directoryentry" />

**Tabella 37 allocazione fornitore DirectoryEntry**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EntryType</td>
<td>0</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#791-entrytype-field">sezione 7.9.1</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>GeneralSecondaryFlags</td>
<td>1</td>
<td>1</td>
<td>Questo campo è obbligatorio e la <a href="#792-generalsecondaryflags-field">sezione 7.9.2</a> ne definisce il contenuto.</td>
</tr>
<tr class="odd">
<td>VendorGuid</td>
<td>2</td>
<td>16</td>
<td>Questo campo è obbligatorio e la <a href="#793-vendorguid-field">sezione 7.9.3</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>VendorDefined</td>
<td>18</td>
<td>2</td>
<td>Questo campo è obbligatorio e i fornitori possono definirne il contenuto.</td>
</tr>
<tr class="odd">
<td>FirstCluster</td>
<td>20</td>
<td>4</td>
<td>Questo campo è obbligatorio e la <a href="#794-firstcluster-field">sezione 7.9.4</a> ne definisce il contenuto.</td>
</tr>
<tr class="even">
<td>Lunghezza dati</td>
<td>24</td>
<td>8</td>
<td>Questo campo è obbligatorio e la <a href="#795-datalength-field">sezione 7.9.5</a> ne definisce il contenuto.</td>
</tr>
</tbody>
</table>

#### <a name="791-entrytype-field"></a>Campo 7.9.1 EntryType

Il campo EntryType deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1](#641-entrytype-field).

##### <a name="7911-typecode-field"></a>Campo TypeCode 7.9.1.1

Il campo TypeCode deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.1](#6411-typecode-field).

Per la voce della directory di allocazione del fornitore, il valore valido per questo campo è 1.

##### <a name="7912-typeimportance-field"></a>Campo 7.9.1.2 TypeImportance

Il campo TypeImportance deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.2](#6412-typeimportance-field).

Per la voce della directory di allocazione del fornitore, il valore valido per questo campo è 1.

##### <a name="7913-typecategory-field"></a>Campo 7.9.1.3 TypeCategory

Il campo TypeCategory deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.3](#6413-typecategory-field).

##### <a name="7914-inuse-field"></a>Campo 7.9.1.4 InUse

Il campo InUse deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.1.4](#6414-inuse-field).

#### <a name="792-generalsecondaryflags-field"></a>Campo 7.9.2 GeneralSecondaryFlags

Il campo GeneralSecondaryFlags deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico (vedere la [sezione 6.4.2](#642-generalsecondaryflags-field)) e definisce il contenuto del campo CustomDefined da riservare.

##### <a name="7921-allocationpossible-field"></a>Campo 7.9.2.1 AllocationPossible

Il campo AllocationPossible deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.1](#6421-allocationpossible-field).

Per la voce della directory di allocazione del fornitore, il valore valido per questo campo è 1.

##### <a name="7922-nofatchain-field"></a>Campo 7.9.2.2 NoFatChain

Il campo NoFatChain deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.2.2](#6422-nofatchain-field).

#### <a name="793-vendorguid-field"></a>Campo 7.9.3 VendorGuid

Il campo VendorGuid deve contenere un GUID che identifica in modo univoco l'allocazione del fornitore specificata.

Tutti i valori possibili per questo campo sono validi, ad eccezione del GUID null, ovvero {00000000-0000-0000-0000-000000000000} . Tuttavia, i fornitori devono usare uno strumento di generazione GUID, ad esempio GuidGen.exe, per selezionare un GUID durante la definizione delle estensioni.

Il valore di questo campo determina la struttura specifica del fornitore del contenuto dei cluster associati, se presenti.

#### <a name="794-firstcluster-field"></a>Campo 7.9.4 FirstCluster

Il campo FirstCluster deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.3](#643-firstcluster-field).

#### <a name="795-datalength-field"></a>7.9.5-campo DataLength

Il campo DATALENGTH deve essere conforme alla definizione fornita nel modello DirectoryEntry secondario generico. vedere la [sezione 6.4.4](#644-datalength-field).

### <a name="710-texfat-padding-directory-entry"></a>7,10 voce della directory di riempimento TexFAT

Questa specifica, exFAT Revision 1,00 file System Basic Specification, non definisce la voce della directory di riempimento TexFAT. Tuttavia, il codice di tipo è 1 e l'importanza del tipo è 1. Le implementazioni di questa specifica considerano le voci della directory di riempimento TexFAT come qualsiasi altra voce di directory primaria benigna non riconosciuta, le implementazioni non devono spostare le voci di directory di TexFAT Padding.

## <a name="8-implementation-notes"></a>8 Note sull'implementazione

### <a name="81-recommended-write-ordering"></a>8,1 ordine di scrittura consigliato

Le implementazioni devono garantire che il volume sia il più elastico possibile per l'alimentazione di errori e altri guasti inevitabili. Quando si creano nuove voci di directory o si modificano le allocazioni del cluster, le implementazioni dovrebbero in genere seguire questo ordine di scrittura:

1. Impostare il valore del campo VolumeDirty su 1

2. Aggiornare il FAT attivo, se necessario

3. Aggiornare la bitmap di allocazione attiva

4. Crea o aggiorna la voce della directory, se necessario

5. Cancellare il valore del campo VolumeDirty in 0, se il relativo valore prima del primo passaggio era 0

Quando si eliminano voci di directory o si liberano allocazioni cluster, le implementazioni devono seguire questo ordine di scrittura:

1. Impostare il valore del campo VolumeDirty su 1

2. Eliminare o aggiornare la voce della directory, se necessario

3. Aggiornare il FAT attivo, se necessario

4. Aggiornare la bitmap di allocazione attiva

5. Cancellare il valore del campo VolumeDirty in 0, se il relativo valore prima del primo passaggio era 0

### <a name="82-implications-of-unrecognized-directory-entries"></a>8,2 conseguenze delle voci di directory non riconosciute

Le specifiche exFAT future dello stesso numero di revisione principale, 1 e numero di revisione secondaria maggiore di 0, possono definire nuove voci di directory secondarie primarie benigne e secondarie critiche. Solo le specifiche exFAT di un numero di revisione principale superiore possono definire nuove voci di directory primarie critiche. Le implementazioni di questa specifica, exFAT Revision 1,00 file System Basic Specification, devono poter montare e accedere a qualsiasi volume exFAT di revisione principale 1 e qualsiasi numero di revisione secondaria. Sono presenti scenari in cui un'implementazione può rilevare voci di directory che non riconoscono. Di seguito vengono descritte le implicazioni di questi scenari:

1. La presenza di voci di directory primarie critiche non riconosciute nella directory radice esegue il rendering del volume non valido. La presenza di qualsiasi voce di directory primaria critica, ad eccezione delle voci di directory di file, in una directory non radice, rende non valida la directory di hosting.

2. Le implementazioni non devono modificare le voci di directory primarie benigne non riconosciute o le relative allocazioni cluster associate. Tuttavia, quando si elimina una directory e solo quando si elimina una directory, le implementazioni elimineranno le voci di directory primarie benigne non riconosciute e libereranno tutte le allocazioni del cluster associate, se presenti.

3. Le implementazioni non devono modificare le voci di directory secondarie critiche non riconosciute o le allocazioni cluster associate. La presenza di una o più voci di directory secondarie critiche non riconosciute in un set di voci di directory esegue il rendering dell'intero set di voci di directory non riconosciuto. Quando si elimina un set di voci di directory che contiene una o più voci di directory secondarie critiche non riconosciute, le implementazioni devono liberare tutte le allocazioni del cluster, se presenti, associate a voci di directory secondarie critiche non riconosciute.
   Inoltre, se il set di voci di directory descrive una directory, le implementazioni possono:

   - Attraversare la directory

   - Enumerare le voci di directory in esso contenute

   - Elimina voci di directory contenute

   - Spostare le voci di directory contenute in una directory diversa

   Tuttavia, le implementazioni non devono:

   - Modificare le voci di directory contenute, eccetto Delete, come indicato

   - Crea nuove voci di directory contenute

   - Apre le voci di directory contenute, ad eccezione di attraversamento ed enumerazione, come indicato

4. Le implementazioni non devono modificare le voci di directory secondarie benigne non riconosciute o le relative allocazioni cluster associate.
   Le implementazioni devono ignorare le voci di directory secondarie benigne non riconosciute. Quando si elimina un set di voci di directory, le implementazioni devono liberare tutte le allocazioni del cluster, se presenti, associate a voci di directory secondarie benigne non riconosciute.

## <a name="9-file-system-limits"></a>9 limiti del file System

### <a name="91-sector-size-limits"></a>Limiti delle dimensioni del settore 9,1

Il campo BytesPerSectorShift definisce i limiti inferiore e superiore delle dimensioni del settore (che restituisce il **limite inferiore: 512 byte; limite massimo: 4.096 byte**).

### <a name="92-cluster-size-limits"></a>Limiti delle dimensioni del cluster 9,2

Il campo SectorsPerClusterShift definisce i limiti di dimensioni inferiori e superiori del cluster (**limite inferiore: 1 settore; limite superiore: 25--settori BytesPerSectorShift**, che restituiscono 32 MB).

### <a name="93-cluster-heap-size-limits"></a>Limiti delle dimensioni dell'heap del cluster 9,3

L'heap del cluster deve contenere almeno abbastanza spazio per ospitare le seguenti strutture di base file system: la directory radice, tutte le bitmap di allocazione e la tabella del case.

Il limite inferiore delle dimensioni dell'heap del cluster è una funzione del limite di dimensioni inferiori di ogni struttura di base file system che risiede nell'heap del cluster. Anche in base al più piccolo cluster possibile (512 byte), ogni struttura di base file system non richiede più di un cluster. Il **limite inferiore è quindi: 2 + cluster NumberOfFats**, che restituisce 3 o 4 cluster, a seconda del valore del campo NumberOfFats.

Il limite superiore per le dimensioni dell'heap del cluster è una semplice funzione del numero massimo possibile di cluster, definito dal campo Clustercount-(**limite superiore: 2 Cluster <sup>32</sup>-11**). Indipendentemente dalle dimensioni del cluster, tale heap cluster dispone di spazio sufficiente per ospitare almeno le strutture di base file system.

### <a name="94-volume-size-limits"></a>Limiti di dimensioni del volume 9,4

Il campo VolumeLength definisce i limiti di dimensioni inferiori e superiori del volume (limite inferiore: **2 settori <sup>BytesPerSectorShift</sup><sup>20</sup>/2**, che restituiscono 1 MB; **limite superiore: 2 settori <sup>64</sup>-1**, che, date le dimensioni massime possibili del settore, restituiscono approssimativamente 64ZB. Tuttavia, questa specifica consiglia non più di 2 cluster<sup>24</sup>-2 nell'heap del cluster. vedere la [sezione 3.1.9](#319-clustercount-field). Il limite superiore consigliato di un volume è quindi: ClusterHeapOffset + (2<sup>24</sup>-2) \* 2<sup>SectorsPerClusterShift</sup>. Data la dimensione massima possibile del cluster, 32 MB e presupponendo che ClusterHeapOffset sia 96MB (spazio sufficiente per le aree di avvio principale e di backup e solo il primo FAT), il limite superiore consigliato di un volume restituisce approssimativamente 512TB.

### <a name="95-directory-size-limits"></a>9,5 limiti delle dimensioni della directory

Il campo DATALENGTH della voce della directory dell'estensione di flusso definisce i limiti della dimensione inferiore e superiore (**limite inferiore: 0 byte; limite massimo: 256 MB**). Ciò significa che una directory può ospitare fino a 8.388.608 voci di directory (ogni voce di directory utilizza 32 byte). Dato il più piccolo possibile set di voci di directory di file, tre voci di directory, una directory può ospitare fino a 2.796.202 file.

## <a name="10-appendix"></a>10 Appendice

### <a name="101-globally-unique-identifiers-guids"></a>10,1 identificatori univoci globali (GUID)

Un GUID è l'implementazione Microsoft di un identificatore univoco universale. Un GUID è un valore a 128 bit costituito da un gruppo di 8 cifre esadecimali, seguite da tre gruppi di 4 cifre esadecimali ciascuna e seguita da un gruppo di 12 cifre esadecimali, ad esempio {6B29FC40-CA47-1067-B31D-00DD010662DA} (vedere la [tabella 38](#table-38-guid-structure)).

<div id="table-38-guid-structure" />

**Tabella 38 GUID struttura**

<table>
<thead>
<tr class="header">
<th><strong>Nome campo</strong></th>
<th><p><strong>Offset</strong></p>
<p><strong>byte</strong></p></th>
<th><p><strong>Dimensioni</strong></p>
<p><strong>byte</strong></p></th>
<th><strong>Commenti</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Data1</td>
<td>0</td>
<td>4</td>
<td>Questo campo è obbligatorio e contiene i quattro byte dal primo gruppo del GUID (6B29FC40h dall'esempio).</td>
</tr>
<tr class="even">
<td>Data2</td>
<td>4</td>
<td>2</td>
<td>Questo campo è obbligatorio e contiene i due byte dal secondo gruppo del GUID (CA47h dall'esempio).</td>
</tr>
<tr class="odd">
<td>Data3</td>
<td>6</td>
<td>2</td>
<td>Questo campo è obbligatorio e contiene i due byte del terzo gruppo del GUID (1067h dall'esempio).</td>
</tr>
<tr class="even">
<td>DATA4 [0]</td>
<td>8</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il byte più significativo del quarto gruppo del GUID (B3H dall'esempio).</td>
</tr>
<tr class="odd">
<td>DATA4 [1]</td>
<td>9</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il byte meno significativo del quarto gruppo del GUID (1Dh dall'esempio).</td>
</tr>
<tr class="even">
<td>DATA4 [2]</td>
<td>10</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il primo byte del quinto gruppo del GUID (00h dell'esempio).</td>
</tr>
<tr class="odd">
<td>DATA4 [3]</td>
<td>11</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il secondo byte del quinto gruppo del GUID (DDh dall'esempio).</td>
</tr>
<tr class="even">
<td>DATA4 [4]</td>
<td>12</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il terzo byte del quinto gruppo del GUID (01h dall'esempio).</td>
</tr>
<tr class="odd">
<td>DATA4 [5]</td>
<td>13</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il quarto byte del quinto gruppo del GUID (06h dall'esempio).</td>
</tr>
<tr class="even">
<td>DATA4 [6]</td>
<td>14</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il quinto byte del quinto gruppo del GUID (62H dall'esempio).</td>
</tr>
<tr class="odd">
<td>DATA4 [7]</td>
<td>15</td>
<td>1</td>
<td>Questo campo è obbligatorio e contiene il sesto byte del quinto gruppo del GUID (DAh dell'esempio).</td>
</tr>
</tbody>
</table>

### <a name="102-partition-tables"></a>10,2 tabelle delle partizioni

Per garantire l'interoperabilità dei volumi exFAT in un'ampia gamma di scenari di utilizzo, le implementazioni devono usare il tipo di partizione 07h per l'archiviazione partizionata MBR e il GUID della partizione {EBD0A0A2-B9E5-4433-87C0-68B6B72699C7} per l'archiviazione partizionata GPT.

## <a name="11-documentation-change-history"></a>11 cronologia modifiche documentazione

La tabella 39 descrive la cronologia delle versioni di, le correzioni a, le aggiunte a, le rimozioni da e i chiarimenti di questo documento.

<div id="table-39-documentation-change-history" />

**Tabella 39 cronologia modifiche documentazione**

<table>
<thead>
<tr class="header">
<th><strong>Data</strong></th>
<th><strong>Descrizione della modifica</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>08-Jan-2008</td>
<td><p>Primo rilascio della specifica di base, che include:</p>
<blockquote>
<p>Sezione 1, introduzione</p>
<p>Sezione 2,<br />
Struttura del volume</p>
<p>Sezione 3, principali e aree di avvio di backup</p>
<p>Sezione 4, area della tabella di allocazione file</p>
<p>Sezione 5, area dati</p>
<p>Sezione 6, struttura di directory</p>
<p>Sezione 7, definizioni di voci di directory</p>
<p>Sezione 8, Note sull'implementazione</p>
<p>Sezione 9, limiti del file System</p>
<p>Sezione 10, appendice</p>
</blockquote></td>
</tr>
<tr class="even">
<td>08-giu-2008</td>
<td><p>Seconda versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Aggiunta della sezione 11,<br />
Cronologia modifiche documentazione</p>
<p>Aggiunta delle voci dell'estensione del fornitore e della directory di allocazione del fornitore nelle sezioni 7,8 e 7,9</p>
<p>Aggiunta della tabella dei casi di completamento consigliata nelle sezioni 7.2.5 e 7.2.5.1</p>
<p>Aggiunta dei campi UtcOffset nella sezione 7,4 e aggiunta dell'acronimo UTC nella sezione 1,3</p>
<p>Correzione della dimensione del campo CustomDefined nella tabella 19</p>
<p>Correzione dell'intervallo valido di valori NameLength nella sezione 7.6.3</p>
<p>Correzione e chiarimento dei campi timestamp e 10msIncrement nella sezione 7,4</p>
<p>Chiarimento della struttura dei parametri null nella sezione 3,3</p>
<p>Chiarimento del significato dei valori del campo NoFatChain nella sezione 6.3.4.2</p>
<p>Chiarimento del significato dei valori del campo DATALENGTH nella sezione 6.2.3</p>
<p>Chiarimento del campo VolumeDirty nella sezione 3.1.13.2 e dell'ordine di scrittura consigliato nella sezione 8,1</p>
<p>Chiarimento del campo MediaFailure nella sezione 3.1.13.3</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>01-ott-2008</td>
<td><p>Terza versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Spiegazione dei campi da aggiungere a</p>
<p>Aggiunta della definizione UTC nella tabella 2 sezione 1,3</p>
<p>Sezioni modificate 1,5, per garantire l'allineamento con il documento di specifica TexFAT.</p>
<p>È stata chiarita la restrizione che solo Microsoft può definire il layout delle voci di directory nella sezione 6,2</p>
<p>Aggiunto il chiarimento che il campo FirstCluster deve essere zero se DATALENGTH è zero e NoFatChain è impostato su Section 6.3.5 e Section 6.4.3</p>
<p>Requisiti chiariti per le voci di directory di file valide nella sezione 7,4</p>
<p>Aggiunto il requisito per i nomi di file e directory univoci alla sezione 7,7</p>
<p>Aggiunta nota di implementazione per ASCII alla fine della sezione 7.7.3</p>
</blockquote></td>
</tr>
<tr class="even">
<td>01-Jan-2009</td>
<td><p>Quarta versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Rimossi riferimenti a Windows CE voci di controllo di accesso</p>
<p>Aggiunta di chiarimenti alla sezione 7.2.5.1 per richiedere in modo esplicito una tabella del case completa</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>02-Sep-2009</td>
<td><p>Quinta versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Modificare la formattazione del documento per consentire una migliore conversione PDF</p>
</blockquote></td>
</tr>
<tr class="even">
<td>24-feb-2010</td>
<td><p>Sesta versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Istruzione non corretta modificata: "il campo FirstCluster deve essere zero se DATALENGTH è zero e NoFatChain è impostato" nella sezione 6.3.5 e la sezione 6.4.3 su "Se il bit NoFatChain è 1, FirstCluster deve puntare a un cluster valido nell'heap del cluster" per chiarire che deve essere presente un'allocazione valida se il bit NoFatChain è impostato.</p>
<p>Aggiunta di "Se il bit NoFatChain è 1, DATALENGTH non deve essere zero. Se il campo FirstCluster è zero, DATALENGTH deve anche essere zero "per la sezione 6.3.6 e la sezione 6.4.4 per chiarire che deve essere presente un'allocazione valida se è impostato il bit NoFatChain.</p>
<p>Avviso di copyright aggiornato a 2010</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>26-Aug-2019</td>
<td><p>Settima versione della specifica di base, che include le modifiche seguenti:</p>
<blockquote>
<p>Termini legali aggiornati relativi alla specifica, tra cui:</p>
<p>Rimozione dell'avviso Microsoft confidential</p>
<p>Rimozione della sezione del contratto di licenza per la documentazione tecnica di Microsoft Corporation</p>
<p>Avviso di copyright aggiornato a 2019</p>
</blockquote></td>
</tr>
</tbody>
</table>
