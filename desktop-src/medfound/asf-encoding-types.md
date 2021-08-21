---
description: Tipi di codifica ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipi di codifica ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83e1b9f39118cea5e7c5610b9480ea3d615a002d7f889933e3f3e7d62f0b53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035579"
---
# <a name="asf-encoding-types"></a>Tipi di codifica ASF

I metodi di codifica sono tutti incentrati sul buffer usato dal codificatore per gestire i dati di input non compressi. Questo buffer è definito dalla velocità in bit del flusso, in bit al secondo, e dalla finestra del buffer, in millisecondi. Quando si esegue la codifica in file ASF, Windows codificatori multimediali rispettano i vincoli del buffer. Per altre informazioni sulla finestra del buffer, vedere [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md). Sapere come e quando usare ogni metodo può aiutare a creare contenuto compresso di alta qualità. La tabella seguente contiene collegamenti ad argomenti su ognuno dei metodi di codifica disponibili che un'applicazione può usare per codificare i dati multimediali in ASF.



| Metodo di codifica                                                                                      | Descrizione                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codifica a velocità in bit costante](constant-bit-rate-encoding.md)                                         | Il codificatore comprime i dati a una velocità in bit specificata.                                                                                                                                                     |
| [Codifica della velocità in bit variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md)       | Il codificatore comprime i dati in un particolare valore di qualità in modo che la qualità del supporto codificato sia coerente per tutta la durata, indipendentemente dai requisiti del buffer del flusso risultante. |
| [Codifica a velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | Il codificatore comprime i dati alla massima qualità possibile mantenendo una velocità in bit specificata. Questa modalità è detta anche codifica VBR (Variable Bit Rate) a 2 passi.                                    |
| [Codifica della velocità in bit della variabile vincolata di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | Il codificatore comprime i dati a una velocità in bit specificata mantenendo i valori del buffer nella finestra del buffer massima e nella velocità in bit specificate. Questa modalità è detta anche VBR di picco a 2 passi.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 



