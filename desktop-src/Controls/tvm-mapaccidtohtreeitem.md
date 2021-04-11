---
title: Messaggio TVM_MAPACCIDTOHTREEITEM (COMmctrl. h)
description: Esegue il mapping di un ID di accessibilità a un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- Controlli di Windows Message TVM_MAPACCIDTOHTREEITEM
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
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048102"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>\_Messaggio MAPACCIDTOHTREEITEM TVM

Esegue il mapping di un ID di accessibilità a un **HTREEITEM**.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>**Uint** che contiene l'ID di accessibilità di cui eseguire il mapping a un **HTREEITEM**. </dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l' **HTREEITEM** a cui è stato eseguito il mapping dell'ID di accessibilità specificato.

## <a name="remarks"></a>Commenti

Quando si aggiunge un elemento a un controllo di visualizzazione albero, un **HTREEITEM** restituisce un valore che identifica in modo univoco l'elemento.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_MapAccIDToHTREEITEM TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





