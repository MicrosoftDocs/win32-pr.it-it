---
title: Messaggio PSM_PAGETOINDEX (Prsht. h)
description: Accetta l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro PageToIndex di PropSheet.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- Controlli di Windows Message PSM_PAGETOINDEX
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301837"
---
# <a name="psm_pagetoindex-message"></a>\_Messaggio PAGETOINDEX di PSM

Accetta l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PageToIndex di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle HPROPSHEETPAGE per la pagina della finestra delle proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero della pagina della finestra delle proprietà specificato da *lParam* se ha esito positivo. In caso contrario, restituisce -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





