---
description: Revoca del certificato OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revoca del certificato OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092729"
---
# <a name="opm-certificate-revocation"></a>Revoca del certificato OPM

Un certificato OPM (Output Protection Manager) può essere revocato da Microsoft. L'elenco di certificati revocati viene archiviato in un elenco di revoche globale. Il formato grl è il seguente:



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
<td>Struttura <a href="grl-header.md"><strong>GRL_HEADER</strong></a> corrente.</td>
</tr>
<tr class="even">
<td>Core</td>
<td>Contiene gli elenchi di revoche seguenti:
<ul>
<li>Revoche binarie del kernel</li>
<li>Revoche binarie in modalità utente</li>
<li>Revoche di certificati</li>
<li>Radici attendibili (riservate)</li>
</ul>
L'elenco di radici attendibili non viene attualmente usato ed è riservato per un uso futuro.</td>
</tr>
<tr class="odd">
<td>Voci estendibili</td>
<td>Contiene informazioni utilizzate da altri componenti. Questa sezione non è pertinente per OPM.</td>
</tr>
<tr class="even">
<td>Rinnovi:</td>
<td>Contiene GUID che definiscono Windows Update identificatori. Questa sezione contiene gli identificatori per gli elenchi seguenti:
<ul>
<li>Revoche binarie del kernel</li>
<li>Revoche binarie in modalità utente</li>
<li>Revoche di certificati</li>
</ul>
Un'applicazione può usare questi identificatori per richiedere una versione rinnovata di un file binario revocato, se disponibile.</td>
</tr>
<tr class="odd">
<td>Firma: sezione Core</td>
<td>Firma l'intestazione e le sezioni principali.</td>
</tr>
<tr class="even">
<td>Firma: sezione Estendibile</td>
<td>Firma l'intestazione e le sezioni estensibili.</td>
</tr>
</tbody>
</table>



 

L'intestazione GRL è una [**struttura GRL \_ HEADER.**](grl-header.md) Il **membro dwSequenceNumber** della struttura contiene il numero di versione GRL. Questo numero viene incrementato ogni volta che il grl viene aggiornato e una nuova versione inserita nel computer dell'utente.

I certificati OPM revocati sono elencati nell'elenco delle revoche di certificati della sezione Core. Ogni voce core nella grl è una matrice di 20 byte che contiene l'hash SHA-1 della chiave pubblica del certificato revocato.

Le sezioni Firma contengono firme che possono essere usate per verificare che l'grl non sia stato manomesso. Ogni sezione Signature contiene la [**struttura MF \_ SIGNATURE.**](mf-signature.md) La prima firma firma l'intestazione più la sezione Core. La seconda firma firma l'intestazione e la sezione Estendibile. questa firma non è pertinente per OPM.

Per assicurarsi che l'grl non sia stato manomesso, verificare la firma come segue:

1.  Trovare l'inizio della [**struttura MF \_ SIGNATURE.**](mf-signature.md) La posizione della **struttura MF \_ SIGNATURE** è specificata nel membro **cbSignatureCoreOffset** della [**struttura GRL \_ HEADER.**](grl-header.md) La posizione viene specificata come offset in byte dall'inizio dell'oggetto GRL.
2.  Analizzare la [**struttura MF \_ SIGNATURE**](mf-signature.md) come firma PKCS \# 7 con una catena di certificati.
3.  Verificare la catena di certificati fino a una radice attendibile.
4.  Verificare che il certificato foglia abbia l'identificatore di oggetto seguente nell'EKU: "1.3.6.1.4.1.311.10.5.4".
5.  Calcolare un hash dei byte che includono l'intestazione e le sezioni principali dell'oggetto GRL.
6.  Verificare che l'hash corrisponda alla firma nel certificato foglia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> <dt>

[**INTESTAZIONE \_ GRL**](grl-header.md)
</dt> <dt>

[**FIRMA \_ MF**](mf-signature.md)
</dt> </dl>

 

 



