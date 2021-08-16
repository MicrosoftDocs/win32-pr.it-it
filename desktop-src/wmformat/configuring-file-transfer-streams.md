---
title: Configurazione del trasferimento file Flussi
description: Configurazione del trasferimento file Flussi
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- flussi, configurazione di flussi di trasferimento file
- codec, configurazione di flussi di trasferimento file
- flussi di trasferimento di file
- flussi, estensioni di unità dati
- codec, estensioni di unità dati
- estensioni di unità dati, flussi di trasferimento di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0be95c9760a02275e223f56785149f6867d4aaf2462d07d158991b3cd21c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849064"
---
# <a name="configuring-file-transfer-streams"></a>Configurazione del trasferimento file Flussi

I flussi di trasferimento file non richiedono impostazioni speciali nella [**struttura WM \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) È necessaria un'estensione unità dati per associare un nome file a ogni esempio. Per inviare un nome con esempi di trasferimento di file, è necessario implementare un sistema di estensione unità dati per il flusso.

Per impostare un'estensione unità dati per il flusso, seguire questa procedura:

1.  Ottenere un puntatore [**all'interfaccia IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig::QueryInterface**.
2.  Aggiungere un'estensione unità dati per il flusso chiamando [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) come segue:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di tipi di flusso arbitrari**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**File Flussi**](file-streams.md)
</dt> </dl>

 

 




