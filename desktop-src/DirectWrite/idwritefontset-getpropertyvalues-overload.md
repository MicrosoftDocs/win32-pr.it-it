---
title: Metodi IdWriteFontSet GetPropertyValues (Dwrite \_ 3.h)
description: Restituisce i valori delle proprietà per il set di caratteri.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Metodi GetPropertyValues Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cffc669d71bf7f78087fe3c105c182ca86b4ebf5a689bcdb6c2807dfae3c0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816362"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>Metodi IDWriteFontSet::GetPropertyValues

Restituisce i valori delle proprietà per il set di caratteri.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Restituisce tutti i valori univoci delle proprietà nel set, che possono essere usati per scopi quali la visualizzazione di un elenco di famiglie o tag cloud. Tutti i valori vengono restituiti indipendentemente dalla lingua, inclusi tutti i nomi localizzati. <br/>                                                                                       |
| [**GetPropertyValues(DWRITE \_ FONT \_ PROPERTY \_ ID, const \* WCHAR, IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Restituisce tutti i valori univoci delle proprietà nel set, che possono essere usati per scopi quali la visualizzazione di un elenco di famiglie o tag cloud. I valori vengono restituiti in ordine di priorità in base all'elenco delle lingue, in modo che se un tipo di carattere contiene più di un nome localizzato, verrà restituito quello preferito. <br/> |
| [**GetPropertyValues(UINT32, DWRITE \_ FONT \_ PROPERTY \_ ID, \* BOOL, IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Restituisce i valori delle proprietà di un indice dell'elemento del tipo di carattere specifico.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dwrite \_ 3.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
