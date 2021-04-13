---
title: Messaggio UDM_GETPOS32 (COMmctrl. h)
description: Restituisce la posizione a 32 bit di un controllo di scorrimento.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- Controlli di Windows Message UDM_GETPOS32
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475725"
---
# <a name="udm_getpos32-message"></a>\_Messaggio UDM GETPOS32

Restituisce la posizione a 32 bit di un controllo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore **bool** impostato su zero se il valore viene recuperato correttamente o diverso da zero se si verifica un errore. Se questo parametro è impostato su **null**, gli errori non vengono segnalati.

Se si usa **UDM \_ GETPOS32** in una situazione tra processi, questo parametro deve essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione di un controllo di scorrimento con precisione a 32 bit. Le applicazioni devono controllare il valore *lParam* per determinare se il valore restituito è valido.

## <a name="remarks"></a>Commenti

Quando elabora questo messaggio, il controllo di scorrimento aggiorna la posizione corrente in base alla didascalia della finestra di Buddy. Restituisce un errore se non è presente alcuna finestra di Buddy o se la didascalia specifica un valore non valido o non compreso nell'intervallo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETPOS UDM**](udm-getpos.md)
</dt> <dt>

[**\_SETPOS UDM**](udm-setpos.md)
</dt> <dt>

[**\_SETPOS32 UDM**](udm-setpos32.md)
</dt> </dl>

 

 





