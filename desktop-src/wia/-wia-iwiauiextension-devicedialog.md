---
description: "Metodo IWiaUIExtension::D eviceDialog: fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita."
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: Metodo IWiaUIExtension::D eviceDialog (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116709"
---
# <a name="iwiauiextensiondevicedialog-method"></a>Metodo IWiaUIExtension::D eviceDialog

Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeviceDialogData* \[ Pollici\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA \***

Punta a una [**struttura DEVICEDIALOGDATA**](-wia-devicedialogdata.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se il metodo ha esito positivo, restituisce S \_ OK. Se l'utente annulla la finestra di dialogo, il metodo restituisce S \_ FALSE. Se il metodo non è implementato, restituisce E \_ NOTIMPL. Se il metodo ha esito negativo, restituisce un codice di errore COM standard.

## <a name="remarks"></a>Commenti

Se si implementa [**l'interfaccia IWiaUIExtension**](-wia-iwiauiextension.md) e non si vuole sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve fare altro che restituire E \_ NOTIMPL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




