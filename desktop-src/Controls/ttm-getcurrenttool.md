---
title: Messaggio TTM_GETCURRENTTOOL (COMmctrl. h)
description: Recupera le informazioni per lo strumento corrente in un controllo ToolTip.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- Controlli di Windows Message TTM_GETCURRENTTOOL
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964242"
---
# <a name="ttm_getcurrenttool-message"></a>\_Messaggio TTM GETCURRENTTOOL

Recupera le informazioni per lo strumento corrente in un controllo ToolTip.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che riceve informazioni sullo strumento corrente. Se questo valore è **null**, il valore restituito indica l'esistenza dello strumento corrente senza recuperare effettivamente le informazioni sullo strumento. Se questo valore non è **null**, prima di inviare questo messaggio è necessario compilare il membro **cbSize** della struttura **TOOLINFO** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario. Se *lParam* è **null**, restituisce un valore diverso da zero se esiste uno strumento corrente oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ GETCURRENTTOOLW** (Unicode) e **TTM \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





