---
title: Messaggio PSM_INDEXTOHWND (Prsht. h)
description: Accetta l'indice di una pagina della finestra delle proprietà e restituisce l'handle della finestra. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro IndexToHwnd di PropSheet.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Controlli di Windows Message PSM_INDEXTOHWND
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120826"
---
# <a name="psm_indextohwnd-message"></a>\_Messaggio INDEXTOHWND di PSM

Accetta l'indice di una pagina della finestra delle proprietà e restituisce l'handle della finestra. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ IndexToHwnd di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .

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

Restituisce l'handle per la finestra della pagina della finestra delle proprietà specificata da *wParam* in caso di esito positivo. In caso contrario, restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





