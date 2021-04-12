---
title: WMCreateStreamForURL (funzione)
description: La funzione WMCreateStreamForURL viene implementata dall'applicazione per creare un oggetto IStream COM per un determinato URL.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Formato Windows Media della funzione WMCreateStreamForURL
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397783"
---
# <a name="wmcreatestreamforurl-function"></a>WMCreateStreamForURL (funzione)

La funzione **WMCreateStreamForURL** viene implementata dall'applicazione per creare un oggetto **IStream** com per un determinato URL.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszURL* \[ in\]
</dt> <dd>

Puntatore a una stringa di caratteri wide contenente l'URL.

</dd> <dt>

*pfCorrectSource* \[ out\]
</dt> <dd>

Puntatore a un flag, true impedirà all'SDK di provare altri plug-in di origine per questo URL.

</dd> <dt>

*ppStream* \[ out\]
</dt> <dd>

Puntatore a un puntatore all'oggetto **IStream** creato dal metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, deve restituire S \_ OK. Se ha esito negativo, deve restituire un codice di errore **HRESULT** appropriato e \* *ppStream* deve essere impostato su **null**.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Plug-in di origine**](source-plug-ins.md)
</dt> </dl>

 

 




