---
title: Struttura CURSORDIR
description: Contiene le dimensioni di una singola immagine del cursore in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menu struttura CURSORDIR e altre risorse
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400858"
---
# <a name="cursordir-structure"></a>Struttura CURSORDIR

Contiene le dimensioni di una singola immagine del cursore in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Larghezza, in pixel, del cursore. I valori accettabili sono 16, 32 e 64.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Altezza, in pixel, del cursore. I valori accettabili sono 16, 32 e 64.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **CURSORDIR** viene passata nella struttura [**RESDIR**](resdir.md) se la struttura **RESDIR** descrive un cursore.

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

 

 





