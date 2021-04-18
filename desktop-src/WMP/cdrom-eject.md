---
title: Cdrom. EJECT (metodo)
description: Il metodo EJECT espelle il CD o il DVD dall'unità. | Cdrom. EJECT (metodo)
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- Metodo EJECT Media Player Windows
- Metodo EJECT Windows Media Player, classe cdrom
- Classe cdrom Media Player Windows, metodo EJECT
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
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321459"
---
# <a name="cdromeject-method"></a>Cdrom. EJECT (metodo)

Il metodo **eject** espelle il CD o il DVD dall'unità.

## <a name="syntax"></a>Sintassi


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se lo sportello dell'unità è aperto, questo metodo chiude lo sportello.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creato un elemento Button HTML che usa *CDROM*. **eject** per aprire la porta dell'unità con indice identificatore unità zero. L'oggetto **Player** è stato creato con ID = "Player".


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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Versione<br/>                  | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto cdrom**](cdrom-object.md)
</dt> <dt>

[**Player. riproduzione**](player-playstate.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





