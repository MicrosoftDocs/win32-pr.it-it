---
title: PLAYLIST.copy
description: Il metodo copy avvia un'operazione di copia dal CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- Playlist.copy Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b897d22c1aa8e666c5de40aecb8ef63d17384957e82eee8dc7d569f0e71f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003191"
---
# <a name="playlistcopy"></a>PLAYLIST.copy

Il **metodo copy** avvia un'operazione di copia dal CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo copia solo gli elementi selezionati nella playlist e funziona allo stesso modo del riquadro Copia da **CD** nella modalità completa di Windows Media Player. Per il funzionamento di questo metodo, è necessario che nell'unità CD sia presente un CD. Impostare **l'attributo checkboxesVisible** su true per consentire agli utenti di selezionare singoli elementi in un CD prima della copia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**PLAYLIST.copying**](playlist-copying.md)
</dt> </dl>

 

 





