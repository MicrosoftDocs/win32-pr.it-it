---
title: LM_GETIDEALSIZE messaggio (Commctrl.h)
description: "LM_GETIDEALSIZE messaggio: recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo."
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE di windows del messaggio
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
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112389"
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
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

