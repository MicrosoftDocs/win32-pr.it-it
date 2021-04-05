---
title: Messaggio HDM_HITTEST (COMmctrl. h)
description: Verifica un punto per determinare quale elemento di intestazione, se presente, si trova in corrispondenza del punto specificato.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Controlli di Windows Message HDM_HITTEST
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
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120306"
---
# <a name="hdm_hittest-message"></a>\_Messaggio HDM HITTEST

Verifica un punto per determinare quale elemento di intestazione, se presente, si trova in corrispondenza del punto specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) contenente la posizione in cui eseguire il test e ricevere informazioni sui risultati del test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento in corrispondenza della posizione specificata, se presente, oppure 1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





