---
description: Inviato da un'estensione di File Manager per recuperare il tipo di finestra di File Manager con lo stato attivo per l'input.
title: FM_GETFOCUS messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: 7512595008ad79d33bf1ac9b381b63831977282b83a8ce595c3d2689087c869c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459111"
---
# <a name="fm_getfocus-message"></a>Messaggio \_ FM GETFOCUS

Inviato da un'estensione di File Manager per recuperare il tipo di finestra di File Manager con lo stato attivo per l'input.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il tipo di finestra di Gestione file con lo stato attivo per l'input. Può essere uno dei valori seguenti.



| Codice restituito                                                                                    | Descrizione                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ DIR**</dt> </dl>    | Parte della directory di una finestra della directory.<br/> |
| <dl> <dt>**ALBERO \_ FMFOCUS**</dt> </dl>   | Parte dell'albero di una finestra della directory.<br/>      |
| <dl> <dt>**UNITÀ \_ FMFOCUS**</dt> </dl> | Barra delle unità di una finestra della directory.<br/>         |
| <dl> <dt>**RICERCA \_ FMFOCUS**</dt> </dl> | Finestra Risultati ricerca.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 




