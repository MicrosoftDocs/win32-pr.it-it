---
description: Nota Questa API è deprecata. Le nuove applicazioni non devono usarlo. Il tipo di dati MSPID identifica lo scopo di un flusso multimediale.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9d274fc4131c0aa4494d610cbe1145ad79b848b5f6280d4ad6a10b298a8b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075751"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Questa API è deprecata. Le nuove applicazioni non devono usarlo.

 

Il **tipo di dati MSPID** identifica lo scopo di un flusso multimediale.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Commenti

**MSPID** è semplicemente un typedef per GUID. Sono definiti gli MSPID seguenti.



| Valore               | Descrizione           |
|---------------------|-----------------------|
| MSPID \_ PrimaryVideo | Flusso video primario. |
| MSPID \_ PrimaryAudio | Flusso audio primario. |



 

Il **tipo REFMSPID** definisce un riferimento a un **MSPID**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mmstream.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati di streaming multimediali](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




