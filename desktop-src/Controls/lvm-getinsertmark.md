---
title: LVM_GETINSERTMARK messaggio (Commctrl.h)
description: Recupera la posizione del punto di inserimento.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e64281ccc9d4638353ddbb6062ce5cf1c0a678e009639dcc43cd0d4cf52741
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002671"
---
# <a name="lvm_getinsertmark-message"></a>Messaggio LVM \_ GETINSERTMARK

Recupera la posizione del punto di inserimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">una struttura LVINSERTMARK</a> che riceve la posizione del punto di inserimento.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario. **False** viene restituito se le dimensioni nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non sono uguali alle dimensioni effettive della struttura.

## <a name="remarks"></a>Commenti

Un punto di inserimento può essere visualizzato solo se il controllo visualizzazione elenco si trova nella visualizzazione icone, nella visualizzazione icone piccola o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





