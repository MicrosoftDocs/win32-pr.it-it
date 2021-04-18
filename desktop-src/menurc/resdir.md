---
title: Struttura RESDIR
description: Contiene informazioni su un singolo componente icona o cursore in un gruppo di risorse. Esiste una struttura RESDIR per ogni componente del gruppo. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menu struttura RESDIR e altre risorse
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301195"
---
# <a name="resdir-structure"></a>Struttura RESDIR

Contiene informazioni su un singolo componente icona o cursore in un gruppo di risorse. Esiste una struttura **RESDIR** per ogni componente del gruppo. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a>Members

<dl> <dt>

**Icona**
</dt> <dd>

Tipo: **[ **ICONRESDIR**](iconresdir.md)**

</dd> <dd>

Larghezza, altezza e numero di colori dell'icona indicata.

</dd> <dt>

**Cursore**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Larghezza e altezza del cursore indicato.

</dd> <dt>

**Aerei**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Numero di piani di colore nell'icona o nella bitmap del cursore.

</dd> <dt>

**BitCount**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Numero di bit per pixel nell'icona o nella bitmap del cursore.

</dd> <dt>

**BytesInRes**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Dimensioni in byte della risorsa.

</dd> <dt>

**IconCursorId**
</dt> <dd>

Tipo: **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Icona o cursore con un identificatore ordinale univoco.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una o più strutture **RESDIR** seguono immediatamente la struttura [**NEWHEADER**](newheader.md) nel file res. Il membro **ResCount** della struttura **NEWHEADER** specifica il numero di strutture **RESDIR** . Si noti che la struttura **RESDIR** è costituita da una struttura [**ICONRESDIR**](iconresdir.md) o da una struttura [**CURSORDIR**](cursordir.md) seguita dai membri **Planes**, **BitCount**, **BytesInRes** e **IconCursorId** . Se la struttura **RESDIR** contiene informazioni su un cursore, le prime due **parole** il compilatore di risorse scrive nella risorsa [del \_ cursore RT](/windows/desktop/menurc/resource-types) sono i membri **xHotSpot** e **yHotSpot** della struttura [**LOCALHEADER**](localheader.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**ICONRESDIR**](iconresdir.md)
</dt> <dt>

[**LOCALHEADER**](localheader.md)
</dt> <dt>

[**NEWHEADER**](newheader.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

