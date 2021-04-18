---
title: Attributo DLNAServerUDN
description: L'attributo DLNAServerUDN è il nome univoco del dispositivo del server che ospita l'elemento multimediale.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- Attributo DLNAServerUDN Windows Media Player
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329946"
---
# <a name="dlnaserverudn-attribute"></a>Attributo DLNAServerUDN

L'attributo **DLNAServerUDN** è il nome univoco del dispositivo del server che ospita l'elemento multimediale.

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi della playlist**](playlist-attributes-ref.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente. È disponibile solo per gli elementi multimediali che appartengono a una libreria remota; ovvero una libreria che è stata resa disponibile da un altro utente nella rete domestica. Per determinare se un catalogo multimediale è remoto, chiamare [**IWMPLibrary:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





