---
title: TB_SETBOUNDINGSIZE messaggio (Commctrl.h)
description: Imposta le dimensioni di delimitazione per un controllo barra degli strumenti a più colonne.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d409769e08e489d922dbdc2361779953555000dca784a6f7b977bbbcd3a5e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167744"
---
# <a name="tb_setboundingsize-message"></a>TB \_ SETBOUNDINGSIZE message

\[Destinato all'uso interno; non consigliato per l'uso nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Imposta le dimensioni di delimitazione per un controllo barra degli strumenti a più colonne.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura SIZE**](/previous-versions//dd145106(v=vs.85)) il cui **membro cy** contiene l'altezza di delimitazione. Il **membro cx** (larghezza) viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

Le dimensioni di delimitazione controllano l'organizzazione dei pulsanti in colonne. Se il controllo barra degli strumenti non ha lo stile [**TBSTYLE \_ EX \_ MULTICOLUMN,**](toolbar-extended-styles.md) questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

