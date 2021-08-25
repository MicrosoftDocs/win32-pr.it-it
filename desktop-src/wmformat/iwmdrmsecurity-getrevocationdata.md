---
title: Metodo IWMDRMSecurity GetRevocationData (Wmdrmsdk.h)
description: Il metodo GetRevocationData recupera un elenco di revoche di certificati dall'archivio locale.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Metodo GetRevocationData windows Media Format
- Metodo GetRevocationData windows Media Format , interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity windows Media Format , metodo GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5035bc94051c61baaef7bcf474b4d6ebb4413b549dfff038bae7105f32d087b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808481"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>Metodo IWMDRMSecurity::GetRevocationData

Il **metodo GetRevocationData** recupera un elenco di revoche di certificati dall'archivio locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*f \_ guidRevocationType* \[ in\]
</dt> <dd>

GUID che identifica il tipo di elenco di revoche da recuperare. Usare una delle costanti nella tabella seguente.



| Costante GUID                 | Descrizione                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM \_ REVOCATIONTYPE \_ APP    | Specifica l'elenco di revoche di certificati dell'applicazione.                           |
| DISPOSITIVO WMDRM \_ \_ REVOCATIONTYPE | Specifica l'elenco di revoche di certificati del dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Specifica l'Windows di revoche di certificati di Media DRM per dispositivi di rete. |



 

</dd> <dt>

*f \_ pbCRL* \[ out\]
</dt> <dd>

Buffer che riceve l'elenco di revoche. Impostare su **NULL per** ottenere le dimensioni del buffer necessarie.

</dd> <dt>

*f \_ pcbCRL* \[ in, out\]
</dt> <dd>

Dimensione del buffer in byte. Se *f \_ pbCRL* è **NULL,** questo valore viene impostato sulle dimensioni del buffer richieste nell'output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

[**Revoca e rinnovo automatici dei componenti**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





