---
title: Assegnazione di priorità al flusso
description: Assegnazione di priorità al flusso
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, assegnazione di priorità al flusso
- ASF (Advanced Systems Format), assegnazione di priorità ai flussi
- ASF (formato avanzato dei sistemi), assegnazione di priorità ai flussi
- Windows Media Format SDK, ordine di priorità per i flussi
- ASF (Advanced Systems Format), ordine di priorità per i flussi
- ASF (Advanced Systems Format), ordine di priorità per i flussi
- flussi, priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046324"
---
# <a name="stream-prioritization"></a>Assegnazione di priorità al flusso

Quando si crea un file ASF, è possibile specificare un ordine di priorità per i flussi costitutivi. Se si esegue il flusso di un file con priorità e la larghezza di banda disponibile non è sufficiente per la distribuzione di tutti i flussi, il lettore eliminerà i flussi in ordine di priorità inverso. In questo modo è possibile garantire che i flussi più importanti nel file non verranno eliminati a causa di problemi di rete.

La definizione delle priorità del flusso viene configurata con un oggetto di assegnazione di priorità del flusso e aggiunta al profilo. Un profilo può contenere un solo oggetto di assegnazione di priorità del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
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

[**Uso della priorità di flusso**](using-stream-prioritization.md)
</dt> </dl>

 

 




