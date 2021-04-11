---
title: Messaggio TVM_MAPHTREEITEMTOACCID (COMmctrl. h)
description: Esegue il mapping di un HTREEITEM a un ID di accessibilità.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Controlli di Windows Message TVM_MAPHTREEITEMTOACCID
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119798"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>\_Messaggio MAPHTREEITEMTOACCID TVM

Esegue il mapping di un **HTREEITEM** a un ID di accessibilità.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>**HTREEITEM** di cui è stato eseguito il mapping a un ID di accessibilità.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un ID di accessibilità.

## <a name="remarks"></a>Commenti

Quando si aggiunge un elemento a un controllo di visualizzazione albero, viene restituito un handle **HTREEITEM** che identifica in modo univoco l'elemento.

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

[**\_MapHTREEITEMtoAccID TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





