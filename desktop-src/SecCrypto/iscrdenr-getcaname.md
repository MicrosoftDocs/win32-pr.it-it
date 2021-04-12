---
description: Recupera il nome dell'autorità di certificazione (CA) specificata per un modello di certificato specificato.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Metodo ISCrdEnr:: getCAName'
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
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233501"
---
# <a name="iscrdenrgetcaname-method"></a>Metodo ISCrdEnr:: getCAName

Il metodo **getCAName** Recupera il nome dell'autorità di [*certificazione*](../secgloss/c-gly.md) (CA) specificata per un modello di certificato specificato.

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

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se il nome fa riferimento al nome della CA o al nome del computer della CA. Se questo valore viene spaventato \_ registrare il \_ nome del computer della CA \_ \_ (definito come 0x01), il nome si riferisce al nome del computer della CA. in caso contrario, il nome fa riferimento al nome della CA.

</dd> <dt>

*bstrCertTemplateName* \[ in\]
</dt> <dd>

Nome del modello di certificato.

</dd> <dt>

*pbstrCAName* \[ out\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome dell'autorità di certificazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che rappresenta il nome dell'autorità di certificazione.

## <a name="remarks"></a>Commenti

Il nome dell'autorità di certificazione predefinito è il primo nome nell'elenco di autorità di certificazione disponibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



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

 

 
