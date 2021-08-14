---
description: La struttura PORT \_ INFO \_ 2 identifica una porta della stampante supportata.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: PORT_INFO_2 (Winspool.h)
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
ms.openlocfilehash: 053745ff90e022ef2ed466518a9210d6dde18d3562fdb4232d9f4d262460ea7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470941"
---
# <a name="port_info_2-structure"></a>Struttura PORT \_ INFO \_ 2

La **struttura PORT INFO \_ \_ 2** identifica una porta della stampante supportata.

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

Puntatore a una stringa con terminazione Null che identifica una porta della stampante supportata, ad esempio "LPT1:".

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che identifica un monitoraggio installato, ad esempio "monitoraggio PJL". Può essere **NULL.**

</dd> <dt>

**pDescription**
</dt> <dd>

Puntatore a una stringa con terminazione Null che descrive la porta in modo più dettagliato(ad esempio, se **pPortName** è "LPT1:", **pDescription** è "porta stampante"). Può essere **NULL.**

</dd> <dt>

**fPortType**
</dt> <dd>

Maschera di bit che descrive il tipo di porta. Questo membro può essere una combinazione dei valori seguenti:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**TIPO \_ DI \_ PORTA WRITE**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**TIPO \_ DI \_ PORTA READ**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**TIPO \_ DI PORTA \_ REINDIRIZZATO**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**TIPO \_ DI PORTA NET \_ \_ COLLEGATA**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Riservato; deve essere zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare la **struttura PORT \_ INFO \_ 2** quando si [**chiama EnumPorts**](enumports.md) se sono installati più monitor che supportano le stesse porte.

È possibile eseguire query sul membro **fPortType** per determinare le informazioni sulla porta. Si noti che le impostazioni della porta non influenzano gli attributi della stampante (come restituito dal **membro Attributes** di PRINTER [**INFO \_ \_ 2).**](printer-info-2.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ PORT \_ INFO \_ 2W** (Unicode) e **\_ PORT INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




