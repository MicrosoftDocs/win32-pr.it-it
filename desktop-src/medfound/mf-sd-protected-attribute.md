---
description: Indica se un flusso contiene contenuto protetto.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: MF_SD_PROTECTED attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae6cf92b3ada6309de7e92a722db38c88ce94a8af88aa6cc0176f738ff194b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474051"
---
# <a name="mf_sd_protected-attribute"></a>Attributo \_ MF SD \_ PROTECTED

Indica se un flusso contiene contenuto protetto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di flusso. Se il valore dell'attributo è **TRUE,** il flusso contiene contenuto protetto. Se il valore è **FALSE** o l'attributo non è impostato, il flusso contiene contenuto non crittografato.

Anziché controllare ogni flusso per questo attributo, è possibile passare un descrittore di presentazione alla [**funzione MFRequireProtectedEnvironment.**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) Questa funzione verifica se il descrittore di presentazione contiene flussi protetti.

Un'origine multimediale deve impostare questo attributo sul descrittore di flusso se il contenuto richiede il percorso del supporto protetto (PMP).

La costante GUID per questo attributo viene esportata da mfuuid.lib.

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
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributi del descrittore di flusso](stream-descriptor-attributes.md)
</dt> </dl>

 

 




