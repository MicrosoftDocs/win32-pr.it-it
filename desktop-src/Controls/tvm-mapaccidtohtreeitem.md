---
title: TVM_MAPACCIDTOHTREEITEM messaggio (Commctrl.h)
description: Mappe un ID di accessibilità a un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM dei messaggi Windows
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6481d8db806156d10536ac0ec7c66fdeb4693a1133365767b4c3dc37ad8420f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045801"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>Messaggio TVM \_ MAPACCIDTOHTREEITEM

Mappe un ID di accessibilità a **un HTREEITEM.**

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>**UINT che** contiene l'ID di accessibilità di cui eseguire il mapping a **un HTREEITEM.** </dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **l'elemento HTREEITEM** a cui è mappato l'ID di accessibilità specificato.

## <a name="remarks"></a>Commenti

Quando si aggiunge un elemento a un controllo di visualizzazione albero, viene restituito **un elemento HTREEITEM,** che identifica in modo univoco l'elemento.

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TreeView \_ MapAccIDToHTREEITEM**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





