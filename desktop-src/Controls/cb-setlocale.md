---
title: Messaggio CB_SETLOCALE (winuser. h)
description: Un'applicazione invia un \_ messaggio setlocale di CB per impostare le impostazioni locali correnti della casella combinata. Se la casella combinata ha lo \_ stile di ordinamento CBS e le stringhe vengono aggiunte tramite CB \_ ADDSTRING, le impostazioni locali di una casella combinata influiscono sulla modalità di ordinamento degli elementi dell'elenco.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- Controlli di Windows Message CB_SETLOCALE
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477650"
---
# <a name="cb_setlocale-message"></a>\_Messaggio setlocale di CB

Un'applicazione invia un **messaggio \_ setlocale di CB** per impostare le impostazioni locali correnti della casella combinata. Se la casella combinata ha lo stile di [**\_ ordinamento CBS**](combo-box-styles.md) e le stringhe vengono aggiunte tramite [**CB \_ ADDSTRING**](cb-addstring.md), le impostazioni locali di una casella combinata influiscono sulla modalità di ordinamento degli elementi dell'elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali per la casella combinata da usare per l'ordinamento quando si aggiunge il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'identificatore delle impostazioni locali precedente. Se *wParam* specifica le impostazioni locali non installate nel sistema, il valore restituito è CB \_ Err e le impostazioni locali correnti della casella combinata non vengono modificate.

## <a name="remarks"></a>Commenti

Usare la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) per creare un identificatore delle impostazioni locali e la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) per costruire un identificatore di lingua. L'identificatore di lingua è costituito da un identificatore di lingua principale e da un identificatore di lingua.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETlocale**](cb-getlocale.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

