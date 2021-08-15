---
title: LVM_MAPINDEXTOID messaggio (Commctrl.h)
description: Mappe'indice di un elemento a un ID univoco.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254bfff0ee1598b0657b44a967b9e1331b076a462c8703855c5dd23109a8835d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958150"
---
# <a name="lvm_mapindextoid-message"></a>Messaggio \_ MAPINDEXTOID LVM

Mappe'indice di un elemento a un ID univoco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice di un elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un ID univoco.

## <a name="remarks"></a>Commenti

I controlli visualizzazione elenco tiene traccia internamente degli elementi in base all'indice. Ciò può causare problemi perché gli indici possono cambiare durante la durata del controllo.

Il controllo visualizzazione elenco può contrassegnare un elemento con un ID quando viene creato. È possibile usare questo ID per garantire l'univocità durante la durata del controllo di visualizzazione elenco.

Per identificare in modo univoco un elemento, prendere l'indice restituito da una chiamata come [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chiamare **LVM \_ MAPINDEXTOID**. Il valore restituito è un ID univoco.

> [!Note]  
> In un ambiente multithreading, l'indice è garantito solo nel thread che ospita il controllo visualizzazione elenco, non nei thread in background.

 

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

