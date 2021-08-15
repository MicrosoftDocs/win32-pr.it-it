---
description: Notifica a una barra delle app che l'utente ha selezionato il comando Sovrapponi, Affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni.
title: ABN_WINDOWARRANGE messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27c679b7ccdb5eb92ebe87676cd136c71adcda862472f6f300056511001a683a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225022"
---
# <a name="abn_windowarrange-message"></a>Messaggio \_ WINDOWARRANGE ABN

Notifica a una barra delle app che l'utente ha selezionato il comando Sovrapponi, Affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fBeginning* 
</dt> <dd>

Flag che specifica se l'operazione di propagazione o affiancata sta iniziando. Questo parametro è **TRUE se** l'operazione inizia e le finestre non sono ancora state spostate. È **FALSE se** l'operazione è stata completata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il sistema invia questo messaggio di notifica due volte prima *con lParam* impostato su **TRUE** e quindi con *lParam* impostato su **FALSE.** La prima notifica viene inviata prima che le finestre siano propagate o affiancate e la seconda viene inviata dopo che si è verificata l'operazione a cascata o affiancata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




