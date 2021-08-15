---
title: LM_GETIDEALSIZE messaggio (Commctrl.h)
description: "LM_GETIDEALSIZE messaggio: recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo."
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035a919aabeb5d07587c7d9e4fc97e5edc728de4ec8fc476448dca62658f1ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958375"
---
# <a name="lm_getidealsize-message"></a>Messaggio \_ LM GETIDEALSIZE

Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Larghezza massima del collegamento, in pixel.</dd> <dt>

*lParam* \[ Cambio\]
</dt> <dd>Quando il messaggio viene restituito, contiene un puntatore a una <a href="/previous-versions//dd145106(v=vs.85)">**struttura SIZE.**</a> Il **membro cy** di questa struttura indica l'altezza ideale del controllo per la larghezza specificata. Regola il membro **cx** in base alla quantità di spazio effettivamente necessaria.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Intero che rappresenta l'altezza preferita del testo del collegamento, in pixel.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

