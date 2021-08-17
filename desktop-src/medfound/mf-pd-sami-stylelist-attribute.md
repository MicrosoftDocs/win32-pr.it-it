---
description: Contiene i nomi descrittivi degli stili SAMI (Synchronized Accessible Media Interchange) definiti nel file SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: MF_PD_SAMI_STYLELIST attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f57d418eb86c19d3aa2db12808dde810456c38ec6abd45fbece450b30f60f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876174"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>Attributo \_ \_ SAMI \_ STYLELIST del PD MF

Contiene i nomi descrittivi degli stili SAMI (Synchronized Accessible Media Interchange) definiti nel file SAMI.

[L'origine supporto SAMI](sami-media-source.md) imposta questo attributo sul descrittore di presentazione creato.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il BLOB dell'attributo ha la struttura seguente:



Tipo di dati

Descrizione

Dimensioni (byte)

**Dword**

Numero di stringhe di stile.

4

Per ogni stringa di stile:

**Dword**

Dimensione della stringa in byte, incluso il **carattere NULL.**

4

**LPWSTR**

Stringa di caratteri wide con terminazione Null contenente il nome dello stile.

Varia



 

Per impostare lo stile o recuperare lo stile corrente, usare [**l'interfaccia IMFSAMIStyle.**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="examples"></a>Esempio


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Origine supporto SAMI](sami-media-source.md)
</dt> </dl>

 

 




