---
description: Tipi di codifica ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipi di codifica ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128007"
---
# <a name="asf-encoding-types"></a>Tipi di codifica ASF

I metodi di codifica si concentrano tutti sul buffer utilizzato dal codificatore per gestire i dati di input non compressi. Questo buffer è definito dalla velocità in bit del flusso, in bit al secondo e dalla finestra del buffer, in millisecondi. Quando si esegue la codifica nei file ASF, i codificatori Windows Media rispettano i vincoli del buffer. Per ulteriori informazioni sulla finestra buffer, vedere [il modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md). Sapere come e quando usare ogni metodo può essere utile per creare contenuti compressi di alta qualità. La tabella seguente contiene collegamenti ad argomenti su ognuno dei metodi di codifica disponibili che un'applicazione può usare per codificare i dati multimediali in ASF.



| Metodo di codifica                                                                                      | Descrizione                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codifica della velocità in bit costante](constant-bit-rate-encoding.md)                                         | Il codificatore comprime i dati a una velocità in bit specificata.                                                                                                                                                     |
| [Codifica della velocità in bit della variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md)       | Il codificatore comprime i dati in un particolare valore di qualità, in modo che la qualità del supporto codificato sia coerente per tutta la sua durata, indipendentemente dai requisiti del buffer del flusso risultante. |
| [Codifica della velocità in bit variabile non vincolata](unconstrained-variable-bit-rate--vbr--encoding.md)       | Il codificatore comprime i dati alla massima qualità possibile mantenendo una velocità in bit specificata. Questa modalità è detta anche codifica con velocità in bit variabile (VBR) a 2 passaggi.                                    |
| [Codifica della velocità in bit a variabili con vincoli di picco](peak-constrained-variable-bit-rate--vbr--encoding.md) | Il codificatore comprime i dati in base a una velocità in bit specificata mantenendo i valori del buffer nella finestra del buffer massima specificata e nella velocità in bit. Questa modalità viene chiamata anche 2-pass di picco VBR.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Codificatori Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



