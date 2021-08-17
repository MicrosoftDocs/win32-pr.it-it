---
title: Metodo IWMDRMSecurity GetMachineCertificate (Wmdrmsdk.h)
description: Il metodo GetMachineCertificate recupera il certificato del computer del sottosistema DRM nel computer client.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Metodo GetMachineCertificate per Windows Media Format
- Metodo GetMachineCertificate in formato Windows Media, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity windows Media Format , metodo GetMachineCertificate
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
ms.openlocfilehash: 4fd85a3b74ee28e5faa8df5fc264d50366803f4073ec97a36920577d417e4f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084698"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>Metodo IWMDRMSecurity::GetMachineCertificate

Il **metodo GetMachineCertificate** recupera il certificato del computer del sottosistema DRM nel computer client.

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

*dwCertificateType* \[ Pollici\]
</dt> <dd>

Tipo di certificato da recuperare. Impostare su uno dei valori nella tabella seguente.



| Valore                        | Descrizione                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| TIPO DI CERTIFICATO WMDRM \_ \_ \_ V1 | Il certificato verrà recuperato nel formato usato dai componenti legacy.            |
| TIPO DI CERTIFICATO WMDRM \_ \_ \_ V2 | Il certificato verrà recuperato nel formato usato dai componenti Windows Vista. |



 

</dd> <dt>

*rgbVersion \[ 4 \]* \[ out\]
</dt> <dd>

Matrice di quattro byte che specifica la versione del sottosistema DRM nel computer client.

</dd> <dt>

*ppbCertificate* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore ai dati del certificato. Impostare su **NULL per** fare in modo che il metodo fornisse le dimensioni del buffer necessarie per contenere il certificato in *pcbCertificate*.

</dd> <dt>

*pcbCertificate* \[ in, out\]
</dt> <dd>

Dimensioni del certificato in byte. Se *ppbCertificate* è **NULL,** questo valore verrà impostato sulla dimensione del certificato. Se *ppbCertificate* non è **NULL,** questo valore deve essere impostato sulla dimensione del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





