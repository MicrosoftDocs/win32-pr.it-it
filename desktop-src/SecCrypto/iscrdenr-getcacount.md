---
description: Restituisce il numero di autorità di certificazione (CAs) disponibili per emettere un certificato in base al modello di certificato specificato.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Metodo ISCrdEnr:: getCACount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317718"
---
# <a name="iscrdenrgetcacount-method"></a>Metodo ISCrdEnr:: getCACount

Il metodo **getCACount** restituisce il numero di [*autorità di certificazione*](../secgloss/c-gly.md) (CAS) disponibili per emettere un certificato in base al modello di certificato specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrCertTemplateName* \[ in\]
</dt> <dd>

Stringa che rappresenta il nome del modello di certificato.

</dd> <dt>

*pdwCACount* \[ out\]
</dt> <dd>

Puntatore a un oggetto **Long** che restituisce il numero di autorità di certificazione disponibili che emetteranno un certificato per il modello di certificato specificato in *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Valore **Long** che rappresenta il numero di autorità di certificazione disponibili che emetteranno un certificato per il modello di certificato specificato in *bstrCertTemplateName*.

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

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
