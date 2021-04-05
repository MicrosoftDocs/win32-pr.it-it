---
title: Messaggio LVM_GETINSERTMARK (COMmctrl. h)
description: Recupera la posizione del punto di inserimento.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- Controlli di Windows Message LVM_GETINSERTMARK
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873581"
---
# <a name="lvm_getinsertmark-message"></a>\_Messaggio GETINSERTMARK LVM

Recupera la posizione del punto di inserimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> che riceve la posizione del punto di inserimento.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario. Viene restituito **false** se la dimensione nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non è uguale alla dimensione effettiva della struttura.

## <a name="remarks"></a>Commenti

Un punto di inserimento può essere visualizzato solo se il controllo elenco-visualizzazione si trova nella visualizzazione icone, nella visualizzazione icone piccola o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





