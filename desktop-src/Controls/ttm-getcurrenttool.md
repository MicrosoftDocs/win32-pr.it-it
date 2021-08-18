---
title: TTM_GETCURRENTTOOL messaggio (Commctrl.h)
description: Recupera le informazioni per lo strumento corrente in un controllo descrizione comando.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL controlli Windows messaggio
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
ms.openlocfilehash: 4558e582e4619cd7d96380a1e38e2efe68808b9241e4c627e12a74946965d8de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769341"
---
# <a name="ttm_getcurrenttool-message"></a>TTM \_ GETCURRENTTOOL message

Recupera le informazioni per lo strumento corrente in un controllo descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che riceve informazioni sullo strumento corrente. Se questo valore è **NULL,** il valore restituito indica l'esistenza dello strumento corrente senza recuperare effettivamente le informazioni sullo strumento. Se questo valore non è **NULL,** il **membro cbSize** della struttura **TOOLINFO** deve essere compilato prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario. Se *lParam* è **NULL,** restituisce un valore diverso da zero se esiste uno strumento corrente oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ GETCURRENTTOOLW** (Unicode) e **TTM \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





