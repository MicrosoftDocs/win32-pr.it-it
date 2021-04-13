---
description: La struttura della richiesta di i/o spaventato \_ \_ inizia una struttura delle informazioni di controllo del protocollo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: Struttura SCARD_IO_REQUEST (Winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345321"
---
# <a name="scard_io_request-structure"></a>Struttura della \_ \_ richiesta di i/o spaventato

La struttura della **\_ \_ richiesta** di i/o spaventato inizia una struttura delle informazioni di controllo del protocollo. Tutte le informazioni specifiche del protocollo seguono immediatamente la struttura. L'intera lunghezza della struttura deve essere allineata con le dimensioni della parola dell'architettura hardware sottostante. Ad esempio, in Win32 la lunghezza di qualsiasi informazione PCI deve essere un multiplo di quattro byte, in modo che venga allineata a un limite di 32 bit.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a>Members

<dl> <dt>

**dwProtocol**
</dt> <dd>

Protocollo in uso.

</dd> <dt>

**cbPciLength**
</dt> <dd>

Lunghezza, in byte, della struttura della **\_ \_ richiesta** di i/o spaventato più le informazioni specifiche di PCI seguenti.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winsmcrd. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




