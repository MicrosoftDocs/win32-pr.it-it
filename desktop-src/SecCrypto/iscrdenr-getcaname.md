---
description: Recupera il nome dell'autorità di certificazione (CA) specificata per un modello di certificato specificato.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: Metodo ISCrdEnr::getCAName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 6de5d1108ab09c9658af307d6a67c5a94a5dc35514720a221540de263f516c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960281"
---
# <a name="iscrdenrgetcaname-method"></a>Metodo ISCrdEnr::getCAName

Il **metodo getCAName** recupera il nome dell'autorità [*di certificazione*](../secgloss/c-gly.md) (CA) specificata per un modello di certificato specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che determina se il nome fa riferimento al nome della CA o al nome del computer della CA. Se questo valore è SCARD ENROLL CA MACHINE NAME (definito come 0x01), il nome fa riferimento al nome del computer della CA; in caso contrario, il nome fa riferimento al nome \_ \_ della \_ \_ CA.

</dd> <dt>

*bstrCertTemplateName* \[ Pollici\]
</dt> <dd>

Nome del modello di certificato.

</dd> <dt>

*pbstrCAName* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome della CA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

### <a name="vb"></a>VB

Stringa che rappresenta il nome della CA.

## <a name="remarks"></a>Commenti

Il nome predefinito della CA è il nome nell'elenco di CA disponibili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
