---
description: Implementazione del codec.
ms.assetid: 5ec23f95-cc7d-4c16-979a-f1d2cc485bb0
title: Implementazione di codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1bb9c51788526d68b370dec782b433e6f8d7114ece2b4f5a735ef7662f869d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974860"
---
# <a name="codec-implementation"></a>Implementazione di codec

I Windows codec audio e video multimediali vengono implementati come oggetti COM. In genere, un codec viene implementato come coppia di oggetti COM: uno per il codificatore e uno per il decodificatore. Il codificatore ha un identificatore di classe (CLSID) e il decodificatore ha un CLSID diverso. Ad esempio, la parte del codificatore del codec Windows Media Audio 9 ha un CLSID rappresentato dalla costante **CLSID \_ CWMAEncMediaObject** e la parte del decodificatore dello stesso codec ha un CLSID rappresentato dalla costante **CLSID \_ CWMADecMediaObject**.

In alcuni casi, più di un codificatore è incluso in un singolo oggetto COM. Ad esempio, il codificatore Windows Media Video 9 e il codificatore Windows Media Video 9.1 fanno entrambi parte dello stesso oggetto COM. Di conseguenza, entrambi hanno lo stesso CLSID, rappresentato dalla costante **CLSID \_ CWMV9EncMediaObject**. Analogamente, alcuni oggetti COM includono più decodificatori.

Ogni oggetto codificatore o decodificatore espone [**l'interfaccia IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) in modo che l'oggetto possa essere usato come oggetto directx media (DMO) e [**l'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Per la maggior parte dei codificatori, indipendentemente dal fatto che si usi il codificatore come DMO o MFT, si usa lo stesso CLSID per creare un'istanza del codificatore. Ad esempio, per creare un'istanza del codificatore Windows Media Video 9, usare **CLSID \_ CWMV9EncMediaObject**, indipendentemente dal fatto che si intenda usare il codificatore come DMO o MFT. Analogamente, per la maggior parte dei decodificatori, ogni decodificatore ha un singolo CLSID indipendentemente dal fatto che si usi il decodificatore come DMO o MFT.

> [!Note]  
> Esistono alcune eccezioni all'istruzione precedente sull'uso di un singolo CLSID per il DMO mFT. Ad esempio, il decodificatore MPEG-4 Part 2 ha un CLSID quando funge da DMO e un CLSID diverso quando funge da MFT.

 

Oltre alle interfacce di base, ogni codificatore o oggetto decodificatore implementa due interfacce simili per l'uso delle proprietà del codec, **IPropertyBag** e **IPropertyStore.** Le versioni precedenti degli oggetti codificatore e decodificatore usano **IPropertyBag**, che identifica ogni proprietà in base a un valore stringa contenente un nome di proprietà. **IPropertyStore è** un'interfaccia più recente che identifica le proprietà con un valore univoco della chiave di proprietà. È stato **aggiunto il supporto per IPropertyStore** per fornire supporto per MFT. La maggior parte delle stringhe di nome della proprietà **IPropertyBag** ha un GUID della chiave di proprietà **IPropertyStore** corrispondente e la maggior parte dei GUID ha una stringa di nome **IPropertyBag** corrispondente, con alcune eccezioni.

Questa documentazione elenca le proprietà in base alla costante della chiave di proprietà, ma ogni voce include la costante stringa nome-proprietà da usare con **IPropertyBag** quando appropriato.

## <a name="related-topics"></a>Argomenti correlati

[Codec Windows Media](windows-media-codecs.md)
