---
description: Chiude la sessione del tasto supporto e deve essere chiamata prima del rilascio della sessione chiave.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'Metodo IMFMediaKeySession:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320504"
---
# <a name="imfmediakeysessionclose-method"></a>Metodo IMFMediaKeySession:: Close

Chiude la sessione del tasto supporto e deve essere chiamata prima del rilascio della sessione chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




