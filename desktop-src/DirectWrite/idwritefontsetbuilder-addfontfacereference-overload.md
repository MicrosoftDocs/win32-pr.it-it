---
title: Metodi ADDFontFaceReference di IDWriteFontSetBuilder (Dwrite \_ 3.h)
description: Aggiunge un riferimento a un tipo di carattere al set da compilarsi.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Metodi AddFontFaceReference Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c9edfed7680b18ef9ffb271cb59de3a54d4b408ac5f194a7bead1bbb3fb9b2ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075581"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>Metodi IDWriteFontSetBuilder::AddFontFaceReference

Aggiunge un riferimento a un tipo di carattere al set da compilarsi.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference(IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Aggiunge un riferimento a un tipo di carattere al set da compilarsi. I metadati necessari verranno estratti automaticamente dal tipo di carattere quando si chiama CreateFontSet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference(IDWriteFontFaceReference, \* const DWRITE \_ FONT \_ \* PROPERTY, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Aggiunge un riferimento a un tipo di carattere al set da compilarsi. Il chiamante fornisce informazioni sufficienti per la ricerca, evitando la necessità di aprire il tipo di carattere potenzialmente non locale. Tutte le proprietà non fornite dal chiamante saranno mancanti e tali proprietà non saranno disponibili come filtri in GetMatchingFonts. GetPropertyValues per le proprietà mancanti restituirà un elenco di stringhe vuoto. Le proprietà passate devono in genere essere coerenti con il contenuto effettivo del tipo di carattere, ma non è necessario che lo siano. È possibile, ad esempio, creare un alias di un tipo di carattere usando un nome o un identificatore univoco diverso oppure impostare tag personalizzati non presenti nel tipo di carattere effettivo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dwrite \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
