---
title: Condivisione della larghezza di banda
description: Condivisione della larghezza di banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media Format SDK, condivisione della larghezza di banda
- ASF (Advanced Systems Format), condivisione della larghezza di banda
- ASF (formato avanzato dei sistemi), condivisione della larghezza di banda
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- condivisione della larghezza di banda, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046328"
---
# <a name="bandwidth-sharing"></a>Condivisione della larghezza di banda

È possibile specificare i flussi in un file che, quando vengono riuniti, utilizzare una larghezza di banda inferiore rispetto alla somma delle frequenze di bit dichiarate combinate. Specificando la condivisione della larghezza di banda nel profilo, è necessario chiarire alla lettura delle applicazioni che la larghezza di banda disponibile necessaria per trasmettere il file non è quella che potrebbe sembrare.

Nessuno degli oggetti di Windows Media Format SDK modifica il comportamento in risposta alle informazioni di condivisione della larghezza di banda, fornito esclusivamente in modo da consentire la lettura delle applicazioni quando si determina se un file può essere riprodotto con un recapito limitato della larghezza di banda.

La condivisione della larghezza di banda è configurata con un oggetto di condivisione della larghezza di banda e viene aggiunta a un profilo prima di iniziare a scrivere un file

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Oggetto di condivisione della larghezza di banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Interfaccia IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**Interfaccia IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Uso della condivisione della larghezza di banda**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




