---
title: MENUEX_TEMPLATE_ITEM struttura
description: Definisce una voce di menu in un modello di menu esteso. Questa definizione di struttura è solo a scopo di spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM struttura menu e altre risorse
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6352c7ce596a59d69b21f1ba424ac50b471e13cd97320f0df184bce2e1abd295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733906"
---
# <a name="menuex_template_item-structure"></a>Struttura MENUEX \_ TEMPLATE \_ ITEM

Definisce una voce di menu in un modello di menu esteso. Questa definizione di struttura è solo a scopo di spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a>Members

<dl> <dt>

**dwType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo di voce di menu. Questo membro può essere una combinazione dei valori di tipo (a partire da MFT) elencati con la [**struttura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

</dd> <dt>

**dwState**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stato della voce di menu. Questo membro può essere una combinazione dei valori di stato (a partire da MFS) elencati con la [**struttura MENUITEMINFO.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)

</dd> <dt>

**Uid**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Identificatore della voce di menu. Si tratta di un valore definito dall'applicazione che identifica la voce di menu. In una risorsa di menu estesa, le voci che aprono menu a discesa o sottomenu, nonché le voci di comando, possono avere identificatori.

</dd> <dt>

**Wflags**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Specifica se la voce di menu è l'ultima voce nella barra dei menu, nel menu a discesa, nel sottomenu o nel menu di scelta rapida e se si tratta di una voce che apre un menu a discesa o un sottomenu. Questo membro può essere zero o più di questi valori. Per le applicazioni a 32 bit, questo membro è una parola; Per le applicazioni a 16 bit, è un byte.

<dt>

0x80
</dt> <dd>

La struttura definisce l'ultima voce di menu nella barra dei menu, nel menu a discesa, nel sottomenu o nel menu di scelta rapida.

</dd> <dt>

0x01
</dt> <dd>

La struttura definisce un elemento che apre un menu a discesa o un sottomenu. Le strutture successive definiscono le voci di menu nel sottomenu o nel menu a discesa corrispondente.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Testo della voce di menu. Questo membro è una stringa Unicode con terminazione Null, allineata su un confine di parola. Le dimensioni della definizione della voce di menu variano a seconda della lunghezza di questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un modello di menu esteso è costituito da una [**struttura MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) seguita da una o più strutture **MENUEX TEMPLATE \_ \_ ITEM** contigue. Le **strutture MENUEX \_ TEMPLATE \_ ITEM,** di lunghezza variabile, sono allineate in base **ai limiti DWORD.** Per creare un menu da un modello di menu esteso in memoria, usare la [**funzione LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**INTESTAZIONE DEL MODELLO MENUEX \_ \_**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

 





