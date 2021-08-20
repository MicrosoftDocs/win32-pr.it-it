---
description: Specifica l'identificatore di chiave per un file ASF (Advanced Systems Format) crittografato. Questo attributo corrisponde al campo KEY ID dell'intestazione content encryption, definito nella specifica ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: MF_PD_ASF_CONTENTENCRYPTION_KEYID attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edae0f324e7ab4889b21ae69714da16bfa88803db1d3aef808e4ba715522f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876434"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>Attributo MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID

Specifica l'identificatore di chiave per un file ASF (Advanced Systems Format) crittografato. Questo attributo corrisponde al campo KEY ID dell'intestazione content encryption, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto asf.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera il campo KEY ID, lo converte in una stringa di caratteri wide e quindi popola una matrice con terminazione Null di **WCHAR.** La dimensione della matrice è uguale al campo Lunghezza ID chiave dell'intestazione di crittografia del contenuto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




