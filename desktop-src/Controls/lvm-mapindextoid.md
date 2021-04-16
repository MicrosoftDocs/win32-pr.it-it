---
title: Messaggio LVM_MAPINDEXTOID (COMmctrl. h)
description: Esegue il mapping dell'indice di un elemento a un ID univoco.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- Controlli di Windows Message LVM_MAPINDEXTOID
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
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476090"
---
# <a name="lvm_mapindextoid-message"></a>\_Messaggio MAPINDEXTOID LVM

Esegue il mapping dell'indice di un elemento a un ID univoco.

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

I controlli di visualizzazione elenco internamente rilevano gli elementi in base all'indice. Questo può presentare problemi perché gli indici possono cambiare durante la durata del controllo.

Il controllo elenco-visualizzazione consente di contrassegnare un elemento con un ID quando viene creato l'elemento. È possibile usare questo ID per garantire l'univocità durante il ciclo di vita del controllo visualizzazione elenco.

Per identificare in modo univoco un elemento, prendere l'indice restituito da una chiamata, ad esempio [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chiamare **LVM \_ MAPINDEXTOID**. Il valore restituito è un ID univoco.

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



 

