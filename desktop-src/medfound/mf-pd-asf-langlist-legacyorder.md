---
description: Contiene un elenco di lingue RFC 1766 utilizzate nella presentazione corrente.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: Attributo MF_PD_ASF_LANGLIST_LEGACYORDER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315017"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>\_ \_ \_ Attributo LEGACYORDER di MF PD \_ ASF

Contiene un elenco di lingue RFC 1766 utilizzate nella presentazione corrente.

## <a name="data-type"></a>Tipo di dati

**BYTE \[\]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione generati dall' [oggetto ContentInfo ASF](asf-contentinfo-object.md) mediante una chiamata a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Il formato della matrice di byte è il seguente:



| Campo oggetto elenco lingue | Tipo di dati    | Dimensione    | Descrizione                            |
|----------------------------|--------------|---------|----------------------------------------|
| Conteggio record ID lingua  | **DWORD**    | 4 byte | Numero di lingue                    |
| Record ID lingua        | **BYTE**\[\] | Varia  | Matrice di stringhe di linguaggio (vedere di seguito). |



 

Il primo **valore DWORD** è il numero di lingue, seguito da una matrice di stringhe dell'identificatore di lingua. Ogni stringa ha il formato seguente:



| Campo oggetto elenco lingue | Tipo di dati     | Dimensione    | Descrizione                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Lunghezza ID lingua         | **DWORD**     | 4 byte | Lunghezza della stringa in byte, incluse le dimensioni del carattere **null** finale. |
| ID lingua                | **WCHAR**\[\] | Varia  | Stringa con terminazione null che contiene il nome della lingua RFC 1766.                           |



 

Ogni stringa è un tag di lingua conforme a RFC 1766.

Utilizzare questo attributo solo per compatibilità con le versioni precedenti con l'ordine di enumerazione dell'interfaccia [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) in Windows Media Format SDK. Le stringhe della lingua sono archiviate in un ordine diverso nell'attributo [**lang di MF \_ PD \_ ASF \_**](mf-pd-asf-langlist-attribute.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
