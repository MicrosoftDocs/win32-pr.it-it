---
title: Struttura LOCALHEADER
description: Contiene le coordinate x e y di un'area sensibile associata al cursore identificato da una struttura RESDIR. La definizione della struttura qui fornita è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Struttura LOCALHEADER Menu e altre risorse
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ec46b802b847b73c99cc81939531d8f9ec1a6a2e0addb4c928d5610ac5b80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870319"
---
# <a name="localheader-structure"></a>Struttura LOCALHEADER

Contiene le coordinate x e y di un'area sensibile associata al cursore identificato da una [**struttura RESDIR.**](resdir.md) La definizione della struttura qui fornita è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**xHotSpot**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Coordinata x dell'area sensibile del cursore, in pixel.

</dd> <dt>

**yHotSpot**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Coordinata y dell'area sensibile del cursore, in pixel.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura LOCALHEADER** è il primo dato scritto nella risorsa [RT \_ CURSOR](/windows/desktop/menurc/resource-types) se una [**struttura RESDIR**](resdir.md) contiene informazioni su un cursore.

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

[**RESDIR**](resdir.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Risorse](resources.md)
</dt> </dl>

 

