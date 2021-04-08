---
description: Specifica se un Media Foundation Transform (MFT) copia gli attributi dagli esempi di input agli esempi di output.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Proprietà MFPKEY_EXATTRIBUTE_SUPPORTED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880805"
---
# <a name="mfpkey_exattribute_supported-property"></a>\_ \_ Proprietà supportata MFPKEY EXATTRIBUTE

Specifica se un Media Foundation Transform (MFT) copia gli attributi dagli esempi di input agli esempi di output.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**\_bool Variant**

\_bool VT

**boolVal**



## <a name="remarks"></a>Commenti

Questo attributo può avere i valori seguenti.



| Valore              | Descrizione                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ true**  | Il MFT copia gli attributi dagli esempi di input negli esempi di output.                                                                                 |
| **VARIANTE \_ false** | La sessione multimediale copia gli attributi dagli esempi di input agli esempi di output. Non sovrascrive gli attributi impostati da MFT sugli esempi di output. |



 

Per ottenere questo attributo, chiamare **QueryInterface** sulla MFT per l'interfaccia **IPropertyStore** .

Il valore predefinito è **Variant \_ false**. Se MFT non espone l'interfaccia **IPropertyStore** o se questa proprietà non è impostata, trattare il valore come **Variant \_ false**.

Questa proprietà è di sola lettura.

> [!NOTE] 
> Questo attributo non è applicabile a MFTs asincrono. Gli attributi non verranno copiati dagli esempi di input agli esempi di output per MFTs asincroni, indipendentemente dal valore di questo attributo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene restituito VARIANT \_ true se una MFT copia gli attributi di esempio.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




