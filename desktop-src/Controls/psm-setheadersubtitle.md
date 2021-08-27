---
title: PSM_SETHEADERSUBTITLE messaggio (Prsht.h)
description: Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro PropSheet SetHeaderSubTitle.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- PSM_SETHEADERSUBTITLE controlli Windows messaggio
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e030b75a933ba7f647f8b3dffa5e45637999d45f3299f8280fd1db3afb9857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088501"
---
# <a name="psm_setheadersubtitle-message"></a>PSM \_ SETHEADERSUBTITLE message

Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet SetHeaderSubTitle.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della pagina della procedura guidata.

</dd> <dt>

*lParam* 
</dt> <dd>

Sottotitolo nuova intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se si specifica la pagina corrente, verrà ridisegnata immediatamente per visualizzare il nuovo sottotitolo.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ ACROBATWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl>      |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETHEADERSUBTITLEW** (Unicode) e **PSM \_ SETHEADERSUBTITLEA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**PSM \_ HWNDTOINDEX**](psm-hwndtoindex.md)
</dt> <dt>

[**PSM \_ IDTOINDEX**](psm-idtoindex.md)
</dt> <dt>

[**PSM \_ PAGETOINDEX**](psm-pagetoindex.md)
</dt> </dl>

 

 





