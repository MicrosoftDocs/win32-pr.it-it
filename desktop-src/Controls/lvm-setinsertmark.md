---
title: LVM_SETINSERTMARK messaggio (Commctrl.h)
description: Imposta il punto di inserimento sulla posizione definita.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- LVM_SETINSERTMARK controlli di Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae1cad35bd20605c4cb229dac69eb7461add8b7240b495cc48fb809d39aa098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919861"
---
# <a name="lvm_setinsertmark-message"></a>Messaggio LVM \_ SETINSERTMARK

Imposta il punto di inserimento sulla posizione definita.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">struttura LVINSERTMARK</a> che specifica dove impostare il punto di inserimento.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario. **False** viene restituito se le dimensioni nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non sono uguali alle dimensioni effettive della struttura o quando un punto di inserimento non è applicabile nella visualizzazione corrente.

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



 

 





