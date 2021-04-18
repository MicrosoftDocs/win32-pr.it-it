---
title: Messaggio PSM_SETHEADERTITLE (Prsht. h)
description: Imposta il testo del titolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHeaderTitle di PropSheet.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Controlli di Windows Message PSM_SETHEADERTITLE
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301017"
---
# <a name="psm_setheadertitle-message"></a>\_Messaggio SETHEADERTITLE di PSM

Imposta il testo del titolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHeaderTitle di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della pagina della procedura guidata.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuovo sottotitolo dell'intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se si specifica la pagina corrente, verrà ridisegnata immediatamente per visualizzare il nuovo titolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETHEADERTITLEW** (Unicode) e **PSM \_ SETHEADERTITLEA** (ANSI)<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**HWNDTOINDEX di PSM \_**](psm-hwndtoindex.md)
</dt> <dt>

[**IDTOINDEX di PSM \_**](psm-idtoindex.md)
</dt> <dt>

[**PAGETOINDEX di PSM \_**](psm-pagetoindex.md)
</dt> </dl>

 

 





