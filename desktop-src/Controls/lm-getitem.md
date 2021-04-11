---
title: Messaggio LM_GETITEM (COMmctrl. h)
description: Recupera gli Stati e gli attributi di un elemento.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- Controlli di Windows Message LM_GETITEM
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119026"
---
# <a name="lm_getitem-message"></a>\_Messaggio GETitem di LM

Recupera gli Stati e gli attributi di un elemento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere **null**. </dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litey</a> da riempire con le informazioni sull'elemento. </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il messaggio riesce a ottenere i valori e gli attributi specificati.

## <a name="remarks"></a>Commenti

Con il messaggio **LM \_ GetItem** , è possibile accedere ai collegamenti solo tramite l'indice numerico restituito nel membro **iLink** di [**liteo**](/windows/win32/api/commctrl/ns-commctrl-litem). L'accesso al collegamento tramite il nome ID restituito in **szId** non è supportato.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





