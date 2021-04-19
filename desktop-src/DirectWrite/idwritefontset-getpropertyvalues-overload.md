---
title: Metodi GetPropertyValues IDWriteFontSet (DWrite \_ 3. h)
description: Restituisce i valori delle proprietà per il set di caratteri.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Scrittura diretta metodi GetPropertyValues
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328149"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a>Metodi IDWriteFontSet:: GetPropertyValues

Restituisce i valori delle proprietà per il set di caratteri.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetPropertyValues ( \_ \_ ID proprietà carattere DWrite \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))                       | Restituisce tutti i valori di proprietà univoci nel set, che possono essere utilizzati per scopi quali la visualizzazione di un elenco di famiglie o tag cloud. Tutti i valori vengono restituiti indipendentemente dalla lingua, inclusi tutti i nomi localizzati. <br/>                                                                                       |
| [**GetPropertyValues ( \_ ID della proprietà del tipo di carattere DWrite \_ \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))        | Restituisce tutti i valori di proprietà univoci nel set, che possono essere utilizzati per scopi quali la visualizzazione di un elenco di famiglie o tag cloud. I valori vengono restituiti in ordine di priorità in base all'elenco di lingue, in modo che se un tipo di carattere contiene più di un nome localizzato, verrà restituito quello preferito. <br/> |
| [**GetPropertyValues (UINT32, \_ ID proprietà del tipo di carattere DWrite \_ \_ , bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) | Restituisce i valori delle proprietà di un indice di elemento del tipo di carattere specifico.<br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DWrite \_ 3. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

�

�
