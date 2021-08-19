---
description: La struttura PRINTER \_ INFO \_ 3 specifica le informazioni di sicurezza della stampante.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: PRINTER_INFO_3 struttura (Winspool.h)
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
ms.openlocfilehash: c6b9bc249921b3247f5df898c2810d735dc1a75c8e643e965b3fd249d9496f78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867926"
---
# <a name="printer_info_3-structure"></a>Struttura PRINTER \_ INFO \_ 3

La **struttura PRINTER INFO \_ \_ 3** specifica le informazioni di sicurezza della stampante.

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

Puntatore a [**una struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che specifica le informazioni di sicurezza di una stampante.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura PRINTER INFO \_ \_ 3** consente a un'applicazione di ottenere e impostare il descrittore di sicurezza di una stampante. Il chiamante può eseguire questa operazione anche se non dispone di autorizzazioni specifiche per la stampante, purché abbia i diritti standard descritti in [**SetPrinter**](setprinter.md) e [**GetPrinter**](getprinter.md). Di conseguenza, un'applicazione può negare temporaneamente l'accesso a una stampante, consentendo al proprietario della stampante di accedere all'ACL discrezionale della stampante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 1**](printer-info-1.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAZIONI \_ SULLA \_ STAMPANTE 4**](printer-info-4.md)
</dt> <dt>

[**DESCRITTORE \_ DI SICUREZZA**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

