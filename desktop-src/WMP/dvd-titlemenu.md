---
title: DVD. titleMenu, metodo
description: Il metodo titleMenu interrompe la riproduzione del titolo e visualizza il menu del titolo.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- Metodo titleMenu Windows Media Player
- Metodo titleMenu Windows Media Player, classe DVD
- Classe DVD Media Player Windows, metodo titleMenu
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
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340592"
---
# <a name="dvdtitlemenu-method"></a>DVD. titleMenu, metodo

Il metodo **titleMenu** interrompe la riproduzione del titolo e visualizza il menu del titolo.

## <a name="syntax"></a>Sintassi


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Ogni DVD viene creato in modo diverso. Il DVD deve contenere un menu per il funzionamento di questo metodo. Alcuni DVD vengono creati in modo che i metodi **tomenu** e **titleMenu** aprano lo stesso menu. Il metodo **titleMenu** richiama in genere il menu del titolo, ma può richiamare invece il menu superiore se non è disponibile alcun menu titolo.

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

[**DVD. menu di scelta rapida**](dvd-topmenu.md)
</dt> </dl>

 

 





