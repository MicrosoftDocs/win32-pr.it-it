---
title: Formati di dati e supporti di trasferimento
description: Formati di dati e supporti di trasferimento
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccbab96fbaca83330737521f253b3c625e67ea9a024d87d35276da2826a3964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501431"
---
# <a name="data-formats-and-transfer-media"></a>Formati di dati e supporti di trasferimento

La maggior parte delle piattaforme, Windows, definisce un protocollo standard per il trasferimento dei dati tra applicazioni, in base a un set di funzioni denominate Appunti. Le applicazioni che usano queste funzioni possono condividere i dati anche se i formati di dati nativi sono molto diversi. In genere, questi Appunti hanno due lacune significative che COM ha superato.

In primo luogo, le descrizioni dei dati usano solo un identificatore di formato, ad esempio l'identificatore di formato degli Appunti a 16 bit singolo in Windows, il che significa che gli Appunti possono descrivere solo la struttura dei dati, ovvero l'ordinamento dei bit. Può segnalare "Ho una bitmap" "o ho del testo", ma non può specificare i dispositivi di destinazione per cui sono composti i dati, quali visualizzazioni o aspetti di se stessi possono fornire i dati o quali supporti di archiviazione sono più adatti per il trasferimento. Ad esempio, non può segnalare "Ho una stringa di testo archiviata nella memoria globale e formattata per la presentazione sullo schermo o su una stampante" o "Ho una bitmap di sketch di anteprima di cui è stato eseguito il rendering per una stampante a matrice di punti da 100 dpi e archiviata come file su disco".

In secondo luogo, tutti i trasferimenti di dati che usano gli Appunti vengono in genere eseguiti tramite la memoria globale. L'uso della memoria globale è ragionevolmente efficiente per piccole quantità di dati, ma estremamente inefficiente per grandi quantità, ad esempio un oggetto multimediale di 20 MB. La memoria globale è lenta per un oggetto dati di grandi dimensioni, le cui dimensioni richiedono uno scambio notevole con la memoria virtuale su disco. Nei casi in cui i dati s scambiati risiederanno comunque principalmente su disco, forzarlo attraverso questo collo di bottiglia della memoria virtuale è altamente inefficiente. Un modo migliore sarebbe ignorare completamente la memoria globale e semplicemente trasferire i dati direttamente sul disco.

Per risolvere questi problemi, COM fornisce due strutture di dati: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Per altre informazioni, vedere i seguenti argomenti:

-   [Struttura FORMATETC](the-formatetc-structure.md)
-   [Struttura STGMEDIUM](the-stgmedium-structure.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

 




