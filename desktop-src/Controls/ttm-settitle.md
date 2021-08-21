---
title: TTM_SETTITLE messaggio (Commctrl.h)
description: Aggiunge un'icona standard e una stringa del titolo a una descrizione comando.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE controlli Windows messaggio
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e159ce522ea27361f93beaa96da06959fba6f92fedf5981dfd049ddc7f36cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166354"
---
# <a name="ttm_settitle-message"></a>TTM \_ SETTITLE message

Aggiunge un'icona standard e una stringa del titolo a una descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Impostare *wParam* su uno dei valori seguenti per specificare l'icona da visualizzare. A Windows XP SP2 e versioni successive, questo parametro può contenere anche un **valore HICON.** Si presuppone che qualsiasi valore maggiore di \_ TTI ERROR sia **hiCON.**



| Valore                                                                                                                                                                      | Significato                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ NONE**</dt> </dl>                             | Nessuna icona.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**TTI \_ INFO**</dt> </dl>                             | Icona Informazioni.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**AVVISO \_ TTI**</dt> </dl>                    | Icona avviso<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**ERRORE \_ TTI**</dt> </dl>                          | Icona di errore<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI \_ INFO \_ LARGE**</dt> </dl>          | Icona di errore di grandi dimensioni<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**AVVISO TTI \_ \_ DI GRANDI DIMENSIONI**</dt> </dl> | Icona di errore di grandi dimensioni<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**ERRORE TTI \_ \_ DI GRANDI DIMENSIONI**</dt> </dl>       | Icona di errore di grandi dimensioni<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa del titolo. È necessario assegnare un valore a *lParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo, **FALSE** in caso contrario.

## <a name="remarks"></a>Commenti

Il titolo di una descrizione comando viene visualizzato sopra il testo, con un tipo di carattere diverso. Non è sufficiente avere un titolo. La descrizione comando deve contenere anche testo oppure non viene visualizzata.

Quando *wParam contiene* un **hiCON,** una copia dell'icona viene creata dalla finestra di descrizione comando.

Quando si **chiama TTM \_ SETTITLE,** la stringa a cui punta *lParam* non deve superare i 100 **TCHAR,** incluso il valore NULL di **terminazione.**

## <a name="examples"></a>Esempio

L'esempio seguente illustra come aggiungere un titolo e un'icona di sistema a una descrizione comando.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ SETTITLEW** (Unicode) e **TTM \_ SETTITLEA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli descrizione comando](tooltip-controls.md)
</dt> </dl>

 

 





