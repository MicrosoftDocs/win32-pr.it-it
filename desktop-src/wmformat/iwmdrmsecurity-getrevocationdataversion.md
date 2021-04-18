---
title: Metodo IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: Il metodo GetRevocationDataVersion Recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Metodo GetRevocationDataVersion Windows Media Format
- Metodo GetRevocationDataVersion Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325536"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>Metodo IWMDRMSecurity:: GetRevocationDataVersion

Il metodo **GetRevocationDataVersion** Recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
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

*f \_ pdwCRLVersion* \[\]
</dt> <dd>

Variabile che riceve il numero di versione.

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

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





