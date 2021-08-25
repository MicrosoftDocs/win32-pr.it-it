---
description: Specifica il nome dell'autorità di certificazione (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: Metodo ISCrdEnr::setCAName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 726b1d6d6a31831e5db192b5a71dea9efa32f624333ee7f6d6d2eea432dacae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960271"
---
# <a name="iscrdenrsetcaname-method"></a>Metodo ISCrdEnr::setCAName

Il **metodo setCAName** specifica il nome dell'autorità [*di certificazione*](../secgloss/c-gly.md) (CA).

## <a name="syntax"></a>Sintassi


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che specifica se il nome fa riferimento al nome della CA o al nome computer della CA. Se questo valore è SCARD ENROLL CA MACHINE NAME (definito come 0x01), il nome fa riferimento al nome \_ \_ computer della \_ \_ CA. In caso contrario, il nome fa riferimento al nome della CA.

</dd> <dt>

*bstrCertTemplateName* \[ Pollici\]
</dt> <dd>

Nome del modello di certificato.

</dd> <dt>

*bstrCAName* \[ Pollici\]
</dt> <dd>

Nome della CA da utilizzare con il modello di certificato specificato da *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata ha avuto esito positivo.

## <a name="remarks"></a>Commenti

Usare questo metodo per specificare una CA per un modello di certificato.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
