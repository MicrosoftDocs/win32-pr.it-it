---
title: Messaggio TB_HASACCELERATOR (COMmctrl. h)
description: Recupera un conteggio dei pulsanti della barra degli strumenti con il carattere di accelerazione specificato.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- Controlli di Windows Message TB_HASACCELERATOR
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
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477104"
---
# <a name="tb_hasaccelerator-message"></a>TB \_ HASACCELERATOR messaggio

\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Recupera un conteggio dei pulsanti della barra degli strumenti con il carattere di accelerazione specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Oggetto **WCHAR** che rappresenta il carattere dell'acceleratore di input da testare.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore **int** che riceve il numero di pulsanti con il carattere di accelerazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

Innanzitutto, il sistema esegue una query su tutti i pulsanti della barra degli strumenti per individuare gli acceleratori corrispondenti Se non viene trovata alcuna corrispondenza, il sistema invia la notifica [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) alla finestra padre, richiedendo l'indice del pulsante con il carattere di accelerazione specificato. Se l'elemento padre fornisce un indice, il conteggio viene impostato su 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





