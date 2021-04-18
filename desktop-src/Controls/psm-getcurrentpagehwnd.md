---
title: Messaggio PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Recupera un handle per la finestra della pagina corrente di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Controlli di Windows Message PSM_GETCURRENTPAGEHWND
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302200"
---
# <a name="psm_getcurrentpagehwnd-message"></a>\_Messaggio GETCURRENTPAGEHWND di PSM

Recupera un handle per la finestra della pagina corrente di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle per la finestra della pagina della finestra delle proprietà corrente.

## <a name="remarks"></a>Commenti

Usare il messaggio **PSM \_ GETCURRENTPAGEHWND** con le finestre delle proprietà non modali per determinare quando eliminare la finestra di dialogo. Quando l'utente fa clic sul pulsante **OK** o **Annulla** , **PSM \_ GETCURRENTPAGEHWND** restituisce **null** ed è quindi possibile usare la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) per eliminare definitivamente la finestra di dialogo.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

