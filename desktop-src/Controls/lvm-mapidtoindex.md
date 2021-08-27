---
title: LVM_MAPIDTOINDEX messaggio (Commctrl.h)
description: Mappe'ID di un elemento in un indice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b5380d52f839f28324b808ed0d3304b6c5e2837869e0f0cfc6ab99d8f00b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079871"
---
# <a name="lvm_mapidtoindex-message"></a>Messaggio \_ LVM MAPIDTOINDEX

Mappe'ID di un elemento in un indice.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

ID univoco di un elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice più corrente.

## <a name="remarks"></a>Commenti

I controlli visualizzazione elenco tiene traccia internamente degli elementi in base all'indice. Ciò può presentare problemi perché gli indici possono cambiare durante la durata del controllo.

Il controllo visualizzazione elenco può contrassegnare un elemento con un ID quando viene creato. È possibile usare questo ID per garantire l'univocità durante la durata del controllo visualizzazione elenco.

Per identificare in modo univoco un elemento, prendere l'indice restituito da una chiamata, ad esempio [**IComponent::GetDisplayInfo,**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chiamare [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md). Il valore restituito è un ID univoco.

Se è necessario l'indice di un elemento dopo la creazione di un ID, è possibile chiamare **LVM \_ MAPIDTOINDEX** con l'ID univoco e restituisce l'indice più corrente.

**LVM \_ MAPIDTOINDEX** non è supportato con lo stile [**LVS \_ OWNERDATA.**](list-view-window-styles.md)

> [!Note]  
> In un ambiente multithreading l'indice è garantito solo nel thread che ospita il controllo visualizzazione elenco, non nei thread in background.

 

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

