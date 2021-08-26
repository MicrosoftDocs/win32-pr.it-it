---
description: Rimuove il buffer di origine specificato dalla raccolta di buffer di origine gestiti dall'oggetto IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: Metodo IMFMediaSourceExtension::RemoveSourceBuffer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 52c15882b57191169f033ab8a3b6c2f50f10f8e20b8f081c7bc70b7509b9a58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013971"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>Metodo IMFMediaSourceExtension::RemoveSourceBuffer

Rimuove il buffer di origine specificato dalla raccolta di buffer di origine gestiti [**dall'oggetto IMFMediaSourceExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceBuffer* \[ Pollici\]
</dt> <dd>

Buffer da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




