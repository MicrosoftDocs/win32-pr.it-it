---
title: Messaggio di EM_GETTOUCHOPTIONS (RichEdit. h)
description: Recupera le opzioni di tocco associate a un controllo Rich Edit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Controlli di Windows Message EM_GETTOUCHOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048603"
---
# <a name="em_gettouchoptions-message"></a>\_Messaggio GETTOUCHOPTIONS em

Recupera le opzioni di tocco associate a un controllo Rich Edit.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Opzioni di tocco da recuperare. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                        | Significato                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**\_SHOWHANDLES RTO**</dt> </dl>          | Recupera un valore che indica se le pinze tocco sono visibili.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**\_DISABLEHANDLES RTO**</dt> </dl> | Il recupero del flag non è implementato.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore dell'opzione specificata dal parametro *wParam* . È diverso da zero se *wParam* è **RTO \_ SHOWHANDLES** e le pinze tocco sono visibili; zero, in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTOUCHOPTIONS em**](em-settouchoptions.md)
</dt> </dl>

 

 





