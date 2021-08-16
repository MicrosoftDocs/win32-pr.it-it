---
title: Impostazione delle estensioni unità dati
description: Impostazione delle estensioni unità dati
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- Advanced Systems Format (ASF), estensioni unità dati
- ASF (Advanced Systems Format),estensioni unità dati
- estensioni di unità dati, impostazione
- flussi, estensioni di unità dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1bb88e9aa0c3bc00d4c21a1c262b7ff4a44fbc2f426f139b3b782a0bbdb7b83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197483"
---
# <a name="setting-data-unit-extensions"></a>Impostazione delle estensioni unità dati

Alcuni flussi sono configurati per l'uso di estensioni di unità dati per associare dati supplementari a singoli esempi. Per altre informazioni sugli esempi estesi, vedere [Estensioni unità dati](data-unit-extensions.md).

La maggior parte dei sistemi di estensione per unità dati richiede un'estensione per ogni campione nel flusso. Se non si specifica un'estensione delle dimensioni corrette, il writer rifiuterà l'esempio.

Per aggiungere dati estesi a un esempio, usare il [**metodo INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) È possibile ottenere informazioni sulle estensioni delle unità dati configurate in un flusso usando i metodi [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) e [**IWMStreamConfig2::GetDataUnitExtension.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di estensioni delle unità dati**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




