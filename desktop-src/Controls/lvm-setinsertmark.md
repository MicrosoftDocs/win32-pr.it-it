---
title: Messaggio LVM_SETINSERTMARK (COMmctrl. h)
description: Imposta il punto di inserimento sulla posizione definita.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- Controlli di Windows Message LVM_SETINSERTMARK
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118990"
---
# <a name="lvm_setinsertmark-message"></a>\_Messaggio SETINSERTMARK LVM

Imposta il punto di inserimento sulla posizione definita.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> che specifica la posizione in cui impostare il punto di inserimento.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario. Viene restituito **false** se la dimensione nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non è uguale alla dimensione effettiva della struttura o quando un punto di inserimento non è applicabile nella visualizzazione corrente.

## <a name="remarks"></a>Commenti

Un punto di inserimento può essere visualizzato solo se il controllo elenco-visualizzazione si trova nella visualizzazione icone, nella visualizzazione icone piccole o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





