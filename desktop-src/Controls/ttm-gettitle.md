---
title: TTM_GETTITLE messaggio (Commctrl.h)
description: Recuperare informazioni relative al titolo di un controllo descrizione comando.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- TTM_GETTITLE controlli Windows messaggio
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242e20f3360caac03874524df38267fc0b103ec8f1c04d8d30df106fc9c65ac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797441"
---
# <a name="ttm_gettitle-message"></a>Messaggio \_ GETTITLE TTM

Recuperare informazioni relative al titolo di un controllo descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) che contiene informazioni sul titolo di una descrizione comando.

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



 

 





