---
title: DVD. tomenu (metodo)
description: Il metodo di menu di scelta rapida interrompe la riproduzione del titolo e visualizza il menu principale (o radice) per il titolo corrente.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- Windows Media Player metodo di menu di scelta rapida
- Metodo di menu di scelta rapida Windows Media Player, classe DVD
- Classe DVD Media Player Windows, metodo tomenu
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
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477380"
---
# <a name="dvdtopmenu-method"></a>DVD. tomenu (metodo)

Il metodo di **menu di scelta rapida** interrompe la riproduzione del titolo e visualizza il menu principale (o radice) per il titolo corrente.

## <a name="syntax"></a>Sintassi


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Il DVD deve contenere un menu per il funzionamento di questo metodo. Alcuni DVD vengono creati in modo che i metodi **tomenu** e **titleMenu** aprano lo stesso menu. Il metodo di **menu di scelta rapida** richiama in genere il menu superiore (o radice), ma può invece richiamare il menu del titolo, se non è disponibile alcun menu radice.

**Windows Media Player 10 Mobile:** Questo metodo ha sempre esito positivo, ma non esegue l'operazione desiderata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Versione<br/>                  | Windows Media Player per Windows XP o versione successiva.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DVD**](dvd-object.md)
</dt> <dt>

[**DVD. titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





