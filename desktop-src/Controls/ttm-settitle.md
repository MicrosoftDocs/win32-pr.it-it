---
title: Messaggio TTM_SETTITLE (COMmctrl. h)
description: Aggiunge un'icona standard e una stringa del titolo a una descrizione comando.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- Controlli di Windows Message TTM_SETTITLE
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
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874486"
---
# <a name="ttm_settitle-message"></a>\_Messaggio TTM

Aggiunge un'icona standard e una stringa del titolo a una descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Impostare *wParam* su uno dei valori seguenti per specificare l'icona da visualizzare. A partire da Windows XP SP2 e versioni successive, questo parametro può contenere anche un valore **HICON** . Si presuppone che un valore maggiore di TTI sia \_ un errore di **HICON**.



| Valore                                                                                                                                                                      | Significato                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ None**</dt> </dl>                             | Nessuna icona.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**\_informazioni tti**</dt> </dl>                             | Icona info.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**avviso di TTI \_**</dt> </dl>                    | Icona avviso<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**\_errore tti**</dt> </dl>                          | Icona di errore<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**\_informazioni tti \_ large**</dt> </dl>          | Icona di errore grande<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**\_avviso tti \_ grande**</dt> </dl> | Icona di errore grande<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**\_errore tti \_ grande**</dt> </dl>       | Icona di errore grande<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla stringa del titolo. È necessario assegnare un valore a *lParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo, **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il titolo di una descrizione comando viene visualizzato sopra il testo, in un tipo di carattere diverso. Non è sufficiente avere un titolo; la descrizione comando deve avere anche testo o non è visualizzata.

Quando *wParam* contiene un **HICON**, viene creata una copia dell'icona dalla finestra della descrizione comando.

Quando si **chiama \_ TTM setitle**, la stringa a cui fa riferimento *lParam* non deve superare 100 **TCHARs** di lunghezza, incluso il **null** di terminazione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come aggiungere un titolo e un'icona di sistema a una descrizione comando.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ SETTITLEW** (Unicode) e **TTM \_ setitlea** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





