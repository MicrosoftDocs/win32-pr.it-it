---
description: Recupera il nome del soggetto dal certificato di firma.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: Metodo ISCrdEnr::getSigningCertificateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 29933856eb644e638e9e58c8da0b0e3d6234e4f0175925c8a1fb5b48b126e3ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622401"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>Metodo ISCrdEnr::getSigningCertificateName

Il **metodo getSigningCertificateName** recupera il nome del soggetto dal certificato di firma.

Questo metodo può essere usato anche per visualizzare il certificato in una finestra di dialogo. Questo metodo chiama la [*funzione CryptoAPI*](../secgloss/c-gly.md) [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

## <a name="syntax"></a>Sintassi


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che determina se il certificato viene visualizzato in una finestra di dialogo. Se questo valore è SCARD \_ ENROLL \_ NO DISPLAY \_ \_ CERT (definito come 0x01),  il certificato di firma non viene visualizzato. Gli altri valori comportano la visualizzazione del certificato di firma nella finestra di dialogo Certificato.

</dd> <dt>

*pbstrSigningCertName* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del certificato di firma. Il certificato di firma verrà usato per firmare la [*richiesta di certificato.*](../secgloss/c-gly.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che rappresenta il nome del certificato di firma. Il certificato di firma verrà usato per firmare la [*richiesta di certificato.*](../secgloss/c-gly.md)

## <a name="remarks"></a>Commenti

Il **metodo getSigningCertificateName** restituisce il nome soggetto del certificato selezionato (o da un altro amministratore) in una precedente chiamata riuscita a [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) o [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md). Questo metodo chiama la funzione [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) per recuperare il nome del soggetto in base alla sequenza descritta per il valore CERT NAME SIMPLE DISPLAY TYPE del parametro \_ \_ \_ \_ *dwType di* **CertGetNameString.**

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

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
