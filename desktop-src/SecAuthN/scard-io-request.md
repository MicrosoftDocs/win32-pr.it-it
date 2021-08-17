---
description: La struttura SCARD \_ IO REQUEST inizia una struttura di informazioni di controllo del \_ protocollo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: SCARD_IO_REQUEST struttura (Winsmcrd.h)
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
ms.openlocfilehash: 9a377643e794b679be593bb99b8750698c92dd3aa8abacd79bfdb1c478c9c7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918887"
---
# <a name="scard_io_request-structure"></a>Struttura \_ SCARD IO \_ REQUEST

La **struttura SCARD \_ IO \_ REQUEST** inizia una struttura di informazioni di controllo del protocollo. Tutte le informazioni specifiche del protocollo seguono quindi immediatamente questa struttura. L'intera lunghezza della struttura deve essere allineata alle dimensioni delle parole dell'architettura hardware sottostante. Ad esempio, in Win32 la lunghezza di tutte le informazioni PCI deve essere un multiplo di quattro byte in modo che sia allineata su un limite a 32 bit.

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

Lunghezza, in byte, della **struttura \_ SCARD IO \_ REQUEST** più le informazioni specifiche di PCI seguenti.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winsmcrd.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




