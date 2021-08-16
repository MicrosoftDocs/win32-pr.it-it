---
title: Funzione WMCreateStreamForURL
description: La funzione WMCreateStreamForURL viene implementata dall'applicazione per creare un oggetto IStream COM per un URL specificato.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Funzione WMCreateStreamForURL windows Media Format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c32302147eeb814c211a77555ab1c9bb3614eddf3d8001015479461e05d40ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653454"
---
# <a name="wmcreatestreamforurl-function"></a>Funzione WMCreateStreamForURL

La **funzione WMCreateStreamForURL** viene implementata dall'applicazione per creare un oggetto **IStream** COM per un URL specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszURL* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa di caratteri wide contenente l'URL.

</dd> <dt>

*pfCorrectSource* \[ Cambio\]
</dt> <dd>

Puntatore a un flag, true impedisce all'SDK di provare altri plug-in di origine per questo URL.

</dd> <dt>

*ppStream* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore **all'oggetto IStream** creato dal metodo .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, deve restituire S \_ OK. Se non riesce, deve restituire un codice di errore **HRESULT** appropriato e \* *ppStream* deve essere impostato su **NULL.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Plug-in di origine**](source-plug-ins.md)
</dt> </dl>

 

 




