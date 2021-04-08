---
title: Messaggio TVM_SETBORDER (COMmctrl. h)
description: Imposta la dimensione del bordo per gli elementi in un controllo di visualizzazione albero. È possibile inviare il messaggio in modo esplicito o usando la macro del bordo del controllo TreeView \_ .
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- Controlli di Windows Message TVM_SETBORDER
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
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874013"
---
# <a name="tvm_setborder-message"></a>\_Messaggio di DEBORDO TVM

**Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.**

Imposta la dimensione del bordo per gli elementi in un controllo di visualizzazione albero. È possibile inviare il messaggio in modo esplicito o usando la macro del [**\_ bordo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) del controllo TreeView.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di azione. Il parametro può essere costituito da uno o più dei valori seguenti:



| Valore                                                                                                                                                         | Significato                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**\_XBORDER TVSBF**</dt> </dl> | Applica la dimensione del bordo specificata al lato sinistro degli elementi nel controllo di visualizzazione ad albero. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**\_YBORDER TVSBF**</dt> </dl> | Applica le dimensioni del bordo specificate alla parte superiore degli elementi nel controllo di visualizzazione ad albero.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **short** che specifica la dimensione del bordo sinistro, in pixel. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **short** che specifica la dimensione del bordo superiore, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **Long** che contiene le dimensioni del bordo precedenti, in pixel. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene le dimensioni precedenti del bordo orizzontale e il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene le dimensioni precedenti del bordo verticale.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

Il bordo dell'elemento viene impostato solo per scopi di spaziatura. Un'impostazione corretta attiva un ricalcolo delle barre di scorrimento.

Questo messaggio potrebbe non essere supportato nelle versioni future di Comctl32.dll. Inoltre, questo messaggio non è definito in commctrl. h. Aggiungere le definizioni seguenti ai file di origine dell'applicazione per usare il messaggio:

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sebordo TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

