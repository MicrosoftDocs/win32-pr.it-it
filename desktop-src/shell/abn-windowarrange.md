---
description: Notifica a un AppBar che l'utente ha selezionato il comando Cascade, affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni.
title: Messaggio ABN_WINDOWARRANGE (Shellapi. h)
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
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525422"
---
# <a name="abn_windowarrange-message"></a>\_Messaggio WINDOWARRANGE di ABN

Notifica a un AppBar che l'utente ha selezionato il comando Cascade, affianca orizzontalmente o Affianca verticalmente dal menu di scelta rapida della barra delle applicazioni.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fBeginning* 
</dt> <dd>

Flag che specifica se l'operazione Cascade o Tile è iniziata. Questo parametro è **true** se l'operazione è iniziata e le finestre non sono ancora state spostate. È **false** se l'operazione è stata completata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il sistema invia questo messaggio di notifica due volte prima con *lParam* impostato su **true** e quindi con *lParam* impostato su **false**. La prima notifica viene inviata prima che le finestre siano a cascata o affiancate, mentre la seconda viene inviata dopo l'esecuzione dell'operazione Cascade o Tile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




