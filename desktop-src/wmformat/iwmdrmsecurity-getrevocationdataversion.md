---
title: Metodo IWMDRMSecurity GetRevocationDataVersion (Wmdrmsdk.h)
description: Il metodo GetRevocationDataVersion recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Metodo GetRevocationDataVersion per Windows Media Format
- Metodo GetRevocationDataVersion in formato Windows Media, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity windows Media Format, metodo GetRevocationDataVersion
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
ms.openlocfilehash: d139b2daf3f3bc6ad78beaa50e19c0141aecd5e8bedac2dd20582fb1536d9b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930781"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>Metodo IWMDRMSecurity::GetRevocationDataVersion

Il **metodo GetRevocationDataVersion** recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*f \_ guidRevocationType* \[ in\]
</dt> <dd>

GUID che specifica il tipo di elenco di revoche. Impostare su una delle costanti nella tabella seguente.



| Costante GUID                 | Descrizione                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM \_ REVOCATIONTYPE \_ APP    | Specifica l'elenco di revoche di certificati dell'applicazione.                           |
| DISPOSITIVO WMDRM \_ REVOCATIONTYPE \_ | Specifica l'elenco di revoche di certificati del dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Specifica il nome Windows DRM multimediale per l'elenco di revoche di certificati dei dispositivi di rete. |



 

</dd> <dt>

*f \_ pdwCRLVersion* \[ out\]
</dt> <dd>

Variabile che riceve il numero di versione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





