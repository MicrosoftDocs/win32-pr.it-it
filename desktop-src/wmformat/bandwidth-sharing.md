---
title: Condivisione della larghezza di banda
description: Condivisione della larghezza di banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows MEDIA Format SDK, condivisione della larghezza di banda
- Advanced Systems Format (ASF), condivisione della larghezza di banda
- ASF (Advanced Systems Format),bandwidth sharing
- Windows MEDIA Format SDK, flussi
- Advanced Systems Format (ASF), flussi
- ASF (Advanced Systems Format), flussi
- condivisione della larghezza di banda, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b01ff94e82f2ce3609a93278fef30c68e1a59445eea22f68f4b0a5d92371a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709411"
---
# <a name="bandwidth-sharing"></a>Condivisione della larghezza di banda

È possibile specificare i flussi in un file che, se combinati, usano una larghezza di banda inferiore rispetto alla somma delle velocità in bit dichiarate combinate. Specificando la condivisione della larghezza di banda nel profilo, si chiarisce alla lettura delle applicazioni che la larghezza di banda disponibile necessaria per trasmettere il file non è ciò che potrebbe sembrare altrimenti.

Nessuno degli oggetti di Windows Media Format SDK modifica il comportamento in risposta alle informazioni sulla condivisione della larghezza di banda, che vengono fornite esclusivamente in modo che la lettura delle applicazioni possa prenderne in considerazione quando si determina se un file può essere riprodotto con una distribuzione limitata della larghezza di banda.

La condivisione della larghezza di banda è configurata con un oggetto di condivisione della larghezza di banda e viene aggiunta a un profilo prima di iniziare a scrivere un file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Oggetto Bandwidth Sharing**](bandwidth-sharing-object.md)
</dt> <dt>

[**Interfaccia IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**Interfaccia IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Uso della condivisione della larghezza di banda**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




