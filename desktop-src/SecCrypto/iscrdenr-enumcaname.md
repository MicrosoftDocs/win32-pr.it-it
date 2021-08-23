---
description: Enumera il nome delle autorità di certificazione (CA) per un nome di modello di certificato specificato.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: Metodo ISCrdEnr::enumCAName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 11742525d616aecc8d83871ae2a59025d1034513ae99d8a7253d16d9e0f64dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005219"
---
# <a name="iscrdenrenumcaname-method"></a>Metodo ISCrdEnr::enumCAName

Il **metodo enumCAName** enumera il nome delle autorità [*di*](../secgloss/c-gly.md) certificazione (CA) per un nome di modello di certificato specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Indice in base zero per la sequenza di enumerazione.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che determina se il nome fa riferimento al nome della CA o al nome del computer della CA. Se questo valore è SCARD ENROLL CA MACHINE NAME (definito come 0x01), il nome fa riferimento al nome \_ \_ del computer della \_ \_ CA. In caso contrario, il nome fa riferimento al nome della CA.

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

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
