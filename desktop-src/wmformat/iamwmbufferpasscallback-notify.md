---
title: Metodo IAMWMBufferPassCallback Notify
description: Il metodo Notify viene chiamato dal pin per ogni buffer recapitato durante il flusso.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Metodo Notify per Windows Media Format
- Notifica al metodo windows Media Format , interfaccia IAMWMBufferPassCallback
- Metodo Notify dell'interfaccia IAMWMBufferPassCallback per Windows Media Format
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f364243e40400884287c6219698991ccf8afc0be86a85ec612a5b193253994dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847536"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>Metodo IAMWMBufferPassCallback::Notify

Il **metodo Notify** viene chiamato dal pin per ogni buffer recapitato durante il flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNSSBuffer3* \[ Pollici\]
</dt> <dd>

Puntatore [**all'interfaccia INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) esposta nell'esempio multimediale.

</dd> <dt>

*pPin* \[ Pollici\]
</dt> <dd>

Puntatore al pin associato al flusso multimediale a cui appartiene l'esempio.

</dd> <dt>

*prtStart* \[ Pollici\]
</dt> <dd>

Ora di inizio dell'esempio.

</dd> <dt>

*prtEnd* \[ Pollici\]
</dt> <dd>

Ora di fine dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non viene specificato alcun valore restituito specifico. Il pin chiamante ignora **il valore HRESULT**.

## <a name="remarks"></a>Commenti

Questo metodo consente a un'applicazione di esaminare e agire sulle informazioni nel buffer multimediale prima dell'elaborazione del contenuto del buffer. L'applicazione è responsabile della conoscenza del tipo di supporto sul pin. Queste informazioni possono essere ottenute ottenendo prima le informazioni sul flusso dal profilo e quindi chiamando il metodo [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) per determinare quale pin è associato a ogni flusso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DirectShow Informazioni di riferimento su QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Interfaccia IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Interfaccia INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 