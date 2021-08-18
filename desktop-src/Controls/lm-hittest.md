---
title: LM_HITTEST messaggio (Commctrl.h)
description: Determina se l'utente ha fatto clic sul collegamento specificato.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 559ea1500c7270ece1785391777133bdaaeb1e95e5b01fa5ca7d4bb76e40f1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958376"
---
# <a name="lm_hittest-message"></a>Messaggio LM \_ HITTEST

Determina se l'utente ha fatto clic sul collegamento specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere **NULL.**</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**una struttura LHITTESTINFO**</a> da riempire con le informazioni sul collegamento su cui l'utente ha fatto clic, se presente. </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'utente ha fatto clic su un collegamento; in caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Se il **messaggio LM \_ HITTEST** ha esito positivo, il sistema inserisce [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) e **LITEM.szID**. Se il **messaggio LM \_ HITTEST** ha esito negativo, non presupporre che le informazioni in **LITEM** siano valide.

> [!Note]  
> Per usare questa API, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





