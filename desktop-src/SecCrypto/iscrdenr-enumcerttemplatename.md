---
description: Enumera i nomi dei modelli di certificato.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: Metodo ISCrdEnr::enumCertTemplateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: aab979e77e9e3e61b9d35125accbdf01934764d5a09daf161480646cdec28e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005199"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>Metodo ISCrdEnr::enumCertTemplateName

Il **metodo enumCertTemplateName** enumera i nomi dei modelli di certificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
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

Valore che determina se il modello di certificato enumerato si applica ai certificati utente o computer. Se questo valore è SCARD \_ ENROLL \_ USER \_ CERT TEMPLATE (definito come 1), l'enumerazione \_ si applica ai modelli di certificato utente. Se questo valore è SCARD \_ ENROLL \_ MACHINE \_ CERT TEMPLATE (definito come 2), l'enumerazione \_ si applica ai modelli di certificato del computer.

</dd> <dt>

*pbstrCertTemplateName* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del modello di certificato enumerato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa contenente il nome del modello di certificato enumerato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr è definito come \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




