---
title: CB_SETLOCALE messaggio (Winuser.h)
description: Un'applicazione invia un messaggio \_ CB SETLOCALE per impostare le impostazioni locali correnti della casella combinata. Se la casella combinata ha lo stile CBS SORT e le stringhe vengono aggiunte usando CB ADDSTRING, le impostazioni locali di una casella combinata influiscono sull'ordinamento \_ \_ degli elementi dell'elenco.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE dei messaggi Windows controlli
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
ms.openlocfilehash: ef1647d8ff4c7a4625151a9ec099800549d831f6b55a7ef6cc6b5ead365e80e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063302"
---
# <a name="cb_setlocale-message"></a>Messaggio \_ CB SETLOCALE

Un'applicazione invia un **messaggio \_ CB SETLOCALE** per impostare le impostazioni locali correnti della casella combinata. Se la casella combinata ha lo stile [**CBS \_ SORT**](combo-box-styles.md) e le stringhe vengono aggiunte usando [**CB \_ ADDSTRING,**](cb-addstring.md)le impostazioni locali di una casella combinata influiscono sull'ordinamento degli elementi dell'elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali per la casella combinata da utilizzare per l'ordinamento quando si aggiunge testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'identificatore delle impostazioni locali precedente. Se *wParam specifica* impostazioni locali non installate nel sistema, il valore restituito è CB ERR e le impostazioni locali correnti della casella combinata \_ non vengono modificate.

## <a name="remarks"></a>Commenti

Usare la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) per costruire un identificatore delle impostazioni locali e la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) per costruire un identificatore di lingua. L'identificatore di lingua è costituito da un identificatore di lingua principale e da un identificatore di sottolinguaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETLOCALE**](cb-getlocale.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

