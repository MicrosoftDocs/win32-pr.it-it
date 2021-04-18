---
description: 'Recupera il nome del certificato risultante da una chiamata precedente riuscita a ISCrdEnr:: registra.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'Metodo ISCrdEnr:: getEnrolledCertificateName'
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
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316147"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>Metodo ISCrdEnr:: getEnrolledCertificateName

Il metodo **getEnrolledCertificateName** Recupera il nome del certificato risultante da una chiamata precedente riuscita a [**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).

Questo metodo può essere utilizzato anche per visualizzare il certificato in una finestra di dialogo. Questo metodo chiama la [](../secgloss/c-gly.md) funzione CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

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

*dwFlags* \[ in\]
</dt> <dd>

Valore che determina se il certificato viene visualizzato in una finestra di dialogo. Se questo valore viene spaventato \_ \_ \_ , nessun \_ certificato di visualizzazione (definito come 0x01), il certificato registrato non viene visualizzato. eventuali altri valori determinano la visualizzazione del certificato registrato nella finestra di dialogo **certificato** .

</dd> <dt>

*pBstrCertName* \[ out\]
</dt> <dd>

Puntatore a una stringa che restituisce il nome del certificato recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="c"></a>C++

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

### <a name="vb"></a>VB

Stringa che rappresenta il nome del certificato recuperato.

## <a name="remarks"></a>Commenti

Poiché questo metodo agisce su un certificato esistente, è necessario avere chiamato correttamente [**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) prima di poter chiamare **getEnrolledCertificateName**.

Il metodo **getEnrolledCertificateName** chiama la funzione [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) per recuperare il nome del certificato in base alla sequenza descritta per il nome del certificato \_ \_ \_ \_ del tipo di visualizzazione semplice del parametro *dwType* di **CertGetNameString**.

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

[**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
