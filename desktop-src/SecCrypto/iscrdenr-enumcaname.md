---
description: Enumera il nome delle autorità di certificazione (CAs) per un determinato nome del modello di certificato.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Metodo ISCrdEnr:: enumCAName'
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
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317720"
---
# <a name="iscrdenrenumcaname-method"></a>Metodo ISCrdEnr:: enumCAName

Il metodo **enumCAName** enumera il nome dell'autorità di [*certificazione*](../secgloss/c-gly.md) (CAS) per un determinato nome del modello di certificato.

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

*dwIndex* \[ in\]
</dt> <dd>

Indice in base zero per la sequenza di enumerazione.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se il nome fa riferimento al nome della CA o al nome del computer della CA. Se questo valore viene spaventato \_ , registrare il \_ nome del computer della CA \_ \_ (definito come 0x01), il nome si riferisce al nome del computer della CA. In caso contrario, il nome si riferisce al nome della CA.

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

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
