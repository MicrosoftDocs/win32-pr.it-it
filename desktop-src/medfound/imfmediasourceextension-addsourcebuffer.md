---
description: Aggiunge un oggetto IMFSourceBuffer alla raccolta di buffer associati a IMFMediaSourceExtension.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: Metodo IMFMediaSourceExtension::AddSourceBuffer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: b49a7c4fb0cb9e45ab0c2823d92ceb6e4076dfcaef4d2e8450f1f3d07f474279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942031"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a>Metodo IMFMediaSourceExtension::AddSourceBuffer

Aggiunge un [**oggetto IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) alla raccolta di buffer associati a [**IMFMediaSourceExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd></dd> <dt>

*pNotify* \[ Pollici\]
</dt> <dd></dd> <dt>

*ppSourceBuffer* \[ Cambio\]
</dt> <dd></dd> </dl>

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

 

 




