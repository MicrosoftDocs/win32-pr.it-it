---
title: Struttura ICONRESDIR
description: Contiene le dimensioni e il formato del colore di una singola immagine di icona in un gruppo di risorse. La definizione della struttura fornita qui è solo a solo supporto della spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Struttura ICONRESDIR Menu e altre risorse
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f81f8b0a530e7c6c85f2ad1749e0a7373f68b0bf902b71a86889b92184806ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034279"
---
# <a name="iconresdir-structure"></a>Struttura ICONRESDIR

Contiene le dimensioni e il formato del colore di una singola immagine di icona in un gruppo di risorse. La definizione della struttura fornita qui è solo a solo supporto della spiegazione. non è presente in alcun file di intestazione standard.

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

Tipo: **BYTE**

</dd> <dd>

Larghezza dell'icona, in pixel. I valori accettabili sono 16, 32 e 64.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Altezza, in pixel, dell'icona. I valori accettabili sono 16, 32 e 64.

</dd> <dt>

**Conteggio colori**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Numero di colori nell'icona. I valori accettabili sono 2, 8 e 16.

</dd> <dt>

**Riservati**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Riservato; deve essere impostato sullo stesso valore del campo riservato nell'intestazione del file icona.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura ICONRESDIR** viene passata nella [**struttura RESDIR**](resdir.md) se la **struttura RESDIR** descrive un'icona.

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

 

 





