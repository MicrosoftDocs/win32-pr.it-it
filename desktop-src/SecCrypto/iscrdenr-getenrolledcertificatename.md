---
description: Recupera il nome del certificato risultante da una precedente chiamata riuscita a ISCrdEnr::enroll.
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: Metodo ISCrdEnr::getEnrolledCertificateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 79158a5c10cee2f4f38163c5a657199415568b36076b9e84f2a54020d1be42a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409491"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>Metodo ISCrdEnr::getEnrolledCertificateName

Il **metodo getEnrolledCertificateName** recupera il nome del certificato risultante da una precedente chiamata riuscita a [**ISCrdEnr::enroll.**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))

Questo metodo può essere utilizzato anche per visualizzare il certificato in una finestra di dialogo. Questo metodo chiama la [*funzione CryptoAPI*](../secgloss/c-gly.md) [**CertGetNameString.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)

## <a name="syntax"></a>Sintassi


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Valore che determina se il certificato viene visualizzato in una finestra di dialogo. Se questo valore è SCARD \_ ENROLL \_ NO DISPLAY \_ \_ CERT (definito  come 0x01), il certificato registrato non viene visualizzato. Qualsiasi altro valore determina la visualizzazione del certificato registrato nella finestra di dialogo Certificato.

</dd> <dt>

*pBstrCertName* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del certificato recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

### <a name="vb"></a>VB

Stringa che rappresenta il nome del certificato recuperato.

## <a name="remarks"></a>Commenti

Poiché questo metodo opera su un certificato esistente, è necessario aver chiamato [**correttamente ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) prima di poter chiamare **getEnrolledCertificateName**.

Il **metodo getEnrolledCertificateName** chiama la funzione [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) per recuperare il nome del certificato in base alla sequenza descritta per il valore CERT NAME SIMPLE DISPLAY TYPE del parametro \_ \_ \_ \_ *dwType* di **CertGetNameString.**

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

[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
