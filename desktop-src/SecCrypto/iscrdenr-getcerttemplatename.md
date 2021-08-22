---
description: Recupera il nome del modello di certificato.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: Metodo ISCrdEnr::getCertTemplateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: aaf37f3907bc2b26ca1adbbded7be5ed7897a74ea9664d4353354d5ad9657d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409621"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>Metodo ISCrdEnr::getCertTemplateName

Il **metodo getCertTemplateName** recupera il nome del modello di certificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che determina se viene restituito il nome reale o il nome visualizzato del modello di certificato. Se *dwFlags* ha il valore SCARD \_ ENROLL CERT TEMPLATE DISPLAY NAME, viene recuperato il nome visualizzato del modello di certificato. In caso contrario, viene visualizzato il nome reale del \_ modello di \_ \_ \_ certificato.

</dd> <dt>

*pbstrCertTemplateName* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del modello di certificato che verrà usato nella richiesta [*di certificato.*](../secgloss/c-gly.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

### <a name="vb"></a>VB

Stringa che rappresenta il nome del modello di certificato che verrà utilizzato nella richiesta [*di certificato.*](../secgloss/c-gly.md)

## <a name="remarks"></a>Commenti

Se non si imposta il nome del modello di certificato chiamando [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), il nome predefinito sarà il nome nell'elenco dei modelli di certificato disponibili.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
