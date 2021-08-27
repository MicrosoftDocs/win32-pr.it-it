---
description: Revoca di certificati OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revoca di certificati OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b4caeace94f852394081620555c0b5b04918bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478907"
---
# <a name="opm-certificate-revocation"></a>Revoca di certificati OPM

Un certificato OPM (Output Protection Manager) può essere revocato da Microsoft. L'elenco di certificati revocati viene archiviato in un elenco di revoche globale (GRL). Il formato GRL è il seguente:




| Sezione | Descrizione | 
|---------|-------------|
| Intestazione | Struttura <a href="grl-header.md"><strong>GRL_HEADER</strong></a> struttura . | 
| Core | Contiene gli elenchi di revoche seguenti:<ul><li>Revoche binarie del kernel</li><li>Revoche binarie in modalità utente</li><li>Revoche di certificati</li><li>Radici attendibili (riservate)</li></ul>L'elenco di radici attendibili non è attualmente usato ed è riservato per un uso futuro. | 
| Voci estendibili | Contiene informazioni usate da altri componenti. Questa sezione non è pertinente per OPM. | 
| Rinnovi: | Contiene GUID che definiscono gli identificatori Windows update. Questa sezione contiene gli identificatori per gli elenchi seguenti:<ul><li>Revoche binarie del kernel</li><li>Revoche binarie in modalità utente</li><li>Revoche di certificati</li></ul>Un'applicazione può usare questi identificatori per richiedere una versione rinnovata di un file binario revocato, se disponibile. | 
| Firma: sezione Core | Firma l'intestazione e le sezioni principali. | 
| Firma: sezione Estendibile | Firma l'intestazione e le sezioni estendibili. | 




 

L'intestazione GRL è una [**struttura GRL \_ HEADER.**](grl-header.md) Il **membro dwSequenceNumber** della struttura contiene il numero di versione GRL. Questo numero viene incrementato ogni volta che il grl viene aggiornato e una nuova versione inserita nel computer dell'utente.

I certificati OPM revocati sono elencati nell'elenco delle revoche di certificati della sezione Core. Ogni voce Core nella GRL è una matrice di 20 byte che contiene l'hash SHA-1 della chiave pubblica del certificato revocato.

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

 

 



