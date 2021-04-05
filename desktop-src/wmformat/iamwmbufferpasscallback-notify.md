---
title: Metodo di notifica IAMWMBufferPassCallback
description: Il metodo Notify viene chiamato dal pin per ogni buffer recapitato durante il flusso.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Notifica metodo Windows Media Format
- Metodo di notifica Windows Media Format, interfaccia IAMWMBufferPassCallback
- Interfaccia IAMWMBufferPassCallback-formato Windows Media, metodo Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118254"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>Metodo IAMWMBufferPassCallback:: Notify

Il metodo **Notify** viene chiamato dal pin per ogni buffer recapitato durante il flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNSSBuffer3* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) esposta nell'esempio multimediale.

</dd> <dt>

*pPin* \[ in\]
</dt> <dd>

Puntatore al pin associato al flusso multimediale a cui appartiene l'esempio.

</dd> <dt>

*prtStart* \[ in\]
</dt> <dd>

Ora di inizio dell'esempio.

</dd> <dt>

*prtEnd* \[ in\]
</dt> <dd>

Ora di fine dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non viene specificato alcun valore restituito specifico. Il pin chiamante ignora **HRESULT**.

## <a name="remarks"></a>Commenti

Questo metodo consente a un'applicazione di esaminare e agire sulle informazioni nel buffer multimediale prima che il contenuto del buffer venga elaborato. L'applicazione è responsabile della conoscenza del tipo di supporto sul pin. Queste informazioni possono essere ottenute ottenendo prima le informazioni sul flusso dal profilo e quindi chiamando il metodo [**IConfigAsfWriter2:: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) per determinare quale pin è associato a ogni flusso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su DirectShow QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Interfaccia IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Interfaccia INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 