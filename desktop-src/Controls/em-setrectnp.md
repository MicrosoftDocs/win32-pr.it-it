---
title: Messaggio EM_SETRECTNP (winuser. h)
description: Imposta il rettangolo di formattazione di un controllo di modifica su più righe.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- Controlli di Windows Message EM_SETRECTNP
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
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964753"
---
# <a name="em_setrectnp-message"></a>\_Messaggio SETRECTNP em

Imposta il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica su più righe. Il **messaggio \_ SETRECTNP em** è identico al [**messaggio \_ serect em**](em-setrect.md) , ad eccezione del fatto che  **em \_ SETRECTNP** non ridisegnato la finestra di controllo di modifica.

Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo. Il rettangolo di limitazione è indipendente dalle dimensioni della finestra di controllo di modifica.

Questo messaggio viene elaborato solo dai controlli di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3,0 e versioni successive:** Indica se il nuovo rettangolo contiene coordinate assolute o relative. Un valore pari a zero indica le coordinate assolute. Il valore 1 indica gli offset relativi al rettangolo di formattazione corrente. Gli offset possono essere positivi o negativi.

**Controlli di modifica:** Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo. Se questo parametro è **null**, il rettangolo di formattazione viene impostato sui valori predefiniti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Supportato in Microsoft Rich Edit 3,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[**serect EM \_**](em-setrect.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

