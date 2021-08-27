---
title: Struttura POPUPMENUITEM
description: Contiene informazioni sulle voci di menu in una risorsa di menu che apre un menu o un sottomenu. La definizione della struttura qui fornita è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Struttura POPUPMENUITEM Menu e altre risorse
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62d769e9756f0d15e7377a79f9aa94802a469746807e3a32b5ba329f76484b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011701"
---
# <a name="popupmenuitem-structure"></a>Struttura POPUPMENUITEM

Contiene informazioni sulle voci di menu in una risorsa di menu che apre un menu o un sottomenu. La definizione della struttura qui fornita è solo per la spiegazione. non è presente in alcun file di intestazione standard.

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

Descrive la voce di menu. Alcuni dei valori che questo membro può avere includono quelli visualizzati nell'elenco seguente.

Oltre ai valori visualizzati, questo membro può anche essere una combinazione dei valori di tipo elencati con il membro **fType** della [**struttura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) I valori di tipo sono quelli che iniziano con MFT \_ . Per usare questi valori di tipo MFT \_ \* predefiniti, includere l'istruzione seguente nel file RC:

`#include "winuser.h"`



| Valore                                                                                                                                                                                                    | Significato                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_ END**</dt> <dt>0x80</dt> </dl>       | La voce di menu è l'ultima nel menu. il flag viene usato internamente dal sistema. <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x01</dt> </dl> | La voce di menu apre un menu o un sottomenu. il flag viene usato internamente dal sistema. <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Descrive la voce di menu. Questo membro può essere una combinazione dei valori di stato elencati con il **membro dwState** della [**struttura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) I valori di stato sono quelli che iniziano con \_ MFS. Per usare questi valori di stato MFS \_ \* predefiniti, includere l'istruzione seguente nel file RC:

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Espressione numerica che identifica la voce di menu passata nel [**messaggio WM \_ COMMAND.**](wm-command.md)

</dd> <dt>

**Resinfo**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Set di flag di bit che specificano il tipo di voce di menu. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_ END**</dt> <dt>0x80</dt> </dl>       | La voce di menu è l'ultima in questo sottomenu o in questa risorsa di menu. questo flag viene usato internamente dal sistema.<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_ POPUP**</dt> <dt>0x01</dt> </dl> | La voce di menu apre un menu o un sottomenu. il flag viene usato internamente dal sistema.<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

Tipo: **szOrOrd**

</dd> <dd>

Stringa Unicode con terminazione Null che contiene il testo per questa voce di menu. Non esiste alcun limite fisso per le dimensioni di questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Esiste una struttura **POPUPMENUITEM** per ogni voce di menu che apre un menu o un sottomenu. Identificare questo tipo di voce  di menu impostando il membro del tipo su **\_ MF POPUP** e impostando il bit **MFR \_ POPUP** nel membro **resInfo** su 0x0001. In questo caso, i dati finali scritti nella risorsa [**RT \_ MENU**](/windows/desktop/menurc/resource-types) per il menu o il sottomenu sono la [**struttura MENUHELPID.**](menuhelpid.md) **MENUHELPID contiene** un'espressione numerica che identifica il menu durante [**l'elaborazione di WM \_ HELP.**](../shell/wm-help.md)

Inoltre, ogni **struttura POPUPMENUITEM** con il bit **POPUP \_ MFR** impostato nel membro **resInfo** sarà seguita da una struttura [**MENUHELPID**](menuhelpid.md) più un numero aggiuntivo di **strutture POPUPMENUITEM,** una per ogni voce di menu in tale sottomenu. **L'ultima struttura POPUPMENUITEM** nel sottomenu avrà il bit **MFR \_ END** impostato nel **membro resInfo.** Per trovare la fine della risorsa, cercare un'opzione **MFR \_ END** corrispondente per ogni **\_ popup MFR** più un'altra **MFR \_ END** corrispondente al set più esterno di voci di menu.

Indicare l'ultima voce di menu impostando il **membro del** tipo su **MF \_ END.** Poiché è possibile annidare i sottomenu, possono essere presenti più livelli **di MF \_ END.** In questi casi, le voci di menu sono sequenziali.

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

 

