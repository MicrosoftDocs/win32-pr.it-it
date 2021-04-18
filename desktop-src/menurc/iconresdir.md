---
title: Struttura ICONRESDIR
description: Contiene le dimensioni e il formato colori di una singola immagine dell'icona in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menu struttura ICONRESDIR e altre risorse
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301768"
---
# <a name="iconresdir-structure"></a>Struttura ICONRESDIR

Contiene le dimensioni e il formato colori di una singola immagine dell'icona in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Larghezza, in pixel, dell'icona. I valori accettabili sono 16, 32 e 64.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Altezza, in pixel, dell'icona. I valori accettabili sono 16, 32 e 64.

</dd> <dt>

**ColorCount**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Il numero di colori nell'icona. I valori accettabili sono 2, 8 e 16.

</dd> <dt>

**riservati**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Riservati deve essere impostato sullo stesso valore di quello del campo riservato nell'intestazione del file icona.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **ICONRESDIR** viene passata nella struttura [**RESDIR**](resdir.md) se la struttura **RESDIR** descrive un'icona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

 





