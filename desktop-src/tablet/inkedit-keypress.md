---
description: Si verifica quando l'utente preme e rilascia un tasto mentre il controllo InkEdit dispone dello stato attivo.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit. KeyPress (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313945"
---
# <a name="inkeditkeypress-event"></a>Evento InkEdit. KeyPress

Si verifica quando l'utente preme e rilascia un tasto mentre il controllo [InkEdit](inkedit-control-reference.md) dispone dello stato attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Char* 
</dt> <dd>

Intero che restituisce un codice ANSI numerico standard. Il parametro *char* viene passato per riferimento. Se lo si modifica, viene inviato un carattere diverso al controllo. Se si modifica il parametro *char* in 0, l'evento viene annullato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'evento ha esito positivo, viene restituito **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** . L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeKeyPress.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Inchiostrato. h (richiede anche il \_ . c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**\[Controllo InkEdit evento KeyDown\]**](inkedit-keydown.md)
</dt> <dt>

[**\[Controllo InkEdit evento KeyUp\]**](inkedit-keyup.md)
</dt> </dl>

 

