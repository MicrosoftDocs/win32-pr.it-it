---
title: Formati di dati e supporti di trasferimento
description: Formati di dati e supporti di trasferimento
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104047583"
---
# <a name="data-formats-and-transfer-media"></a>Formati di dati e supporti di trasferimento

La maggior parte delle piattaforme, tra cui Windows, definisce un protocollo standard per il trasferimento dei dati tra le applicazioni, in base a un set di funzioni denominate Appunti. Le applicazioni che usano queste funzioni possono condividere dati anche se i loro formati di dati nativi sono molto diversi. In genere, questi appunti presentano due carenze significative che COM ha superato.

Per prima cosa, le descrizioni dei dati usano solo un identificatore di formato, ad esempio l'identificatore di formato degli Appunti a 16 bit per Windows, il che significa che gli Appunti possono descrivere solo la struttura dei propri dati, ovvero l'ordine dei bit. Può segnalare, "Ho una bitmap" "o ho del testo", ma non è possibile specificare i dispositivi di destinazione per i quali i dati sono composti, le visualizzazioni o gli aspetti che possono fornire i dati o i supporti di archiviazione più adatti per il trasferimento. Ad esempio, non può segnalare "Ho una stringa di testo archiviata nella memoria globale e formattata per la presentazione sullo schermo o su una stampante" oppure "Ho una bitmap di sketch di anteprima visualizzata per una stampante a matrice di punti dpi 100 e archiviata come file su disco".

In secondo luogo, tutti i trasferimenti di dati tramite gli appunti si verificano generalmente tramite la memoria globale. L'uso della memoria globale è ragionevolmente efficiente per piccole quantità di dati, ma terribilmente inefficiente per grandi quantità, ad esempio un oggetto multimediale da 20 MB. La memoria globale è lenta per un oggetto dati di grandi dimensioni, la cui dimensione richiede un notevole scambio nella memoria virtuale su disco. Nei casi in cui i dati scambiati risiedono principalmente su disco, l'utilizzo forzato di questo collo di bottiglia della memoria virtuale è estremamente inefficiente. Un modo migliore è ignorare completamente la memoria globale e trasferire semplicemente i dati direttamente sul disco.

Per risolvere questi problemi, COM fornisce due strutture di dati: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1). Per altre informazioni, vedere i seguenti argomenti:

-   [Struttura FORMATETC](the-formatetc-structure.md)
-   [Struttura STGMEDIUM](the-stgmedium-structure.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

 




