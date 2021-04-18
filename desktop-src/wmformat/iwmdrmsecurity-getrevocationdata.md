---
title: Metodo IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: Il metodo GetRevocationData recupera un elenco di revoche di certificati dall'archivio locale.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Metodo GetRevocationData Windows Media Format
- Metodo GetRevocationData Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetRevocationData
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
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325538"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>Metodo IWMDRMSecurity:: GetRevocationData

Il metodo **GetRevocationData** recupera un elenco di revoche di certificati dall'archivio locale.

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

*\_ guidRevocationType f* \[\]
</dt> <dd>

GUID che identifica il tipo di elenco di revoche da recuperare. Utilizzare una delle costanti nella tabella seguente.



| Costante GUID                 | Descrizione                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_app WMDRM REVOCATIONTYPE \_    | Specifica l'elenco di revoche di certificati dell'applicazione.                           |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Specifica l'elenco di revoche di certificati del dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ Cardea | Specifica Windows Media DRM per i dispositivi di rete elenco di revoche di certificati. |



 

</dd> <dt>

*f \_ pbCRL* \[\]
</dt> <dd>

Buffer che riceve l'elenco di revoche. Impostare su **null** per ottenere la dimensione del buffer richiesta.

</dd> <dt>

*f \_ pcbCRL* \[ in uscita\]
</dt> <dd>

Dimensione del buffer in byte. Se *f \_ PbCRL* è **null**, questo valore viene impostato sulla dimensione del buffer richiesta nell'output.

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

[**Revoca e rinnovo automatici dei componenti**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





