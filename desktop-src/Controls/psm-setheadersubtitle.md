---
title: Messaggio PSM_SETHEADERSUBTITLE (Prsht. h)
description: Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHeaderSubTitle di PropSheet.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- Controlli di Windows Message PSM_SETHEADERSUBTITLE
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
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964159"
---
# <a name="psm_setheadersubtitle-message"></a>\_Messaggio SETHEADERSUBTITLE di PSM

Imposta il testo del sottotitolo per l'intestazione della pagina interna di una procedura guidata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHeaderSubTitle di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .

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

Se si specifica la pagina corrente, verrà ridisegnata immediatamente per visualizzare il nuovo sottotitolo.

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl>      |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETHEADERSUBTITLEW** (Unicode) e **PSM \_ SETHEADERSUBTITLEA** (ANSI)<br/> |



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

 

 





