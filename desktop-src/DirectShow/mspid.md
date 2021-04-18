---
description: Nota Questa API è deprecata. Le nuove applicazioni non devono utilizzarlo. Il tipo di dati MSPID identifica lo scopo di un flusso multimediale.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330925"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Questa API è deprecata. Le nuove applicazioni non devono utilizzarlo.

 

Il tipo di dati **MSPID** identifica lo scopo di un flusso multimediale.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Commenti

**MSPID** è semplicemente un typedef per GUID. Sono definiti i seguenti MSPIDs.



| Valore               | Descrizione           |
|---------------------|-----------------------|
| \_PRIMARYVIDEO MSPID | Flusso video primario. |
| \_PRIMARYAUDIO MSPID | Flusso audio primario. |



 

Il tipo **REFMSPID** definisce un riferimento a un **MSPID**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mmstream. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati di streaming multimediali](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




