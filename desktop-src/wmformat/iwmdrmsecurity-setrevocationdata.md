---
title: Metodo IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: Il metodo SetRevocationData imposta un elenco di revoche di certificati nell'archivio locale.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Metodo SetRevocationData Windows Media Format
- Metodo SetRevocationData Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325534"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a>Metodo IWMDRMSecurity:: SetRevocationData

Il metodo **SetRevocationData** imposta un elenco di revoche di certificati nell'archivio locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*\_ guidRevocationType f* \[\]
</dt> <dd>

GUID che specifica il tipo di elenco di revoche. Impostare su una delle costanti nella tabella seguente.



| Costante GUID                 | Descrizione                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_app WMDRM REVOCATIONTYPE \_    | Specifica l'elenco di revoche di certificati dell'applicazione.                           |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Specifica l'elenco di revoche di certificati del dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ Cardea | Specifica Windows Media DRM per i dispositivi di rete elenco di revoche di certificati. |



 

</dd> <dt>

*\_ pbCRL f* \[\]
</dt> <dd>

Buffer contenente l'elenco di revoche di certificati.

</dd> <dt>

*\_ cbCRL f* \[\]
</dt> <dd>

Dimensioni del buffer, in byte.

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

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





