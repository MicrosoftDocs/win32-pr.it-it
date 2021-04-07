---
title: Messaggio TB_SETBOUNDINGSIZE (COMmctrl. h)
description: Imposta la dimensione di delimitazione per un controllo della barra degli strumenti a più colonne.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- Controlli di Windows Message TB_SETBOUNDINGSIZE
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
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873285"
---
# <a name="tb_setboundingsize-message"></a>TB \_ SETBOUNDINGSIZE messaggio

\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Imposta la dimensione di delimitazione per un controllo della barra degli strumenti a più colonne.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) il cui membro **CY** contiene l'altezza di delimitazione. Il membro **CX** (la larghezza) viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

La dimensione di delimitazione controlla la modalità di organizzazione dei pulsanti in colonne. Se il controllo Toolbar non ha lo stile [**\_ \_ multicolonna TBSTYLE ex**](toolbar-extended-styles.md) , questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

