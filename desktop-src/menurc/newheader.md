---
title: Struttura NEWHEADER
description: Contiene il numero di componenti icona o cursore in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menu struttura NEWHEADER e altre risorse
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963896"
---
# <a name="newheader-structure"></a>Struttura NEWHEADER

Contiene il numero di componenti icona o cursore in un gruppo di risorse. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Reserved**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Riservati deve essere zero.

</dd> <dt>

**ResType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tipo di risorsa. Questo membro deve avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <dt>**Res \_ CURSORE**</dt> <dt>2</dt> </dl> | Tipo di risorsa Cursor.<br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <dt>**Res \_ ICONA**</dt> <dt>1</dt> </dl>       | Tipo di risorsa icona.<br/>   |



 

</dd> <dt>

**ResCount**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di componenti icona o cursore nel gruppo di risorse.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una o più strutture [**RESDIR**](resdir.md) seguono immediatamente la struttura **NEWHEADER** nel file res. Il membro **ResCount** specifica il numero di strutture **RESDIR** .

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

 

 





