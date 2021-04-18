---
title: Per creare un reader sincrono e aprire un file
description: Per creare un reader sincrono e aprire un file
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- ASF (Advanced Systems Format), creazione di Reader
- ASF (formato avanzato dei sistemi), creazione di Reader
- ASF (Advanced Systems Format), apertura di file
- ASF (Advanced Systems Format), apertura di file
- lettori sincroni, creazione
- lettori sincroni, apertura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299515"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Per creare un reader sincrono e aprire un file

Prima di poter eseguire qualsiasi operazione con il lettore sincrono, sarà necessario creare un oggetto Reader sincrono e caricare un file per la lettura. Per inizializzare il lettore sincrono e aprire un file, seguire questa procedura.

1.  Creare un oggetto Reader sincrono chiamando la funzione [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) . È necessario specificare il livello desiderato di Rights Management per il nuovo oggetto Reader. Le modalità disponibili sono elencate nel tipo di enumerazione **WMT \_ Rights** .
2.  Specificare un file da leggere chiamando [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

Il lettore sincrono supporta inoltre l'utilizzo dell'interfaccia com **IStream** per l'apertura di file. È possibile implementare l'interfaccia **IStream** come desiderato. Una volta aperto il file desiderato in **IStream**, è possibile seguire la procedura sopra indicata, ad eccezione del fatto che è necessario chiamare [**IWMSyncReader:: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) anziché **IWMSyncReader:: Open** nel passaggio 2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




