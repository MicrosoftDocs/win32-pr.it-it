---
description: Recupera il nome dell'oggetto dal certificato di firma.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Metodo ISCrdEnr:: getSigningCertificateName'
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
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401745"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>Metodo ISCrdEnr:: getSigningCertificateName

Il metodo **getSigningCertificateName** Recupera il nome dell'oggetto dal certificato di firma.

Questo metodo può essere utilizzato anche per visualizzare il certificato in una finestra di dialogo. Questo metodo chiama la [](../secgloss/c-gly.md) funzione CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

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

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se il certificato viene visualizzato in una finestra di dialogo. Se questo valore viene spaventato \_ \_ , nessun certificato di \_ visualizzazione \_ (definito come 0x01), il certificato di firma non viene visualizzato; qualsiasi altro valore genera il certificato di firma visualizzato nella finestra di dialogo **certificato** .

</dd> <dt>

*pbstrSigningCertName* \[ out\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del certificato di firma. Il certificato di firma verrà usato per firmare la [*richiesta di certificato*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che rappresenta il nome del certificato di firma. Il certificato di firma verrà usato per firmare la [*richiesta di certificato*](../secgloss/c-gly.md).

## <a name="remarks"></a>Commenti

Il metodo **getSigningCertificateName** restituisce il nome del soggetto del certificato selezionato dall'utente (o da un altro amministratore) in una chiamata precedente riuscita a [**ISCrdEnr:: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) o [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md). Questo metodo chiama la funzione [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) per recuperare il nome del soggetto in base alla sequenza descritta per il \_ nome del certificato \_ \_ \_ del tipo di visualizzazione semplice valore del parametro *dwType* di **CertGetNameString**.

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

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
