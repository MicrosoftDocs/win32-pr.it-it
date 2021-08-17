---
title: HasAttachedImages
description: L'attributo HasAttachedImages è un attributo a livello di file che specifica se il file è un file MP3 con frame APIC ID3 allegati.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Formato multimediale Windows HasAttachedImages
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ec38d0961ffc6ffc50434cdecf69e6dde663dfeaff5e331455a9575b3426e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930861"
---
# <a name="hasattachedimages"></a>HasAttachedImages

**L'attributo HasAttachedImages** è un attributo a livello di file che specifica se il file è un file MP3 con frame APIC ID3 allegati.

## <a name="global-constant"></a>Costante globale

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>Tipo di dati

**TIPO WMT \_ \_ BOOL**

## <a name="remarks"></a>Commenti

Si tratta di un attributo codificato.

Questo attributo non può essere duplicato a livello di file. Se questo attributo viene usato per un singolo flusso, verrà considerato come metadati personalizzati e non trasmetterà il significato normale agli oggetti di Windows Media Format SDK.

**HasAttachedImages** è stato progettato per informare un'applicazione che le immagini erano presenti in modo da poterle recuperare usando [**l'interfaccia IWMImageInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) Ora che le immagini sono supportate usando [**l'attributo WM/Picture,**](wmpicture.md) **HasAttachedImages** non è più necessario.

Per determinare se un file contiene immagini, chiamare [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specificando **l'attributo WM/Picture.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




