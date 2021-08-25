---
description: Specifica il nome del modello di certificato.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: Metodo ISCrdEnr::setCertTemplateName
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
ms.openlocfilehash: 5f757ead06e5d1769e109bcbfc8e3510f4298f32145d60c4c0bc992a01f3ab36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993041"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>Metodo ISCrdEnr::setCertTemplateName

Il **metodo setCertTemplateName** specifica il nome del modello di certificato.

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

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che determina se è in corso l'impostazione del nome reale o del nome visualizzato del modello di certificato. Se *dwFlags ha* il valore SCARD \_ ENROLL CERT TEMPLATE DISPLAY NAME, viene impostato il nome visualizzato \_ del modello di \_ \_ \_ certificato. In caso contrario, viene impostato il nome reale del modello di certificato.

</dd> <dt>

*bstrCertTemplateName* \[ Pollici\]
</dt> <dd>

Nome del modello di certificato che verrà usato nella richiesta di certificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Se non si imposta il nome del modello di certificato chiamando **ISCrdEnr::setCertTemplateName**, il nome predefinito sarà il nome nell'elenco dei modelli di certificato disponibili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr è definito come \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




