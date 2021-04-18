---
title: Messaggio PSM_RECALCPAGESIZES (Prsht. h)
description: Ricalcola le dimensioni di pagina di una finestra delle proprietà standard o della procedura guidata dopo l'aggiunta o la rimozione di pagine. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro RecalcPageSizes di PropSheet.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- Controlli di Windows Message PSM_RECALCPAGESIZES
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302198"
---
# <a name="psm_recalcpagesizes-message"></a>\_Messaggio RECALCPAGESIZES di PSM

Ricalcola le dimensioni di pagina di una finestra delle proprietà standard o della procedura guidata dopo l'aggiunta o la rimozione di pagine. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ RecalcPageSizes di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .

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

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Quando viene creata, una finestra delle proprietà viene ridimensionata per adattarsi alla raccolta iniziale di pagine. Per mantenere la compatibilità con le versioni precedenti dei controlli comuni, le finestre delle proprietà e le procedure guidate non si ridimensionano automaticamente quando le pagine vengono aggiunte o rimosse. Con i controlli comuni [versione 5,80](common-control-versions.md), le applicazioni devono inviare un messaggio **PSM \_ RECALCPAGESIZES** dopo l'aggiunta o la rimozione di pagine con [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)o le macro equivalenti. Garantisce che la finestra delle proprietà sia dimensionata correttamente per la raccolta di pagine corrente. Se il messaggio non viene inviato, è possibile che alcune pagine della finestra delle proprietà vengano troncate o troppo grandi.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





