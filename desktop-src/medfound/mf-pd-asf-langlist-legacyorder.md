---
description: Contiene un elenco di lingue RFC 1766 usate nella presentazione corrente.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: MF_PD_ASF_LANGLIST_LEGACYORDER attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32693550ecbe48d14d6e26b9c509f3b90cfd1c327fd945583f1cdff729db7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102931"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>Attributo \_ LEGACYORDER MF PD \_ ASF \_ LANGLIST \_

Contiene un elenco di lingue RFC 1766 usate nella presentazione corrente.

## <a name="data-type"></a>Tipo di dati

**BYTE \[\]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Si applica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione generati [dall'oggetto ContentInfo](asf-contentinfo-object.md) di ASF da una chiamata a [**IMFASFContentInfo::GeneratePresentationDescriptor.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Il formato della matrice di byte è il seguente:



| Campo Language List Object | Tipo di dati    | Dimensione    | Descrizione                            |
|----------------------------|--------------|---------|----------------------------------------|
| Conteggio record ID lingua  | **Dword**    | 4 byte | Numero di lingue                    |
| Record ID lingua        | **BYTE**\[\] | Varia  | Matrice di stringhe di lingua (vedere di seguito). |



 

Il primo **valore DWORD** è il numero di lingue, seguito da una matrice di stringhe di identificatori di lingua. Ogni stringa ha il formato seguente:



| Campo Language List Object | Tipo di dati     | Dimensione    | Descrizione                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Lunghezza ID lingua         | **Dword**     | 4 byte | Lunghezza della stringa in byte, inclusa la dimensione del carattere **NULL** finale. |
| ID lingua                | **Wchar**\[\] | Varia  | Stringa con terminazione Null contenente il nome della lingua RFC 1766.                           |



 

Ogni stringa è un tag di lingua conforme a RFC 1766.

Usare questo attributo solo per la compatibilità con le versioni precedenti con l'ordine di enumerazione dell'interfaccia [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) in Windows Media Format SDK. Le stringhe di lingua vengono archiviate in un ordine diverso nell'attributo [**\_ \_ \_ LANGLIST di MF PD ASF.**](mf-pd-asf-langlist-attribute.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
