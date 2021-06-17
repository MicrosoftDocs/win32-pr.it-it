---
title: Attributi (Windows Media Format 11 SDK)
description: Informazioni sugli attributi in Windows Media Format 11 SDK. Un attributo è un singolo elemento di metadati.
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK,attributi
- Advanced Systems Format (ASF), attributi
- ASF (Advanced Systems Format), attributi
- attributi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262193"
---
# <a name="attributes-windows-media-format-11-sdk"></a>Attributi (Windows Media Format 11 SDK)

Un attributo è un singolo elemento di metadati. La maggior parte degli attributi può essere impostata dall'applicazione e viene scritta nell'intestazione di un file ASF.

Alcuni degli attributi predefiniti sono attributi codificati. Questi attributi non vengono archiviati nell'intestazione di un file ASF, ma vengono calcolati dagli oggetti di Windows Media Format SDK quando il file viene caricato. Poiché gli attributi codificati vengono sempre calcolati, sono intrinsecamente di sola lettura.

Questo SDK include molte definizioni di attributo che è possibile usare. È anche possibile creare attributi personalizzati per descrivere il contenuto.

Le sezioni seguenti descrivono gli attributi predefiniti.



| Sezione                                                                | Descrizione                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Elenco degli attributi](attribute-list.md)                                   | Fornisce un elenco alfabetico di tutti gli attributi predefiniti. Dopo l'elenco, ogni attributo viene descritto singolarmente.                                                                          |
| [Attributi con più valori](attributes-with-multiple-values.md) | Elenca gli attributi che possono essere aggiunti a un file più di una volta.                                                                                                                                      |
| [Attributi per tipo](attributes-by-type.md)                           | Contiene elenchi di attributi ordinati in base al tipo. Tra questi sono inclusi elenchi di attributi di utilizzo speciale (ad esempio quelli che gestiscono digital rights management) e gli elenchi di attributi suggeriti in base al tipo di contenuto. |
| [Supporto tag ID3](id3-tag-support.md)                                 | Elenca gli attributi compatibili con i tag ID3.                                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMHeaderInfo::GetAttributeByIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




