---
description: Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: Metodo IWiaUIExtension::D eviceDialog (Wiadevd. h)
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
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526448"
---
# <a name="iwiauiextensiondevicedialog-method"></a>IWiaUIExtension::D Metodo eviceDialog

Fornisce un'interfaccia utente personalizzata che sostituisce l'interfaccia utente di sistema predefinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeviceDialogData* \[ in\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA \** _

Punta a una struttura [_ *DEVICEDIALOGDATA* *](-wia-devicedialogdata.md) che contiene tutti i dati necessari per implementare la finestra di dialogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se il metodo ha esito positivo, restituisce S \_ OK. Se l'utente annulla la finestra di dialogo, il metodo restituisce \_ false. Se il metodo non è implementato, restituisce E \_ NOTIMPL. Se il metodo ha esito negativo, viene restituito un codice di errore COM standard.

## <a name="remarks"></a>Commenti

Se si implementa l'interfaccia [**IWiaUIExtension**](-wia-iwiauiextension.md) e non si desidera sostituire l'interfaccia utente di sistema, questo metodo deve comunque essere implementato, ma non deve eseguire alcuna operazione oltre a restituire e \_ NOTIMPL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




