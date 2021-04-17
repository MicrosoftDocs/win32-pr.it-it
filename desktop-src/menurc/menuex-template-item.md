---
title: Struttura MENUEX_TEMPLATE_ITEM
description: Definisce una voce di menu in un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- Menu struttura MENUEX_TEMPLATE_ITEM e altre risorse
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518699"
---
# <a name="menuex_template_item-structure"></a>Struttura dell'elemento del \_ modello menuex \_

Definisce una voce di menu in un modello di menu esteso. Questa definizione di struttura è solo per la spiegazione; non è presente in alcun file di intestazione standard.

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

Tipo di voce di menu. Questo membro può essere una combinazione dei valori di tipo (a partire da MFT) elencati con la struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**dwState**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stato della voce di menu. Questo membro può essere una combinazione dei valori di stato (a partire da MFS) elencati con la struttura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

</dd> <dt>

**uId**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Identificatore della voce di menu. Si tratta di un valore definito dall'applicazione che identifica la voce di menu. In una risorsa di menu esteso gli elementi che aprono menu a discesa o sottomenu nonché elementi di comando possono avere identificatori.

</dd> <dt>

**wFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Specifica se la voce di menu è l'ultimo elemento della barra dei menu, il menu a discesa, il sottomenu o il menu di scelta rapida e se è un elemento che apre un menu a discesa o un sottomenu. Questo membro può essere zero o più di questi valori. Per le applicazioni a 32 bit, questo membro è una parola; per le applicazioni a 16 bit, si tratta di un byte.

<dt>

0x80
</dt> <dd>

La struttura definisce l'ultima voce di menu della barra dei menu, il menu a discesa, il sottomenu o il menu di scelta rapida.

</dd> <dt>

0x01
</dt> <dd>

La struttura definisce un elemento che apre un menu a discesa o un sottomenu. Le strutture successive definiscono le voci di menu nel menu a discesa o nel sottomenu corrispondente.

</dd> </dl> </dd> <dt>

**szText**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Testo della voce di menu. Questo membro è una stringa Unicode con terminazione null, allineata al confine di una parola. Le dimensioni della definizione della voce di menu variano a seconda della lunghezza di questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un modello di menu esteso è costituito da una struttura di [**\_ \_ intestazione del modello menuex**](menuex-template-header.md) seguita da una o più strutture di **\_ \_ elementi del modello menuex** contigue. Le strutture degli **\_ \_ elementi del modello menuex** , che sono di lunghezza variabile, sono allineate ai limiti **DWORD** . Per creare un menu da un modello di menu esteso in memoria, usare la funzione [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .

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

[**\_intestazione del modello menuex \_**](menuex-template-header.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

 





