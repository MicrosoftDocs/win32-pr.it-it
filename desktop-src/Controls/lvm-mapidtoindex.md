---
title: Messaggio LVM_MAPIDTOINDEX (COMmctrl. h)
description: Esegue il mapping dell'ID di un elemento a un indice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- Controlli di Windows Message LVM_MAPIDTOINDEX
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
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302204"
---
# <a name="lvm_mapidtoindex-message"></a>\_Messaggio MAPIDTOINDEX LVM

Esegue il mapping dell'ID di un elemento a un indice.

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

Restituisce l'indice più recente.

## <a name="remarks"></a>Commenti

I controlli di visualizzazione elenco internamente rilevano gli elementi in base all'indice. Questo può presentare problemi perché gli indici possono cambiare durante la durata del controllo.

Il controllo elenco-visualizzazione consente di contrassegnare un elemento con un ID quando viene creato l'elemento. È possibile usare questo ID per garantire l'univocità durante il ciclo di vita del controllo visualizzazione elenco.

Per identificare in modo univoco un elemento, prendere l'indice restituito da una chiamata, ad esempio [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chiamare [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md). Il valore restituito è un ID univoco.

Se è necessario l'indice di un elemento dopo la creazione di un ID, è possibile chiamare **LVM \_ MAPIDTOINDEX** con l'ID univoco e viene restituito l'indice più recente.

**LVM \_ MAPIDTOINDEX** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .

> [!Note]  
> In un ambiente con multithreading, l'indice è garantito solo nel thread che ospita il controllo visualizzazione elenco, non nei thread in background.

 

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

