---
title: TB_HASACCELERATOR messaggio (Commctrl.h)
description: Recupera un conteggio dei pulsanti della barra degli strumenti con il carattere di tasto di scelta rapida specificato.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420f06e71c6920c266c96d8b2580549fa0eaace2bd3abdd37524502d4039aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078285"
---
# <a name="tb_hasaccelerator-message"></a>Messaggio \_ HASACCELERATOR DA TB

\[Destinato all'uso interno; non consigliato per l'uso nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Recupera un conteggio dei pulsanti della barra degli strumenti con il carattere di tasto di scelta rapida specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

WCHAR **che rappresenta** il carattere del tasto di scelta rapida di input da testare.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a **un valore int** che riceve il numero di pulsanti con il carattere di scelta rapida.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

In primo luogo, il sistema esegue una query su tutti i pulsanti della barra degli strumenti per trovare i tasti di scelta rapida corrispondenti. Se non viene trovata alcuna corrispondenza, il sistema invia la notifica [ \_ MAPACCELERATOR TBN](tbn-mapaccelerator.md) alla finestra padre, richiedendo l'indice del pulsante con il carattere di tasto di scelta rapida specificato. Se l'elemento padre fornisce un indice, il conteggio viene impostato su 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





