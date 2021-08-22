---
title: Metodo Cdrom.eject
description: Il metodo eject espulse il CD o il DVD dall'unità. | Metodo Cdrom.eject
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- Eject method Windows Media Player
- Eject method Windows Media Player , Classe Cdrom
- Classe Cdrom Windows Media Player, metodo eject
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bd1c5a7a79c2a9b76b3a7a1997c43713fe0f3c1ae28e635a235feb82d214ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997681"
---
# <a name="cdromeject-method"></a>Metodo Cdrom.eject

Il **metodo di espulsione** espulse il CD o il DVD dall'unità.

## <a name="syntax"></a>Sintassi


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la porta dell'unità è aperta, questo metodo chiude la porta.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento pulsante HTML che usa *Cdrom*. **eject** per aprire la porta dell'unità con indice dell'identificatore di unità zero. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Versione<br/>                  | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Cdrom**](cdrom-object.md)
</dt> <dt>

[**Player.playState**](player-playstate.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





