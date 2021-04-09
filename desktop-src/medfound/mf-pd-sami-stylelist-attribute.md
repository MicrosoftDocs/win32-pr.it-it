---
description: Contiene i nomi descrittivi degli stili SAMI (Synchronized Media Interchange) definiti nel file SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Attributo MF_PD_SAMI_STYLELIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885190"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>Attributo di stile dell'aspetto di MF \_ PD \_ Sami \_

Contiene i nomi descrittivi degli stili SAMI (Synchronized Media Interchange) definiti nel file SAMI.

L' [origine dei supporti Sami](sami-media-source.md) imposta questo attributo sul descrittore della presentazione che crea.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il BLOB dell'attributo presenta la struttura seguente:



Tipo di dati

Descrizione

Dimensioni (byte)

**DWORD**

Numero di stringhe di stile.

4

Per ogni stringa di stile:

**DWORD**

Dimensioni in byte della stringa, incluso il carattere **null** .

4

**LPWSTR**

Stringa di caratteri wide con terminazione null contenente il nome dello stile.

Varia



 

Per impostare lo stile o recuperare lo stile corrente, utilizzare l'interfaccia [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Origine supporto SAMI](sami-media-source.md)
</dt> </dl>

 

 




