---
title: Messaggio PSM_SETCURSEL (Prsht. h)
description: Attiva la pagina specificata in una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- Controlli di Windows Message PSM_SETCURSEL
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119575"
---
# <a name="psm_setcursel-message"></a>\_Messaggio di RImaledizione di PSM

Attiva la pagina specificata in una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della pagina. Un'applicazione può specificare l'indice o l'handle o entrambi. Se vengono specificati entrambi, *lParam* avrà la precedenza.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle della pagina da attivare. Un'applicazione può specificare l'indice o l'handle o entrambi. Se vengono specificati entrambi, *lParam* avrà la precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La finestra che sta per perdere l'attivazione riceve il codice di notifica [ \_ KILLACTIVE PSN](psn-killactive.md) e la finestra che sta ottenendo l'attivazione riceve il codice di notifica [ \_ seattivo PSN](psn-setactive.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





