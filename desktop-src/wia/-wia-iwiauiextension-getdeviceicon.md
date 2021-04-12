---
description: Ottiene un'icona di dispositivo personalizzata.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Metodo IWiaUIExtension:: GetDeviceIcon (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129407"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>Metodo IWiaUIExtension:: GetDeviceIcon

Ottiene un'icona di dispositivo personalizzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDeviceId* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica l'ID dispositivo del dispositivo WIA per il quale deve essere ottenuta l'icona.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Tipo: **HICON \** _

Punta a una posizione di memoria che riceverà un handle per l'icona del dispositivo.

</dd> <dt>

_nSize * \[ in\]
</dt> <dd>

Tipo: **ULONG**

Specifica la dimensione dell'icona desiderata, in pixel. Si presuppone che l'icona sia quadrata, mentre nSize specifica sia la larghezza che l'altezza dell'icona richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




