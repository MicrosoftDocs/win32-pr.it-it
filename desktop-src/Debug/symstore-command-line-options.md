---
description: Le forme di sintassi seguenti sono supportate per le transazioni SymStore. Il primo parametro deve essere sempre add o del. L'ordine degli altri parametri non è importante.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: Opzioni Command-Line SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc166ab82fc40ad11eb9b014a003dc793f3bb7cc1d70792370bd175c68802417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572981"
---
# <a name="symstore-command-line-options"></a>Opzioni Command-Line SymStore

Le forme di sintassi seguenti sono supportate per le transazioni SymStore. Il primo parametro deve essere sempre add o del. L'ordine degli altri parametri non è importante.

**symstore add** \[ **/l** **/o** **/p** **/r /compress**  \] \[ **-:MSG** *Message* \] \[ **-:REL** \] \[ **-:NOREFS** \] **/f** *File* **/s** *Store* **/t** *Product* \[ **/v** *Version* \] \[ **/c** *Comment* \] \[ **/d** *LogFile*\]

**symstore add** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **-:REL -:NOREFS** \] \[  \] **/g** *Condivisione* **/f** *File* **/x** *IndexFile* \[ **/d** *LogFile*\]

**symstore add** \[ **/o** **/compress** \] \[ **/p** \[ **-:MSG** \| *Message* \] \[ **-:REL** \] \[ **-:NOREFS** \] \] **/y** *IndexFile* /g *Share* **/s** *Store* **/t** *Product*  \[ **/v** *Version* \] \[ **/c** *Comment* \] \[ **/d** *LogFile*\]

**Query di symstore** \[ **/o** **/r** \] **/f** *File* **/s** *Archivia* \[ **/d** *LogFile*\]

**symstore del** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *LogFile*\]

**symstore** **/?**



| Parametro      | Significato                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Fa sì che SymStore accoda nuove informazioni di indicizzazione a un file di indice esistente. Questa opzione viene usata solo con l'opzione /x.                                                                                                                                                                                                                                                                                 |
| /c *Commento*   | Specifica un commento per la transazione.                                                                                                                                                                                                                                                                                                                                                                     |
| /compress      | Fa in modo che SymStore crei una versione compressa di ogni file copiato nell'archivio simboli anziché usare una copia non compressa del file. Questa opzione è valida solo quando si archiviano file e non i puntatori e non può essere usata con l'opzione /p.                                                                                                                                                              |
| /d *LogFile*   | Specifica un file di log da utilizzare per l'output del comando. Se non è incluso, le informazioni sulla transazione e altri output vengono inviati a stdout.                                                                                                                                                                                                                                                                     |
| /f *File*      | Specifica uno o più percorsi di file (o directory) da aggiungere. Se un percorso di file specificato inizia con un simbolo '@', è previsto un [file](../midl/response-files.md) di risposta contenente un elenco di file da aggiungere (un percorso file per riga).                                                                                                                                             |
| /g *Condivisione*     | Specifica il server e la condivisione in cui sono stati originariamente archiviati i file di simboli. Se usato con /f, *Share* deve essere identico all'inizio dell'identificatore *File.* Se usato con /y, *Condivisione* deve essere il percorso dei file di simboli originali (non il file di indice). In questo modo è possibile modificare questa parte del percorso del file in un secondo momento nel caso in cui si spostino i file di simboli in un server e in una condivisione diversi. |
| /i *ID*        | Specifica la stringa dell'ID transazione.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Consente al file di essere in una directory locale anziché in un percorso di rete. Questa opzione viene usata solo con l'opzione /p.                                                                                                                                                                                                                                                                                        |
| /o             | Fa in modo che SymStore visualizza l'output dettagliato.                                                                                                                                                                                                                                                                                                                                                                   |
| / p             | Fa in modo che SymStore archivi un puntatore al file anziché al file stesso.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Determina l'aggiunta ricorsiva di file o directory da parte di SymStore.                                                                                                                                                                                                                                                                                                                                                     |
| /s *Store*     | Specifica la directory radice per l'archivio simboli.                                                                                                                                                                                                                                                                                                                                                           |
| /t *Prodotto*   | Specifica il nome del prodotto.                                                                                                                                                                                                                                                                                                                                                                           |
| /v *Versione*   | Specifica la versione del prodotto.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *IndexFile* | Fa in modo che SymStore non archivi i file di simboli effettivi. SymStore registra invece le informazioni in *IndexFile* che consentiranno a SymStore di accedere ai file di simboli in un secondo momento.                                                                                                                                                                                                                         |
| /y *IndexFile* | Fa in modo che SymStore letta i dati da un file creato con /x.                                                                                                                                                                                                                                                                                                                                                |
| -:MSG Message  | Aggiunge l'oggetto Message specificato a ogni file. Questa opzione può essere usata solo quando si usa /p.                                                                                                                                                                                                                                                                                                                     |
| -:REL          | Consente ai percorsi nei puntatori di file di essere relativi. Questa opzione implica l'opzione /l. Questa opzione può essere usata solo quando si usa /p.                                                                                                                                                                                                                                                                     |
| -:NOREFS       | Omette la creazione di file puntatore di riferimento per i file e i puntatori archiviati. Questa opzione è valida solo durante la creazione iniziale di un archivio simboli se l'archivio da modificare è stato creato con questa opzione.                                                                                                                                                                                      |
| /?             | Visualizza il testo della Guida per il comando SymStore.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



