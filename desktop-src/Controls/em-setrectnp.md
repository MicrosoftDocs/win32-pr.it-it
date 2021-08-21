---
title: EM_SETRECTNP messaggio (Winuser.h)
description: 'EM_SETRECTNP: imposta il rettangolo di formattazione di un controllo di modifica su più righe.'
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60341a41706f012064d3b7cbc79aa019f1492c3a8d535866fa51fc7ea8dfd437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831132"
---
# <a name="em_setrectnp-message"></a>Messaggio EM \_ SETRECTNP

Imposta il rettangolo [di formattazione](about-edit-controls.md) di un controllo di modifica su più righe. Il **messaggio EM \_ SETRECTNP** è identico al messaggio [**EM \_ SETRECT,**](em-setrect.md)  ad eccezione del fatto che **EM \_ SETRECTNP** non ridisegna la finestra del controllo di modifica.

Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo. Il rettangolo di limitazione è indipendente dalle dimensioni della finestra del controllo di modifica.

Questo messaggio viene elaborato solo da controlli di modifica su più righe. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3.0 e versioni successive:** Indica se il nuovo rettangolo contiene coordinate assolute o relative. Il valore zero indica coordinate assolute. Il valore 1 indica gli offset rispetto al rettangolo di formattazione corrente. Gli offset possono essere positivi o negativi.

**Controlli di modifica:** Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo. Se questo parametro è **NULL,** il rettangolo di formattazione viene impostato su valori predefiniti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

**Rich Edit:** Supportato in Microsoft Rich Edit 3.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

