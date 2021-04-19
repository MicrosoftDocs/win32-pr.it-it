---
title: Metodo IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: Il metodo GetMachineCertificate Recupera il certificato del computer del sottosistema DRM nel computer client.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Metodo GetMachineCertificate Windows Media Format
- Metodo GetMachineCertificate Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327457"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>Metodo IWMDRMSecurity:: GetMachineCertificate

Il metodo **GetMachineCertificate** Recupera il certificato del computer del sottosistema DRM nel computer client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwCertificateType* \[ in\]
</dt> <dd>

Tipo di certificato da recuperare. Impostare su uno dei valori riportati nella tabella seguente.



| Valore                        | Descrizione                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| \_Tipo di certificato WMDRM \_ \_ V1 | Il certificato verrà recuperato nel formato utilizzato dai componenti legacy.            |
| \_Tipo di certificato WMDRM \_ \_ v2 | Il certificato verrà recuperato nel formato utilizzato dai componenti di Windows Vista. |



 

</dd> <dt>

*rgbVersion \[ 4 \]* in \[ uscita\]
</dt> <dd>

Matrice di quattro byte che specifica la versione del sottosistema DRM nel computer client.

</dd> <dt>

*ppbCertificate* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore ai dati del certificato. Impostare su **null** per fare in modo che il metodo fornisca la dimensione del buffer necessaria per contenere il certificato in *pcbCertificate*.

</dd> <dt>

*pcbCertificate* \[ in uscita\]
</dt> <dd>

Dimensioni in byte del certificato. Se *ppbCertificate* è **null**, questo valore verrà impostato sulle dimensioni del certificato. Se *ppbCertificate* non è **null**, questo valore deve essere impostato sulla dimensione del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





