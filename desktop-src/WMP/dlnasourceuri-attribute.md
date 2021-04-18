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
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327169"
---
# <a name="dlnasourceuri-attribute"></a>Attributo DLNASourceURI

L'attributo **DLNASourceURI** è l'URI (Universal Resource Identifier) dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Altri elementi**](other-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi della playlist**](playlist-attributes-ref.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Se l'elemento si trova nella libreria locale dell'utente corrente, questo attributo, l'attributo [**SourceURL**](sourceurl-attribute.md) e il valore restituito da [**IWMPMedia:: Get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) sono tutti uguali.

Se l'elemento non è presente nella libreria locale dell'utente corrente, ma appartiene a una libreria remota, questo attributo è un identificatore del formato DLNA-playsingle://*xxx*.

È possibile passare un URI DLNA-playsingle al metodo [**IWMPCore3:: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) per ottenere un'interfaccia [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) che consente di visualizzare i metadati dell'elemento multimediale e di modificare potenzialmente la classificazione a stelle dell'elemento multimediale. Si noti, tuttavia, che l'URI DLNA-playsingle deve essere per un servizio di directory del contenuto (CDS) già individuato da Windows Media Player. Il metodo **newMedia** non avvierà l'individuazione UPnP e cercherà i CD.

È possibile modificare la classificazione a stelle di un elemento multimediale in una libreria remota solo se la libreria remota supporta l'operazione di modifica. Le librerie remote ospitate in un computer che esegue Windows 7 supportano l'operazione di modifica. Le librerie remote ospitate in un computer che esegue un sistema operativo Windows precedente a Windows 7 non supportano l'operazione di modifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





