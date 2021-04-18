---
title: Messaggio LVM_SETINFOTIP (COMmctrl. h)
description: Imposta il testo della descrizione comando in risposta ritardata alla \_ notifica GETINFOTIP LVN.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- Controlli di Windows Message LVM_SETINFOTIP
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300976"
---
# <a name="lvm_setinfotip-message"></a>\_Messaggio SETINFOTIP LVM

Imposta il testo della descrizione comando in risposta ritardata alla notifica [ \_ GETINFOTIP LVN](lvn-getinfotip.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> che contiene le informazioni da impostare.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il testo della descrizione comando è impostato come riuscito; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

Il messaggio **LVM \_ SETINFOTIP** consente a un'applicazione di calcolare infotip in background attenendosi alla procedura seguente:

1.  In risposta alla notifica [ \_ GETINFOTIP di LVN](lvn-getinfotip.md) , impostare il membro **pszText** della struttura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) su una stringa vuota e restituire 0.
2.  In background, calcolare l'infotip.
3.  Dopo aver calcolato il infotip, inviare il messaggio **LVM \_ SETINFOTIP** , impostando il membro **pszText** della struttura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sui membri infotip e iItem e **iSubItem** sull'elemento **e sull'elemento** secondario a cui si applica infotip.

Il testo passato al messaggio **LVM \_ SETINFOTIP** viene visualizzato solo se l'elemento e l'elemento secondario descritti dalla struttura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sono ancora in uno stato che richiede un infotip

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





