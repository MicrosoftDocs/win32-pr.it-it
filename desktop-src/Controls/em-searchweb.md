---
title: Messaggio EM_SEARCHWEB (COMmctrl. h)
description: Apre il browser ed esegue una ricerca Web con il testo selezionato come termine di ricerca.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Controlli di Windows Message EM_SEARCHWEB
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874270"
---
# <a name="em_searchweb-message"></a>\_Messaggio SEARCHWEB em

Apre il browser ed esegue una ricerca Web con il testo selezionato come termine di ricerca.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Se la funzionalità "Cerca sul Web" è disabilitata usando il messaggio [**\_ ENABLESEARCHWEB em**](em-enablesearchweb.md) , questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10, 1809 \[\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2019\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ENABLESEARCHWEB em**](em-enablesearchweb.md)
</dt> </dl>

 

 





