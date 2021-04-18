---
title: Metodi AddFontFaceReference di IDWriteFontSetBuilder (DWrite \_ 3. h)
description: Aggiunge un riferimento a un tipo di carattere al set da compilare.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Scrittura diretta metodi AddFontFaceReference
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330166"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a>Metodi IDWriteFontSetBuilder:: AddFontFaceReference

Aggiunge un riferimento a un tipo di carattere al set da compilare.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))                                         | Aggiunge un riferimento a un tipo di carattere al set da compilare. I metadati necessari verranno estratti automaticamente dal tipo di carattere quando si chiama CreateFontSet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**AddFontFaceReference (IDWriteFontFaceReference \* , proprietà Const DWrite \_ Font \_ \* , UInt32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32)) | Aggiunge un riferimento a un tipo di carattere al set da compilare. Il chiamante fornisce informazioni sufficienti per eseguire la ricerca, evitando la necessità di aprire il tipo di carattere potenzialmente non locale. Eventuali proprietà non fornite dal chiamante saranno mancanti e tali proprietà non saranno disponibili come filtri in GetMatchingFonts. GetPropertyValues per le proprietà mancanti restituirà un elenco di stringhe vuote. Le proprietà passate devono essere in genere coerenti con il contenuto effettivo del tipo di carattere, ma non devono essere. È possibile, ad esempio, assegnare un alias a un tipo di carattere usando un nome diverso o un identificatore univoco oppure impostare tag personalizzati non presenti nel tipo di carattere effettivo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DWrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

�

�
