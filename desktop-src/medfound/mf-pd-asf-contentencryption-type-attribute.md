---
description: Specifica il tipo di meccanismo di protezione utilizzato in un file di formato Advanced Systems (ASF).
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: Attributo MF_PD_ASF_CONTENTENCRYPTION_TYPE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879145"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a>\_Attributo di tipo MF PD \_ ASF \_ CONTENTENCRYPTION \_

Specifica il tipo di meccanismo di protezione utilizzato in un file di formato Advanced Systems (ASF).

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Recupera il campo tipo di protezione, lo converte in una stringa di caratteri wide e quindi popola una matrice con terminazione null di **WCHAR** s. Se presente, il valore deve essere "DRM". La dimensione della matrice è uguale al campo della lunghezza del campo del tipo di protezione dell'intestazione della crittografia del contenuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




