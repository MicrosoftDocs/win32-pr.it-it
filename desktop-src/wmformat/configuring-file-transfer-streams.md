---
title: Configurazione di flussi di trasferimento di file
description: Configurazione di flussi di trasferimento di file
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- flussi, configurazione di flussi di trasferimento di file
- codec, configurazione di flussi di trasferimento di file
- flussi di trasferimento di file
- flussi, estensioni di unità dati
- codec, estensioni di unità dati
- estensioni unità dati, flussi di trasferimento file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046345"
---
# <a name="configuring-file-transfer-streams"></a>Configurazione di flussi di trasferimento di file

Per i flussi di trasferimento di file non è necessaria alcuna impostazione speciale nella struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Per l'associazione di un nome file a ogni esempio, è necessario disporre di un'estensione di unità dati. Per inviare un nome con esempi di trasferimento di file, è necessario implementare un sistema di estensione dell'unità dati per il flusso.

Per impostare un'estensione di unità dati per il flusso, seguire questa procedura:

1.  Ottenere un puntatore all'interfaccia [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.
2.  Aggiungere un'estensione per le unità dati per il flusso chiamando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) come indicato di seguito:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flussi di file**](file-streams.md)
</dt> </dl>

 

 




