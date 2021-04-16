---
title: Impostazione delle estensioni delle unità dati
description: Impostazione delle estensioni delle unità dati
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- estensioni unità dati, impostazione
- flussi, estensioni di unità dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516663"
---
# <a name="setting-data-unit-extensions"></a>Impostazione delle estensioni delle unità dati

Alcuni flussi sono configurati per l'uso di estensioni di unità dati per associare dati supplementari a singoli esempi. Per ulteriori informazioni sugli esempi estesi, vedere [estensioni di unità dati](data-unit-extensions.md).

Per la maggior parte dei sistemi di estensione dell'unità dati è necessaria un'estensione per ogni esempio nel flusso. Se non si specifica un'estensione della dimensione corretta, il writer rifiuterà l'esempio.

Per aggiungere dati estesi a un esempio, usare il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Per ottenere informazioni sulle estensioni dell'unità dati configurate in un flusso, è possibile usare i metodi [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) e [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di estensioni delle unità dati**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




