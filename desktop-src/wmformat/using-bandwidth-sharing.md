---
title: Uso della condivisione della larghezza di banda
description: Uso della condivisione della larghezza di banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media Format SDK, condivisione della larghezza di banda
- condivisione della larghezza di banda, informazioni
- profili, condivisione della larghezza di banda
- flussi, condivisione della larghezza di banda
- condivisione della larghezza di banda, interfaccia IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398768"
---
# <a name="using-bandwidth-sharing"></a>Uso della condivisione della larghezza di banda

È possibile usare gli oggetti di condivisione della larghezza di banda per specificare che determinati flussi, quando combinati, non utilizzeranno più larghezza di banda di quanto specificato. Le informazioni in un oggetto di condivisione della larghezza di banda non vengono generate o verificate dal writer né utilizzate dal Reader per alcun elemento.

Quando viene scritto un file con informazioni sulla condivisione della larghezza di banda nel profilo, i dati vengono archiviati nella relativa sezione di intestazione. È possibile usare l'interfaccia [**IWMProfile**](iwmprofile.md) nel lettore per verificare le informazioni di condivisione della larghezza di banda quando il file viene riprodotto.

Ogni oggetto di condivisione della larghezza di banda viene definito da due impostazioni. Per prima cosa si intende la larghezza di banda, definita da una larghezza di banda e una finestra del buffer. La seconda impostazione è un tipo di condivisione della larghezza di banda, che può essere esclusivo o parziale. La condivisione esclusiva della larghezza di banda indica che i flussi costitutivi vengono riprodotti uno alla volta, mentre quello parziale indica che i flussi vengono recapitati contemporaneamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMProfile**](iwmprofile.md)
</dt> <dt>

[**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharingCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




