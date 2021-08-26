---
description: Rappresenta un driver della stampante da cui dipendono altri driver della stampante.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: CORE_PRINTER_DRIVER (Winspool.h)
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
ms.openlocfilehash: 18ac3dba88d9cf781393b01b6594777426b7195e6f68afa0fd00a5bddb01f129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950401"
---
# <a name="core_printer_driver-structure"></a>Struttura CORE \_ PRINTER \_ DRIVER

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

**Guida di base**
</dt> <dd>

GUID del driver della stampante principale.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Data e ora dell'ultima versione del driver della stampante principale.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

ID della versione più recente del driver della stampante principale.

</dd> <dt>

**szPackageID \[ MAX \_ PATH\]**
</dt> <dd>

Percorso del pacchetto driver che contiene il driver principale della stampante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura può rappresentare il driver di base del produttore da cui dipendono i driver per vari modelli di stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ CORE \_ PRINTER \_ DRIVERW** (Unicode) e **\_ CORE PRINTER \_ \_ DRIVERA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




