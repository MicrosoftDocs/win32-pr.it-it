---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revoca del certificato OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527889"
---
# <a name="opm-certificate-revocation"></a>Revoca del certificato OPM

Un certificato di output Protection Manager (OPM) può essere revocato da Microsoft. L'elenco dei certificati revocati viene archiviato in un elenco di revoche globale (GRL). Il GRL ha il formato seguente:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sezione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Intestazione</td>
<td>Struttura <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</td>
</tr>
<tr class="even">
<td>Core</td>
<td>Contiene gli elenchi di revoche seguenti:
<ul>
<li>Revoche binarie del kernel</li>
<li>Revoche binarie in modalità utente</li>
<li>Revoche di certificati</li>
<li>Radici attendibili (riservato)</li>
</ul>
L'elenco di radici attendibili non viene attualmente utilizzato ed è riservato per un utilizzo futuro.</td>
</tr>
<tr class="odd">
<td>Voci estendibili</td>
<td>Contiene informazioni utilizzate da altri componenti. Questa sezione non è pertinente per OPM.</td>
</tr>
<tr class="even">
<td>Rinnovi</td>
<td>Contiene i GUID che definiscono gli identificatori di Windows Update. Questa sezione contiene gli identificatori per gli elenchi seguenti:
<ul>
<li>Revoche binarie del kernel</li>
<li>Revoche binarie in modalità utente</li>
<li>Revoche di certificati</li>
</ul>
Un'applicazione può usare questi identificatori per richiedere una versione rinnovata di un file binario revocato, se disponibile.</td>
</tr>
<tr class="odd">
<td>Firma: sezione principale</td>
<td>Firma l'intestazione e le sezioni principali.</td>
</tr>
<tr class="even">
<td>Firma: sezione estendibile</td>
<td>Firma l'intestazione e le sezioni estendibili.</td>
</tr>
</tbody>
</table>



 

L'intestazione GRL è una struttura di [**\_ intestazione GRL**](grl-header.md) . Il membro **dwSequenceNumber** della struttura contiene il numero di versione di GRL. Questo numero viene incrementato ogni volta che il GRL viene aggiornato e una nuova versione viene inserita nel computer dell'utente.

I certificati OPM revocati sono elencati nell'elenco revoche di certificati della sezione principale. Ogni voce principale in GRL è una matrice di 20 byte contenente l'hash SHA-1 della chiave pubblica del certificato revocato.

Le sezioni della firma contengono le firme che possono essere usate per verificare che il GRL non sia stato alterato. Ogni sezione della firma contiene la struttura della [**\_ firma AM MF**](mf-signature.md) . La prima firma firma l'intestazione più la sezione di base. La seconda firma firma l'intestazione più la sezione estendibile; Questa firma non è pertinente per OPM.

Per assicurarsi che il GRL stesso non sia stato alterato, verificare la firma come segue:

1.  Trovare l'inizio della struttura [**di \_ firma MF**](mf-signature.md) . Il percorso della struttura **di \_ firma MF** viene fornito nel membro **cbSignatureCoreOffset** della struttura dell' [**\_ intestazione GRL**](grl-header.md) . Il percorso viene specificato come offset in byte dall'inizio del GRL.
2.  Analizzare la struttura di [**\_ firma MF**](mf-signature.md) come una \# firma PKCS 7 con una catena di certificati.
3.  Verificare la catena di certificati fino a una radice attendibile.
4.  Verificare che il certificato foglia includa il seguente identificatore di oggetto nell'EKU: "1.3.6.1.4.1.311.10.5.4".
5.  Calcolare un hash dei byte che includono l'intestazione e le sezioni principali del GRL.
6.  Verificare che l'hash corrisponda alla firma nel certificato foglia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> <dt>

[**\_intestazione GRL**](grl-header.md)
</dt> <dt>

[**\_firma MF**](mf-signature.md)
</dt> </dl>

 

 



