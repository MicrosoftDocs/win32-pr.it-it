---
description: La \_ struttura Printer Info \_ 3 specifica le informazioni di sicurezza della stampante.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Struttura PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315982"
---
# <a name="printer_info_3-structure"></a>\_Struttura Info stampante \_ 3

La struttura **Printer \_ info \_ 3** specifica le informazioni di sicurezza della stampante.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>Members

<dl> <dt>

**pSecurityDescriptor**
</dt> <dd>

Puntatore a una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che specifica le informazioni di sicurezza di una stampante.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **Printer \_ info \_ 3** consente a un'applicazione di ottenere e impostare il descrittore di sicurezza di una stampante. Il chiamante può eseguire questa operazione anche se non dispone di autorizzazioni specifiche per la stampante, purché disponga dei diritti standard descritti in [**Seprinter**](setprinter.md) e [**GetPrinter**](getprinter.md). Pertanto, un'applicazione può negare temporaneamente l'accesso a una stampante, consentendo al proprietario della stampante di accedere all'ACL discrezionale della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Informazioni stampante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> <dt>

[**descrittore di sicurezza \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

