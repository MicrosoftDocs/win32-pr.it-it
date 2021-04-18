---
description: Specifica il nome del modello di certificato.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Metodo ISCrdEnr:: setCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312802"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>Metodo ISCrdEnr:: setCertTemplateName

Il metodo **setCertTemplateName** specifica il nome del modello di certificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se è in corso l'impostazione del nome reale o del nome visualizzato del modello di certificato. Se *dwFlags* presenta il valore SCard \_ Registra \_ il \_ \_ nome visualizzato \_ del modello di certificato, viene impostato il nome visualizzato del modello di certificato. In caso contrario, viene impostato il nome reale del modello di certificato.

</dd> <dt>

*bstrCertTemplateName* \[ in\]
</dt> <dd>

Nome del modello di certificato che verrà usato nella richiesta di certificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Se non si imposta il nome del modello di certificato chiamando **ISCrdEnr:: setCertTemplateName**, il nome predefinito è il primo nome nell'elenco dei modelli di certificato disponibili.

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

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




