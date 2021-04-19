---
description: Enumera i nomi dei modelli di certificato.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'Metodo ISCrdEnr:: enumCertTemplateName'
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
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317719"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>Metodo ISCrdEnr:: enumCertTemplateName

Il metodo **enumCertTemplateName** enumera i nomi dei modelli di certificato.

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

*dwIndex* \[ in\]
</dt> <dd>

Indice in base zero per la sequenza di enumerazione.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se il modello di certificato enumerato si applica ai certificati utente o computer. Se questo valore viene spaventato \_ \_ \_ \_ per la registrazione del modello di certificato utente (definito come 1), l'enumerazione si applica ai modelli di certificato utente. Se questo valore viene spaventato \_ , registrare \_ \_ \_ il modello del certificato del computer (definito come 2), l'enumerazione si applica ai modelli di certificato del computer.

</dd> <dt>

*pbstrCertTemplateName* \[ out\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del modello di certificato enumerato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che contiene il nome del modello di certificato enumerato.

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

[**ISCrdEnr::getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




