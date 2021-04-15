---
title: Costanti GXFPF_ (Textstor. h)
description: GXFPF \_ \ Constants consente di specificare la posizione del carattere da restituire in base alle coordinate dello schermo del punto rispetto a un rettangolo delimitatore di caratteri.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475814"
---
# <a name="gxfpf_-constants"></a>\_ \* Costanti GXFPF

Le \_ \* costanti GXFPF specificano la posizione del carattere da restituire in base alle coordinate dello schermo del punto rispetto a un rettangolo delimitatore di caratteri.



| Costante/valore                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**GXFPF \_ ROUND \_ più vicino**</dt> <dt>(0x1)</dt> </dl> | Se le coordinate dello schermo del punto sono contenute in un rettangolo delimitatore di caratteri, la posizione del carattere restituita è il bordo delimitatore più vicino alle coordinate dello schermo del punto.<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**GXFPF \_ PIÙ vicino**</dt> <dt>(0x2)</dt> </dl>                    | Se le coordinate dello schermo del punto non sono contenute in un rettangolo delimitatore di caratteri, viene restituita la posizione del carattere più vicina.<br/>                                                      |



## <a name="remarks"></a>Commenti

I parametri *dwFlags* dei metodi [ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) e [ITfContextOwner:: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) usano queste costanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





