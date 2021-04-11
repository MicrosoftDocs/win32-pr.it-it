---
description: Specifica l'identificatore di chiave per un file ASF (Advanced Systems Format) crittografato. Questo attributo corrisponde al campo ID chiave dell'intestazione di crittografia del contenuto, definito nella specifica ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: Attributo MF_PD_ASF_CONTENTENCRYPTION_KEYID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129003"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>\_Attributo KEYID MF PD \_ ASF \_ CONTENTENCRYPTION \_

Specifica l'identificatore di chiave per un file ASF (Advanced Systems Format) crittografato. Questo attributo corrisponde al campo ID chiave dell'intestazione di crittografia del contenuto, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Recupera il campo ID chiave, lo converte in una stringa di caratteri wide e quindi popola una matrice con terminazione null di **WCHAR** s. La dimensione della matrice è uguale al campo lunghezza ID chiave dell'intestazione della crittografia del contenuto.

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

 

 




