---
title: Attributo DLNASourceURI
description: L'attributo DLNASourceURI è l'URI (Universal Resource Identifier) dell'elemento.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Attributo DLNASourceURI Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e5383de75fef1a0e1957f270a8a5238951bce4ede1418dbf79ba2038777372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997171"
---
# <a name="dlnasourceuri-attribute"></a>Attributo DLNASourceURI

**L'attributo DLNASourceURI** è l'URI (Universal Resource Identifier) dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Altri elementi**](other-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi playlist**](playlist-attributes-ref.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Se l'elemento si trova nella libreria locale dell'utente corrente, questo attributo, l'attributo [**SourceURL**](sourceurl-attribute.md) e il valore restituito da [**IWMPMedia::get \_ sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) sono tutti uguali.

Se l'elemento non si trova nella libreria locale dell'utente corrente, ma appartiene a una libreria remota, questo attributo è un identificatore nel formato dlna-playsingle://*xxx*.

È possibile passare un URI di riproduzione dlna al metodo [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) per ottenere [**un'interfaccia IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) che consente di visualizzare i metadati dell'elemento multimediale e potenzialmente modificare la classificazione a stella dell'elemento multimediale. Si noti, tuttavia, che l'URI dlna-playsingle deve essere per un servizio di directory del contenuto (CDS) che Windows Media Player già individuato. Il **metodo newMedia** non avvierà l'individuazione UPnP e non ricercherà CDS.

È possibile modificare la classificazione a stella di un elemento multimediale in una libreria remota solo se la libreria remota supporta l'operazione di modifica. Le librerie remote ospitate in un computer che esegue Windows 7 supportano l'operazione di modifica. Le librerie remote ospitate in un computer che esegue Windows sistema operativo precedente Windows 7 non supportano l'operazione di modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





