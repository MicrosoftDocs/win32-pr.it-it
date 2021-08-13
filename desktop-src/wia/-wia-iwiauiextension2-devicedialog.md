---
description: "Metodo IWiaUIExtension2::D eviceDialog: fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita."
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: Metodo IWiaUIExtension2::D eviceDialog (Wiadevd.h)
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
ms.openlocfilehash: 582a2fe90e6a455b2c0d0119b749a9d86b912b58150d30f3804466ef5bea2a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439885"
---
# <a name="iwiauiextension2devicedialog-method"></a>Metodo IWiaUIExtension2::D eviceDialog

Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeviceDialogData* \[ Pollici\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA2 \***

Punta a una [**struttura DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se il metodo ha esito positivo, restituisce S \_ OK. Se l'utente annulla il dialogo, il metodo restituisce S \_ FALSE. Se il metodo ha esito negativo, restituisce un codice di errore appropriato. La tabella seguente illustra alcuni dei possibili codici di stato restituiti.



| Codice di errore    | Descrizione                              |
|---------------|------------------------------------------|
| E \_ INVALIDARG | Il parametro pDeviceDialogData è **NULL.** |
| E \_ NOTIMPL    | Il metodo non è implementato.           |



 

## <a name="remarks"></a>Commenti

Se si implementa [**l'interfaccia IWiaUIExtension2**](-wia-iwiauiextension2.md) e non si vuole sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve fare altro che restituire E \_ NOTIMPL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




