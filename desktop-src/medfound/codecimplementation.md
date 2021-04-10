---
description: Implementazione del codec.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Implementazione di codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201c0cb46fc61f117c9b45d059b102560986d5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878469"
---
# <a name="codec-implementation"></a>Implementazione di codec

I codec Windows Media Audio e video sono implementati come oggetti COM. Un codec viene in genere implementato come una coppia di oggetti COM: uno per il codificatore e uno per il decodificatore. Il codificatore ha un identificatore di classe (CLSID) e il decodificatore ha un CLSID diverso. Ad esempio, la parte del codificatore del codec Windows Media Audio 9 ha un CLSID rappresentato dalla costante **CLSID \_ CWMAEncMediaObject** e la parte del decodificatore dello stesso codec presenta un CLSID rappresentato dalla costante **CLSID \_ CWMADecMediaObject**.

In alcuni casi, più di un codificatore è incluso in un singolo oggetto COM. Ad esempio, il codificatore Windows Media Video 9 e il codificatore Windows Media Video 9,1 sono entrambi parte dello stesso oggetto COM. Di conseguenza, entrambi hanno lo stesso CLSID, rappresentato dalla costante **CLSID \_ CWMV9EncMediaObject**. Analogamente, alcuni oggetti COM includono più di un decodificatore.

Ogni oggetto codificatore o decodificatore espone l'interfaccia [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) e l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Per la maggior parte dei codificatori, indipendentemente dal fatto che si usi il codificatore come DMO o MFT, si usa lo stesso CLSID per creare un'istanza del codificatore. Per creare, ad esempio, un'istanza del codificatore Windows Media Video 9, usare **CLSID \_ CWMV9EncMediaObject**, indipendentemente dal fatto che si intenda usare il codificatore come DMO o MFT. Analogamente, per la maggior parte dei decodificatori ogni decodificatore ha un solo CLSID, indipendentemente dal fatto che si usi il decodificatore come DMO o MFT.

> [!Note]  
> Esistono alcune eccezioni all'istruzione precedente sull'uso di un solo CLSID per DMO e MFT. Ad esempio, il decodificatore MPEG-4 Part 2 ha un CLSID quando funge da DMO e un CLSID diverso quando funge da MFT.

 

Oltre alle interfacce di base, ogni oggetto codificatore o decodificatore implementa due interfacce simili per l'utilizzo delle proprietà del codec, **IPropertyBag** e **IPropertyStore**. Le versioni precedenti degli oggetti codificatore e decodificatore usavano **IPropertyBag**, che identifica ogni proprietà in base a un valore stringa contenente un nome di proprietà. **IPropertyStore** è un'interfaccia più recente che identifica le proprietà con un valore di chiave di proprietà univoco. È stato aggiunto il supporto per **IPropertyStore** per fornire supporto per MFTS. La maggior parte delle stringhe del nome di proprietà di **IPropertyBag** dispone di un GUID della chiave della proprietà **IPropertyStore** corrispondente e la maggior parte dei GUID ha una stringa del nome **IPropertyBag** corrispondente, con alcune eccezioni.

Questa documentazione elenca le proprietà in base alla costante della chiave della proprietà, ma ogni voce include la costante della stringa del nome di proprietà da usare con **IPropertyBag** quando appropriato.

## <a name="related-topics"></a>Argomenti correlati

[Codec Windows Media](windows-media-codecs.md)
