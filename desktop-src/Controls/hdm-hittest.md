---
title: HDM_HITTEST messaggio (Commctrl.h)
description: Verifica un punto per determinare quale elemento di intestazione, se presente, si trova nel punto specificato.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST di Windows di messaggio
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc219640d9dd9d5d9a4c9537169401f681e37660554266b3edd653365cf8cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544771"
---
# <a name="hdm_hittest-message"></a>Messaggio \_ HITTEST HDM

Verifica un punto per determinare quale elemento di intestazione, se presente, si trova nel punto specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) che contiene la posizione da testare e riceve informazioni sui risultati del test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento nella posizione specificata, se presente, oppure 1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





