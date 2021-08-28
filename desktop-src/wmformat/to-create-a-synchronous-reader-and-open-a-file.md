---
title: Per creare un lettore sincrono e aprire un file
description: Per creare un lettore sincrono e aprire un file
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF), creazione di lettori
- ASF (Advanced Systems Format), creazione di lettori
- Advanced Systems Format (ASF), apertura di file
- ASF (Advanced Systems Format), apertura di file
- lettori sincroni, creazione
- lettori sincroni,apertura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d1c6897c05bb0d843e5818f078df5235a5afac4a485d6a719ab86b8e4f8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807651"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Per creare un lettore sincrono e aprire un file

Prima di poter eseguire qualsiasi operazione con il lettore sincrono, è necessario creare un oggetto lettore sincrono e caricare un file per la lettura. Per inizializzare il lettore sincrono e aprire un file, seguire questa procedura.

1.  Creare un oggetto lettore sincrono chiamando la [**funzione WMCreateSyncReader.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) È necessario specificare il livello desiderato di Rights Management per il nuovo oggetto lettore. Le modalità disponibili sono elencate nel tipo **di enumerazione WMT \_ RIGHTS.**
2.  Specificare un file da leggere chiamando [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

Il lettore sincrono supporta anche l'uso dell'interfaccia COM **IStream** per l'apertura di file. È possibile implementare **l'interfaccia IStream** in qualsiasi modo. Dopo aver aperto il file desiderato in **IStream,** è possibile seguire i passaggi elencati in precedenza, ad eccezione del fatto che è necessario chiamare [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) anziché **IWMSyncReader::Open** nel passaggio 2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




