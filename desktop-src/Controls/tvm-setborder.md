---
title: TVM_SETBORDER messaggio (Commctrl.h)
description: Imposta le dimensioni del bordo per gli elementi in un controllo di visualizzazione albero. È possibile inviare il messaggio in modo esplicito o usando la \_ macro TreeView SetBorder.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER del messaggio Windows controlli
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1c8cab133fb654e431638be96301325d68d9743109f84ed8def1ee9cc67c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669656"
---
# <a name="tvm_setborder-message"></a>Messaggio \_ TVM SETBORDER

**Destinato all'uso interno; non consigliato per l'uso nelle applicazioni.**

Imposta le dimensioni del bordo per gli elementi in un controllo di visualizzazione albero. È possibile inviare il messaggio in modo esplicito o usando la macro [**\_ TreeView SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di azione. Questo parametro può essere uno o più dei valori seguenti:



| Valore                                                                                                                                                         | Significato                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**TVSBF \_ XBORDER**</dt> </dl> | Applica le dimensioni del bordo specificate al lato sinistro degli elementi nel controllo di visualizzazione albero. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**TVSBF \_ YBORDER**</dt> </dl> | Applica le dimensioni del bordo specificate alla parte superiore degli elementi nel controllo di visualizzazione albero.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un **valore SHORT** che specifica le dimensioni del bordo sinistro, in pixel. HIWORD [**è**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un **valore SHORT** che specifica le dimensioni del bordo superiore, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore LONG** che contiene le dimensioni del bordo precedenti, in pixel. LoWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) le dimensioni precedenti del bordo orizzontale e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene le dimensioni precedenti del bordo verticale.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

Il bordo dell'elemento viene impostato solo a scopo di spaziatura. Un'impostazione riuscita attiva un ricalcolo delle barre di scorrimento.

Questo messaggio potrebbe non essere supportato nelle versioni future di Comctl32.dll. Inoltre, questo messaggio non è definito in commctrl.h. Aggiungere le definizioni seguenti ai file di origine dell'applicazione per usare il messaggio:

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

