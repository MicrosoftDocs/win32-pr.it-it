---
title: Uso della condivisione della larghezza di banda
description: Uso della condivisione della larghezza di banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows MEDIA Format SDK, condivisione della larghezza di banda
- condivisione della larghezza di banda, informazioni
- profili, condivisione della larghezza di banda
- flussi, condivisione della larghezza di banda
- condivisione della larghezza di banda, interfaccia IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7259ddf441a4e32eb7eb4aea19a52d633c6aacd3a27ad6d392e4fea41c3f4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845157"
---
# <a name="using-bandwidth-sharing"></a>Uso della condivisione della larghezza di banda

È possibile usare oggetti di condivisione della larghezza di banda per specificare che determinati flussi, se combinati, non useranno più larghezza di banda di quella specificata. Le informazioni in un oggetto di condivisione della larghezza di banda non vengono generate o verificate dal writer né usate dal lettore per alcun elemento.

Quando viene scritto un file con informazioni sulla condivisione della larghezza di banda nel profilo, i dati vengono archiviati nella relativa sezione di intestazione. È possibile usare [**l'interfaccia IWMProfile**](iwmprofile.md) nel lettore per verificare la presenza di informazioni sulla condivisione della larghezza di banda quando viene riprodotto il file.

Ogni oggetto di condivisione della larghezza di banda è definito da due impostazioni. Il primo è la larghezza di banda, come definito da una larghezza di banda e da una finestra del buffer. La seconda impostazione è un tipo di condivisione della larghezza di banda, che può essere esclusivo o parziale. La condivisione esclusiva della larghezza di banda significa che i flussi costitutivi vengono riprodotti uno alla volta, mentre parziale significa che i flussi vengono recapitati contemporaneamente.

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

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




