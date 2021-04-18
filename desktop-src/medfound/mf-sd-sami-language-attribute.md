---
description: Contiene il nome del linguaggio SAMI (Synchronized Accessible Media Interchange) definito per il flusso.
ms.assetid: 3151c369-9d2b-4f03-9a4a-9b9267314dc1
title: Attributo MF_SD_SAMI_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd476c86ddde7d369265c5302192e4a7c01295f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318413"
---
# <a name="mf_sd_sami_language-attribute"></a>\_Attributo del linguaggio MF SD \_ Sami \_

Contiene il nome del linguaggio SAMI (Synchronized Accessible Media Interchange) definito per il flusso.

Questo attributo è presente nei descrittori di flusso restituiti dall'origine dei supporti SAMI.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

Il nome del linguaggio SAMI viene specificato nel file SAMI.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

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

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributi del descrittore di flusso](stream-descriptor-attributes.md)
</dt> <dt>

[**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)
</dt> </dl>

 

 




