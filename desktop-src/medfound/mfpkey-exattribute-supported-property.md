---
description: Specifica se una trasformazione Media Foundation copia gli attributi dagli esempi di input agli esempi di output.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED proprietà (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248609828df3ef977112058ffe0d169104e68c181fa455ef27f2adcea0220aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663510"
---
# <a name="mfpkey_exattribute_supported-property"></a>MFPKEY \_ EXATTRIBUTE \_ SUPPORTED - proprietà

Specifica se una trasformazione Media Foundation copia gli attributi dagli esempi di input agli esempi di output.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Commenti

Questo attributo può avere i valori seguenti.



| Valore              | Descrizione                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | MFT copia gli attributi dagli esempi di input agli esempi di output.                                                                                 |
| **VARIANT \_ FALSE** | La sessione multimediale copia gli attributi dagli esempi di input agli esempi di output. Non sovrascrive gli attributi che il MFT imposta sugli esempi di output. |



 

Per ottenere questo attributo, chiamare **QueryInterface** in MFT per **l'interfaccia IPropertyStore.**

Il valore predefinito è **VARIANT \_ FALSE.** Se MFT non espone **l'interfaccia IPropertyStore** o se questa proprietà non è impostata, considerare il valore **come VARIANT \_ FALSE.**

Questa proprietà è di sola lettura.

> [!NOTE] 
> Questo attributo non si applica ai MFT asincroni. Gli attributi non verranno copiati dagli esempi di input agli esempi di output per MFT asincroni, indipendentemente dal valore di questo attributo.

## <a name="examples"></a>Esempio

L'esempio seguente restituisce VARIANT \_ TRUE se un MFT copia gli attributi di esempio.


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




