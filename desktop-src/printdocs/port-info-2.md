---
description: La struttura della porta \_ info \_ 2 identifica una porta stampante supportata.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Struttura PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314532"
---
# <a name="port_info_2-structure"></a>Struttura delle informazioni sulla porta \_ \_ 2

La struttura della **porta \_ info \_ 2** identifica una porta stampante supportata.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**pPortName**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica una porta stampante supportata (ad esempio, "LPT1:").

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica un monitoraggio installato (ad esempio, "monitoraggio PJL"). Può essere **null**.

</dd> <dt>

**pDescription**
</dt> <dd>

Puntatore a una stringa con terminazione null che descrive la porta in modo più dettagliato (ad esempio, se **pPortName** è "LPT1:", **pDescription** è "Printer Port"). Può essere **null**.

</dd> <dt>

**fPortType**
</dt> <dd>

Maschera di maschera che descrive il tipo di porta. Questo membro può essere una combinazione dei valori seguenti:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**\_scrittura tipo \_ porta**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**\_tipo porta \_ letto**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**tipo di porta \_ \_ reindirizzato**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**tipo di porta \_ \_ net \_ Attached**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Riservati deve essere zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Utilizzare la struttura **Port \_ info \_ 2** quando si chiama [**EnumPorts**](enumports.md) se sono installati più monitor che supportano le stesse porte.

È possibile eseguire una query sul membro **fPortType** per determinare le informazioni sulla porta. Si noti che le impostazioni della porta non influenzano gli attributi della stampante (restituiti dal membro **Attributes** di [**Printer \_ info \_ 2**](printer-info-2.md)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info porta \_ 2W** (Unicode) e **\_ porta \_ info \_ 2a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




