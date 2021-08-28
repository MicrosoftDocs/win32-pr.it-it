---
title: CCM_SETVERSION messaggio (Commctrl.h)
description: Questo messaggio viene usato per informare il controllo che si prevede un comportamento associato a una determinata versione.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9453b99ff9cd23675b3b5d79593071e4ebb3fbb65d06a78d0fe8094154b2486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320101"
---
# <a name="ccm_setversion-message"></a>Messaggio \_ CCM SETVERSION

Questo messaggio viene usato per informare il controllo che si prevede un comportamento associato a una determinata versione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di versione.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la versione specificata nel messaggio **\_ SETVERSION CCM** precedente. Se *wParam è* impostato su un valore maggiore della versione corrente della DLL, restituisce -1.

## <a name="remarks"></a>Commenti

In alcuni casi, un controllo può comportarsi in modo diverso, a seconda della versione. Questo vale principalmente per i bug risolti nelle versioni successive. Il **messaggio \_ CCM SETVERSION** consente di informare il controllo del comportamento previsto. È possibile determinare la versione specificata inviando un [**messaggio \_ GETVERSION di CCM.**](ccm-getversion.md) Per un esempio di come usare questo messaggio, vedere Disegno personalizzato con List-View [e Tree-View controlli](custom-draw.md).

Se è installata ComCtl32.dll versione 6, indipendentemente dal valore impostato in *wParam*, il messaggio **\_ CCM SETVERSION** restituisce la versione 6.

> [!Note]  
> Questo messaggio imposta solo il numero di versione per il controllo a cui viene inviato.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





