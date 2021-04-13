---
title: Messaggio LM_GETIDEALSIZE (COMmctrl. h)
description: Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- Controlli di Windows Message LM_GETIDEALSIZE
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
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475208"
---
# <a name="lm_getidealsize-message"></a>\_Messaggio GETIDEALSIZE LM

Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Larghezza massima del collegamento, in pixel.</dd> <dt>

*lParam* \[ out\]
</dt> <dd>Quando il messaggio viene restituito, contiene un puntatore a una struttura di <a href="/previous-versions//dd145106(v=vs.85)">**dimensioni**</a> . Il membro **CY** di questa struttura indica l'altezza ideale del controllo per la larghezza specificata. Imposta il membro **CX** sulla quantità di spazio effettivamente necessaria.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Intero che rappresenta l'altezza preferita del testo del collegamento, in pixel.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

