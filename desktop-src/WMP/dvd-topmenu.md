---
title: Metodo DVD.topMenu
description: Il metodo topMenu arresta la riproduzione del titolo e visualizza il menu principale (o radice) per il titolo corrente.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- Metodo topMenu Windows Media Player
- Metodo topMenu Windows Media Player , classe DVD
- Classe DVD Windows Media Player, metodo topMenu
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6042547d26d40c620da503836de1ec15991280b17dd066cf81d32c617e85064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651161"
---
# <a name="dvdtopmenu-method"></a>Metodo DVD.topMenu

Il **metodo topMenu** arresta la riproduzione del titolo e visualizza il menu principale (o radice) per il titolo corrente.

## <a name="syntax"></a>Sintassi


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Il DVD deve contenere un menu per il funzionamento di questo metodo. Alcuni DVD vengono creati in modo che i **metodi topMenu** e **titleMenu** abilitino lo stesso menu. Il **metodo topMenu** in genere richiama il menu principale (o radice), ma può richiamare il menu del titolo, se non è disponibile alcun menu radice.

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

[**DVD.titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





