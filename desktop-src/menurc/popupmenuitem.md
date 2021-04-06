---
title: Struttura POPUPMENUITEM
description: Contiene informazioni sulle voci di menu in una risorsa di menu che aprono un menu o un sottomenu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menu struttura POPUPMENUITEM e altre risorse
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963894"
---
# <a name="popupmenuitem-structure"></a>Struttura POPUPMENUITEM

Contiene informazioni sulle voci di menu in una risorsa di menu che aprono un menu o un sottomenu. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a>Members

<dl> <dt>

**type**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Descrive la voce di menu. Alcuni dei valori che questo membro può avere includono quelli mostrati nell'elenco seguente.

Oltre ai valori indicati, questo membro può anche essere una combinazione dei valori di tipo elencati con il membro **ftype** della struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . I valori del tipo sono quelli che iniziano con MFT \_ . Per usare questi valori di tipo MFT predefiniti \_ \* , includere l'istruzione seguente nel file RC:

`#include "winuser.h"`



| Valore                                                                                                                                                                                                    | Significato                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ FINE**</dt> <dt>0x80</dt> </dl>       | La voce di menu è l'ultima nel menu; il flag viene utilizzato internamente dal sistema. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x01</dt> </dl> | La voce di menu apre un menu o un sottomenu; il flag viene utilizzato internamente dal sistema. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Descrive la voce di menu. Questo membro può essere una combinazione dei valori di stato elencati con il membro **dwState** della struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . I valori di stato sono quelli che iniziano con MFS \_ . Per usare questi valori di stato MFS predefiniti \_ \* , includere l'istruzione seguente nel file RC:

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Espressione numerica che identifica la voce di menu passata nel messaggio del [**\_ comando WM**](wm-command.md) .

</dd> <dt>

**resInfo**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Set di flag di bit che specificano il tipo di voce di menu. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**Fabbisogno \_ di FINE**</dt> <dt>0x80</dt> </dl>       | La voce di menu è l'ultima in questo sottomenu o risorsa di menu; Questo flag viene utilizzato internamente dal sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**Fabbisogno \_ di POPUP**</dt> <dt>0x01</dt> </dl> | La voce di menu apre un menu o un sottomenu; il flag viene utilizzato internamente dal sistema.<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Stringa Unicode con terminazione null che contiene il testo di questa voce di menu. Non esiste un limite fisso per le dimensioni di questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Esiste una struttura **POPUPMENUITEM** per ogni voce di menu che apre un menu o un sottomenu. Identificare questo tipo di voce di menu impostando il membro del **tipo** su **MF \_ popup** e impostando il bit del **\_ popup fabbisogno** nel membro **resInfo** su 0x0001. In questo caso, i dati finali scritti nella risorsa [**di \_ menu RT**](/windows/desktop/menurc/resource-types) per il menu o il sottomenu sono la struttura [**MENUHELPID**](menuhelpid.md) . **MENUHELPID** contiene un'espressione numerica che identifica il menu durante l'elaborazione della [**\_ Guida WM**](../shell/wm-help.md) .

Inoltre, ogni struttura **POPUPMENUITEM** che ha il **bit \_ popup di fabbisogno** impostato nel membro **ResInfo** sarà seguita da una struttura [**MENUHELPID**](menuhelpid.md) più un numero aggiuntivo di strutture **POPUPMENUITEM** , una per ogni voce di menu in quel sottomenu. L'ultima struttura **POPUPMENUITEM** nel sottomenu avrà il bit **\_ finale di fabbisogno** impostato nel membro **resInfo** . Per trovare la fine della risorsa, cercare un termine di un **fabbisogno \_** di base corrispondente per ogni **\_ popup di fabbisogno** , oltre a un' **\_ estremità ulteriore di fabbisogno** che corrisponda al set più esterno di voci di menu.

Indica l'ultima voce di menu impostando il membro del **tipo** su **MF \_ end**. Poiché è possibile annidare i sottomenu, possono essere presenti più livelli di **MF \_ end**. In questi casi, le voci di menu sono sequenziali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUHELPID**](menuhelpid.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

