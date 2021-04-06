---
title: Messaggio LM_HITTEST (COMmctrl. h)
description: Determina se l'utente ha fatto clic sul collegamento specificato.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Controlli di Windows Message LM_HITTEST
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873329"
---
# <a name="lm_hittest-message"></a>\_Messaggio HITTEST di LM

Determina se l'utente ha fatto clic sul collegamento specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere **null**.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> da compilare con informazioni sul collegamento su cui l'utente ha fatto clic, se presente. </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'utente ha fatto clic su un collegamento; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Se il messaggio di **\_ HITTEST** viene completato correttamente, il sistema compila [**iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) e **litey. szId**. Se il messaggio di **\_ HITTEST** viene interrotto, non presupporre che le informazioni in **Lite** è valide.

> [!Note]  
> Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





