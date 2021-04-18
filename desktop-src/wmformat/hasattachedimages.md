---
title: HasAttachedImages
description: L'attributo HasAttachedImages è un attributo a livello di file che specifica se il file è un file MP3 con frame ID3 ad APIC collegati.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- HasAttachedImages Windows Media Format
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299411"
---
# <a name="hasattachedimages"></a>HasAttachedImages

L'attributo **HasAttachedImages** è un attributo a livello di file che specifica se il file è un file MP3 con frame ID3 ad APIC collegati.

## <a name="global-constant"></a>Costante globale

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>Tipo di dati

**\_tipo WMT \_ bool**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.

**HasAttachedImages** è stato progettato per informare un'applicazione che erano presenti immagini in modo che potessero essere recuperate usando l'interfaccia [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) . Ora che le immagini sono supportate usando l'attributo [**WM/Picture**](wmpicture.md) , **HasAttachedImages** non è più necessario.

Per determinare se un file contiene immagini, chiamare [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specificando l'attributo **WM/Picture** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




