---
title: Struttura MPSTATUS_DATA (MpClient. h)
description: Contiene dati sullo stato corrente di un componente del prodotto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- Struttura MPSTATUS_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSTATUS_DATA
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742303"
---
# <a name="mpstatus_data-structure"></a>\_Struttura dei dati MPSTATUS

Contiene dati sullo stato corrente di un componente del prodotto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ComponentID**
</dt> <dd>

Tipo: **[ **MPCOMPONENT \_ ID**](mpcomponent-id.md)**

</dd> <dd>

ID componente specifico per il quale viene segnalato lo stato.

</dd> <dt>

**fEnable**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

Stato richiesto per il componente. **HRESULT** nei dati di callback indica l'esito positivo o negativo della richiesta.

</dd> <dt>

**ComponentStatus**
</dt> <dd>

Dati di stato aggiuntivi a seconda del valore di **ComponentID**.

> [!Note]  
> Attualmente produce un puntatore a una struttura fittizia per tutti i possibili valori di **ComponentID**.

 

<dl> <dt>

**P1**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ As \_ Signature**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P2**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ AV \_ Signature**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P3**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ realtime \_ Monitor**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P4**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ onaccess \_ Protection**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P5**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ Protection**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P6**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ Behavior \_ Monitor**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P7**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ auto \_ Scan**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P8**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ auto \_ SIGUPDATE**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**P9**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ IPC**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**pa**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ NIS**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> <dt>

**PB**
</dt> <dd>

Tipo: **PMPSTATUS \_ DATAEX non \_ usato**

</dd> <dd>

Quando **ComponentID**  ==  **MPCOMPONENT \_ Elam**. Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ID MPCOMPONENT**](mpcomponent-id.md)
</dt> <dt>

[**MPSTATUS \_ DATAEX non \_ usato**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





