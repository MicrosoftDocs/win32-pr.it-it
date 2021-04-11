---
description: Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: Metodo IWiaUIExtension2::D eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226143"
---
# <a name="iwiauiextension2devicedialog-method"></a>IWiaUIExtension2::D Metodo eviceDialog

Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeviceDialogData* \[ in\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA2 \** _

Punta a una struttura [_ *DEVICEDIALOGDATA2* *](-wia-devicedialogdata2.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se il metodo ha esito positivo, restituisce S \_ OK. Se l'utente annulla la finestra di dialogo, il metodo restituisce \_ false. Se il metodo ha esito negativo, viene restituito un codice di errore appropriato. Nella tabella seguente vengono illustrati alcuni dei possibili codici di stato restituiti.



| Codice di errore    | Descrizione                              |
|---------------|------------------------------------------|
| E \_ INVALIDARG | Il parametro pDeviceDialogData è **null**. |
| E \_ NOTIMPL    | Il metodo non è implementato.           |



 

## <a name="remarks"></a>Commenti

Se si implementa l'interfaccia [**IWiaUIExtension2**](-wia-iwiauiextension2.md) e non si desidera sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve eseguire alcuna operazione oltre a restituire e \_ NOTIMPL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




