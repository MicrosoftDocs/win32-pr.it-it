---
title: Per ottenere le statistiche del writer
description: Per ottenere le statistiche del writer
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF), statistiche writer
- ASF (Advanced Systems Format),statistiche writer
- statistiche del writer, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cedd96f1e94b8d3c9499fe08e3eeebb2100e866b141b756483cfb07bb7cb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083966"
---
# <a name="to-get-writer-statistics"></a>Per ottenere le statistiche del writer

Il writer può fornire informazioni statistiche sulle operazioni di scrittura. Esistono due metodi per raccogliere le statistiche del writer: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) e [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). Le informazioni recuperate **da GetStatisticsEx** sono più specifiche delle informazioni recuperate da **GetStatistics.**

Entrambi i metodi popolano le strutture con informazioni statistiche. **GetStatistics** usa la [**struttura WM WRITER \_ \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) e **GetStatisticsEx** usa la [**struttura WM WRITER STATISTICS \_ \_ \_ EX.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) **GetStatisticsEx** non duplica i dati ottenuti **da GetStatistics.** Per le informazioni più complete, è necessario chiamare entrambi i metodi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interfaccia IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




