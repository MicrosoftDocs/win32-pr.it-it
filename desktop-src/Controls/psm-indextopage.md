---
title: Messaggio PSM_INDEXTOPAGE (Prsht. h)
description: Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo handle HPROPSHEETPAGE. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IndexToPage di PropSheet.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Controlli di Windows Message PSM_INDEXTOPAGE
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478239"
---
# <a name="psm_indextopage-message"></a>\_Messaggio INDEXTOPAGE di PSM

Accetta l'indice di una pagina della finestra delle proprietà e restituisce il relativo handle HPROPSHEETPAGE. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToPage di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della pagina.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle HPROPSHEETPAGE della pagina della finestra delle proprietà specificata da *wParam* se ha esito positivo. In caso contrario, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





