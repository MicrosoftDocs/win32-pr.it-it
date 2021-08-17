---
title: TB_SETMETRICS messaggio (Commctrl.h)
description: Imposta le metriche di un controllo barra degli strumenti.
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- TB_SETMETRICS dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c152d0fd1bfef894b1d54db768984697ebef2c9b82ac6d2663401363a338b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967911"
---
# <a name="tb_setmetrics-message"></a>Tb \_ SETMETRICS message (TB SETMETRICS message)

Imposta le metriche di un controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Struttura TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) che contiene le metriche della barra degli strumenti da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





