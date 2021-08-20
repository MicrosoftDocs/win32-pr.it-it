---
title: Metodo DVD.titleMenu
description: Il metodo titleMenu arresta la riproduzione del titolo e visualizza il menu del titolo.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- Metodo titleMenu Windows Media Player
- Metodo titleMenu Windows Media Player , classe DVD
- Classe DVD Windows Media Player, metodo titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1954ea52d5a67dc502278c7f1e821a06c4e2b849dc4040e690275b6d1b0ef0bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996881"
---
# <a name="dvdtitlemenu-method"></a>Metodo DVD.titleMenu

Il **metodo titleMenu** arresta la riproduzione del titolo e visualizza il menu del titolo.

## <a name="syntax"></a>Sintassi


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Il DVD deve contenere un menu per il funzionamento di questo metodo. Alcuni DVD vengono creati in modo che i **metodi topMenu** e **titleMenu** abilitino lo stesso menu. Il **metodo titleMenu** in genere richiama il menu del titolo, ma può richiamare il menu in alto, se non è disponibile alcun menu titolo.

**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione prevista.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Versione<br/>                  | Windows Media Player per Windows XP o versioni successive.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> <dt>

[**DVD.topMenu**](dvd-topmenu.md)
</dt> </dl>

 

 





