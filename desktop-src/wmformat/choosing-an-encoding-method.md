---
title: Scelta di un metodo di codifica
description: Scelta di un metodo di codifica
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- profili, scelta dei metodi di codifica
- profili, metodi di codifica
- codec, scelta di metodi di codifica
- codec, metodi di codifica
- profili, selezione dei metodi di codifica
- codec, selezione di metodi di codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298147"
---
# <a name="choosing-an-encoding-method"></a>Scelta di un metodo di codifica

Alcuni codec, come il codec Windows Media Video 9, supportano più metodi di codifica. Il metodo di codifica scelto per un flusso dipende dal modo in cui deve essere recapitato il flusso. Nella tabella seguente viene descritto quando utilizzare i vari metodi di codifica.



| Metodo di codifica                | Descrizione                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocità in bit costante (CBR) a 1 pass | L'unica opzione per lo streaming live. Codifica a una velocità in bit prevedibile e offre la qualità più bassa di tutti i metodi di codifica.                                                                    |
| 2-pass CBR                     | Utilizzare per i file che verranno trasmessi in rete a un lettore client, ma che non vengono trasmessi da un'origine live. Codifica a una velocità in bit prevedibile, ma con una qualità migliore rispetto a 1-pass CBR. |
| Velocità in bit della variabile 1-pass (VBR) | Usare quando è necessario specificare la qualità dell'output codificato. Offre la qualità più uniforme di tutti i metodi di codifica. Usare solo per i file locali o per il download.                        |
| 2-pass VBR-non vincolato     | Usare quando è necessario specificare una larghezza di banda, ma le fluttuazioni intorno alla larghezza di banda specificata sono accettabili. Per i file locali o solo per il download.                                                    |
| 2-pass VBR-vincolato       | Utilizzare le stesse circostanze come non vincolate, ma quando è necessario specificare una frequenza di bit momentanea massima. Per i file locali o solo per il download.                                                |



 

Nella tabella seguente sono elencati i metodi di codifica supportati dai codec forniti con Windows Media Format SDK.



| Codec                                  | CBR | 2-pass CBR | VBR | 2-pass VBR |
|----------------------------------------|-----|------------|-----|------------|
| Windows Media Video 9                  | X   | X          | X   | X          |
| Windows Media Audio 9 e versioni successive        | X   | X          | X   | X          |
| Schermata Windows Media Video 9           | X   |            | X   |            |
| Windows Media Audio 9 Voice            | X   |            |     |            |
| Windows Media Audio Professional       | X   | X          | X   | X          |
| Windows Media Audio senza perdita di perdite           |     |            | X   |            |
| Windows Media Video 9 Image e versioni successive  | X   |            | X   |            |
| Profilo avanzato Windows Media Video 9 | X   | X          | X   | X          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Progettazione di profili**](designing-profiles.md)
</dt> <dt>

[**Codifica della velocità in bit costante (CBR)**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**Codifica a due passaggi**](two-pass-encoding.md)
</dt> <dt>

[**Codifica della velocità in bit variabile (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




