---
title: Priorità del flusso
description: Priorità del flusso
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows MEDIA Format SDK, definizione della priorità dei flussi
- Advanced Systems Format (ASF), priorità del flusso
- ASF (Advanced Systems Format), priorità del flusso
- Windows Media Format SDK, ordine di priorità per i flussi
- Advanced Systems Format (ASF), ordine di priorità per i flussi
- ASF (Advanced Systems Format), ordine di priorità per i flussi
- flussi, assegnazione di priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd34bab6a7957d7cbcdf97a78fc3d8be1f663d43ef1eb1ec8d4c575571ad0a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197277"
---
# <a name="stream-prioritization"></a>Priorità del flusso

Quando si crea un file ASF, è possibile specificare un ordine di priorità per i flussi costitutivi. Se si trasmettere un file con priorità e la larghezza di banda disponibile non è sufficiente per recapitare tutti i flussi, il lettore elimina i flussi in ordine di priorità inverso. In questo modo è possibile garantire che i flussi più importanti nel file non verranno eliminati a causa di problemi di rete.

La priorità del flusso viene configurata con un oggetto di definizione delle priorità del flusso e aggiunta al profilo. Un profilo può contenere un solo oggetto di priorità del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3::RemoveStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**Interfaccia IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Uso della priorità del flusso**](using-stream-prioritization.md)
</dt> </dl>

 

 




