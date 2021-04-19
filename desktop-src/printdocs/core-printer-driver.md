---
description: Rappresenta un driver della stampante da cui dipendono altri driver della stampante.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Struttura CORE_PRINTER_DRIVER (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311829"
---
# <a name="core_printer_driver-structure"></a>\_Struttura driver della stampante principale \_

Rappresenta un driver della stampante da cui dipendono altri driver della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a>Members

<dl> <dt>

**CoreDriverGUID**
</dt> <dd>

GUID del driver della stampante principale.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Data e ora dell'ultima versione del driver della stampante principale.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

ID versione della versione più recente del driver della stampante principale.

</dd> <dt>

**\[percorso massimo \_ szPackageID\]**
</dt> <dd>

Percorso del pacchetto driver che contiene il driver della stampante principale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura può rappresentare un driver di base del produttore su cui dipendono i driver per diversi modelli di stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Core \_ Printer \_ DRIVERW** (Unicode) e **\_ Core \_ Printer \_ drivera** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




