---
description: Indica se un flusso contiene contenuto protetto.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Attributo MF_SD_PROTECTED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318414"
---
# <a name="mf_sd_protected-attribute"></a>\_ \_ Attributo protetto MF SD

Indica se un flusso contiene contenuto protetto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di flusso. Se il valore dell'attributo è **true**, il flusso contiene contenuto protetto. Se il valore è **false** o l'attributo non è impostato, il flusso contiene contenuto non crittografato.

Anziché controllare ogni flusso per questo attributo, è possibile passare un descrittore di presentazione alla funzione [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) . Questa funzione verifica se il descrittore della presentazione contiene flussi protetti.

Un'origine multimediale deve impostare questo attributo sul descrittore del flusso se il contenuto richiede il percorso del supporto protetto (PMP).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="examples"></a>Esempio


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributi del descrittore di flusso](stream-descriptor-attributes.md)
</dt> </dl>

 

 




