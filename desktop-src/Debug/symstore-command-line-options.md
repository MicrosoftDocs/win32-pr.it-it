---
description: Per le transazioni SymStore sono supportati i seguenti formati di sintassi. Il primo parametro deve essere sempre Add o CANC. L'ordine degli altri parametri non è rilevante.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: Opzioni Command-Line SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b69cdca9ee74cf01041375f26b2e151dc3ec5d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351946"
---
# <a name="symstore-command-line-options"></a>Opzioni Command-Line SymStore

Per le transazioni SymStore sono supportati i seguenti formati di sintassi. Il primo parametro deve essere sempre Add o CANC. L'ordine degli altri parametri non è rilevante.

**SymStore aggiungere** \[ **/l** **/o** **/p** **/r** **/Compress** \] \[ **-: msg** *Message* \] \[ **-: rel** \] \[ **-: norif** \] **/f** *file* **/s** *Store* **/t** *Product* \[ **/v** *versione* \] \[ **/c** *Comment* \] \[ **/d** *logfile*\]

**SymStore aggiungere** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **-: rel** \] \[ **-: norif** \] **/g** *share* **/f** *file* **/x** *IndexFile* \[ **/d** *logfile*\]

**SymStore aggiungere** \[ **/o** **/Compress** \] \[ **/p** \[ **-:** \| *messaggio* msg \] \[ **-: rel** \] \[ **-: norif** \] \] **/y** *IndexFile* **/g** *share* **/s** *Store* **/t** *prodotto* \[ **/v** *versione* \] \[ **/c** *Comment* \] \[ **/d** *logfile*\]

**query SymStore** \[ **/o** **/r** \] **/f** *file* **/s** *Store* \[ **/d** *logfile*\]

**SymStore del** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *filelogfile*\]

**SymStore** **/?**



| Parametro      | Significato                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Fa in modo che SymStore aggiunga nuove informazioni di indicizzazione a un file di indice esistente. Questa opzione viene usata solo con l'opzione/x.                                                                                                                                                                                                                                                                                 |
| *Commento* /c   | Specifica un commento per la transazione.                                                                                                                                                                                                                                                                                                                                                                     |
| /Compress      | Fa in modo che SymStore crei una versione compressa di ogni file copiato nell'archivio simboli anziché utilizzare una copia non compressa del file. Questa opzione è valida solo per l'archiviazione di file e non per i puntatori e non può essere usata con l'opzione/p.                                                                                                                                                              |
| /d *logfile*   | Specifica un file di log da utilizzare per l'output del comando. Se non è incluso, le informazioni sulle transazioni e altro output vengono inviate a stdout.                                                                                                                                                                                                                                                                     |
| /f ( *file* )      | Specifica uno o più percorsi di file (o directory) da aggiungere. Se un percorso di file specificato inizia con un simbolo "@", è previsto un [file di risposta](../midl/response-files.md) contenente un elenco di file da aggiungere (un percorso di file per riga).                                                                                                                                             |
| *condivisione* /g     | Specifica il server e la condivisione in cui sono stati originariamente archiviati i file di simboli. Se usato con/f, la *condivisione* deve essere identica all'inizio dell'identificatore di *file* . Se utilizzata con/y, la *condivisione* deve essere il percorso dei file di simboli originali (non il file di indice). In questo modo è possibile modificare in seguito questa parte del percorso del file nel caso in cui i file di simboli vengano spostati in un server e in una condivisione diversi. |
| *ID* /i        | Specifica la stringa dell'ID di transazione.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Consente al file di trovarsi in una directory locale piuttosto che in un percorso di rete. Questa opzione viene usata solo con l'opzione/p.                                                                                                                                                                                                                                                                                        |
| /o             | Fa in modo che SymStore visualizzi l'output dettagliato.                                                                                                                                                                                                                                                                                                                                                                   |
| / p             | Fa in modo che SymStore memorizzi un puntatore nel file, anziché il file stesso.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Consente a SymStore di aggiungere file o directory in modo ricorsivo.                                                                                                                                                                                                                                                                                                                                                     |
| *Archivio* /s     | Specifica la directory radice per l'archivio dei simboli.                                                                                                                                                                                                                                                                                                                                                           |
| /t *prodotto*   | Specifica il nome del prodotto.                                                                                                                                                                                                                                                                                                                                                                           |
| *versione* /v   | Specifica la versione del prodotto.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *IndexFile* | Consente a SymStore di non archiviare i file di simboli effettivi. Al contrario, SymStore registra le informazioni nel *IndexFile* che consentiranno a SymStore di accedere ai file di simboli in un secondo momento.                                                                                                                                                                                                                         |
| *IndexFile* /y | Fa in modo che SymStore legga i dati da un file creato con/x.                                                                                                                                                                                                                                                                                                                                                |
| -: Messaggio MSG  | Aggiunge il messaggio specificato a ogni file. Questa opzione può essere usata solo quando si usa/p.                                                                                                                                                                                                                                                                                                                     |
| -: REL          | Consente ai percorsi nei puntatori del file di essere relativi. Questa opzione implica l'opzione/l. Questa opzione può essere usata solo quando si usa/p.                                                                                                                                                                                                                                                                     |
| -: NORIF       | Omette la creazione di file di puntatore di riferimento per i file e i puntatori archiviati. Questa opzione è valida solo durante la creazione iniziale di un archivio simboli se l'archivio da modificare è stato creato con questa opzione.                                                                                                                                                                                      |
| /?             | Visualizza il testo della Guida per il comando SymStore.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



