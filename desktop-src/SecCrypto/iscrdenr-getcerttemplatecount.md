---
description: Recupera il numero di modelli di certificato.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'Metodo ISCrdEnr:: getCertTemplateCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884853"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a>Metodo ISCrdEnr:: getCertTemplateCount

Il metodo **getCertTemplateCount** Recupera il numero di modelli di certificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se il modello è per i certificati utente o computer. Se questo valore viene spaventato \_ \_ \_ \_ per la registrazione del modello di certificato utente (definito come 1), il conteggio restituito sarà per i modelli di certificato utente. Se questo valore viene spaventato \_ , registrare \_ \_ \_ il modello di certificato del computer (definito come 2) il numero restituito sarà per i modelli di certificato del computer.

</dd> <dt>

*pdwCertTemplateCount* \[ out\]
</dt> <dd>

Puntatore a un oggetto **Long** che restituisce il numero di modelli di certificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Valore **Long** che rappresenta il numero di modelli di certificato.

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

[**ISCrdEnr::enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




