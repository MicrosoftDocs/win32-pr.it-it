---
title: Per ottenere le statistiche del writer
description: Per ottenere le statistiche del writer
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- ASF (Advanced Systems Format), statistiche del writer
- ASF (formato avanzato dei sistemi), statistiche del writer
- Statistiche writer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103956266"
---
# <a name="to-get-writer-statistics"></a>Per ottenere le statistiche del writer

Il writer può fornire informazioni statistiche sulle operazioni di scrittura. Esistono due metodi per raccogliere le statistiche del writer: [**IWMWriterAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) e [**IWMWriterAdvanced3:: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). Le informazioni recuperate da **GetStatisticsEx** sono più specifiche delle informazioni recuperate da **GetStatistics**.

Entrambi i metodi popolano le strutture con informazioni statistiche. **GetStatistics** usa la struttura delle [**\_ \_ statistiche del writer WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) , mentre **GetStatisticsEx** usa la struttura [**ex di WM \_ writer \_ Statistics \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) . **GetStatisticsEx** non duplica i dati ottenuti da **GetStatistics**. Per informazioni più complete, è necessario chiamare entrambi i metodi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interfaccia IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




