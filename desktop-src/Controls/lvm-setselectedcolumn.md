---
title: LVM_SETSELECTEDCOLUMN messaggio (Commctrl.h)
description: Imposta l'indice della colonna selezionata.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- LVM_SETSELECTEDCOLUMN dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6564e1fda50d11b3d4c520f85184439b0465f1cf5767e7926e6e1c9476f786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019172"
---
# <a name="lvm_setselectedcolumn-message"></a>Messaggio LVM \_ SETSELECTEDCOLUMN

Imposta l'indice della colonna selezionata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Valore di tipo **int che** specifica l'indice di colonna.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="remarks"></a>Commenti

Gli indici di colonna vengono archiviati in una **matrice int.** Vedere il **membro puColumns** di [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





