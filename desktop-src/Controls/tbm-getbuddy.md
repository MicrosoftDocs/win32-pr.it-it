---
title: Messaggio TBM_GETBUDDY (COMmctrl. h)
description: Recupera l'handle a una finestra buddy del controllo TrackBar in una posizione specificata. La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- Controlli di Windows message TBM_GETBUDDY
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964997"
---
# <a name="tbm_getbuddy-message"></a>\_Messaggio TBM GETbuddy

Recupera l'handle a una finestra buddy del controllo TrackBar in una posizione specificata. La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che indica quale handle della finestra buddy verrà recuperato in base alla posizione relativa. I valori validi sono i seguenti:



| Valore                                                                                                                                    | Significato                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Recupera l'handle per l'oggetto Buddy a sinistra del controllo TrackBar. Se il controllo TrackBar utilizza lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , il messaggio recupererà l'oggetto Buddy sopra il TrackBar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Recupera l'handle per l'oggetto Buddy a destra del controllo TrackBar. Se il controllo TrackBar utilizza lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , il messaggio recupererà l'oggetto Buddy al di sotto di TrackBar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per la finestra di Buddy nella posizione specificata da *wParam* oppure **null** se non esiste alcuna finestra di Buddy in tale posizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





