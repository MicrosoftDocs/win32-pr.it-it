---
title: Oggetto buffer
description: Oggetto buffer
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media Format SDK, oggetti buffer
- ASF (Advanced Systems Format), oggetti buffer
- ASF (formato avanzato dei sistemi), oggetti buffer
- oggetti, oggetti buffer
- oggetti buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299505"
---
# <a name="buffer-object"></a>Oggetto buffer

Un oggetto buffer viene usato per conservare gli esempi e distribuirli tra gli oggetti di Windows Media Format SDK e l'applicazione. Quando si scrive un file, si passano gli esempi di input al writer usando oggetti buffer. Quando si legge un file, l'oggetto Reader o l'oggetto Reader sincrono fornisce esempi all'applicazione negli oggetti buffer.

Per la scrittura di esempi in un file, è possibile creare un oggetto buffer usando il metodo [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) . Per la lettura di esempi, l'oggetto Reader e l'oggetto Reader sincrono creano entrambi oggetti buffer internamente. Se si sceglie di, è possibile allocare oggetti buffer personalizzati per la lettura dei file tramite [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) o [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).

Le interfacce seguenti sono supportate da ogni oggetto buffer.



| Interfaccia                          | Descrizione                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | Controlla e fornisce l'accesso al buffer.                          |
| [**INSSBuffer2**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | Non implementato.                                                     |
| [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | Supporta le proprietà del buffer, utilizzate per le estensioni di unità dati. |
| [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | Enumera le proprietà del buffer.                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> </dl>

 

 




