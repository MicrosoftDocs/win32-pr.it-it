---
title: PLAYLIST. Copy
description: Il metodo Copy avvia un'operazione di copia dal CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- PLAYLIST. copiare Media Player Windows
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328046"
---
# <a name="playlistcopy"></a>PLAYLIST. Copy

Il metodo **Copy** avvia un'operazione di copia dal CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo copia solo gli elementi selezionati nella playlist e funziona allo stesso modo del riquadro **copia da CD** nella modalità completa di Windows Media Player. Per il corretto funzionamento di questo metodo, è necessario che sia presente un CD nell'unità CD. Impostare l'attributo **checkboxesVisible** su true per consentire agli utenti di selezionare singoli elementi in un CD prima della copia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**PLAYLIST. copia**](playlist-copying.md)
</dt> </dl>

 

 





