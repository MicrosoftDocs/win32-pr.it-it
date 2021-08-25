---
title: LVM_SETVIEW messaggio (Commctrl.h)
description: Imposta la visualizzazione di un controllo di visualizzazione elenco.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW dei messaggi Windows
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8d07b636a14624632d0e41ebcf6db66f420b9df4f8ca852e55ab2f3e1578e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656201"
---
# <a name="lvm_setview-message"></a>Messaggio \_ LVM SETVIEW

Imposta la visualizzazione di un controllo di visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>**Valore DWORD** che specifica la vista.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 in caso di esito positivo oppure -1 in caso contrario. Ad esempio, se la vista non è valida, viene restituito -1.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori per le visualizzazioni.

-   DETTAGLI \_ VISTA LV \_
-   ICONA VISTA \_ \_ LV
-   LV \_ VIEW \_ LIST
-   LV \_ VIEW \_ SMALLICON
-   RIQUADRO VISTA \_ \_ LV

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comctl32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





