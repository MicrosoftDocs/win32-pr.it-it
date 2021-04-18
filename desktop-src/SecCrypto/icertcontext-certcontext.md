---
description: Imposta o Recupera il \_ contesto PCCERT di un certificato.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Proprietà ICertContext:: CertContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329343"
---
# <a name="icertcontextcertcontext-property"></a>Proprietà ICertContext:: CertContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

La proprietà **CertContext** imposta o Recupera il \_ contesto PCCERT di un certificato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Valore proprietà

Contesto PCCERT \_ del certificato.

## <a name="error-codes"></a>Codici di errore

Se i metodi di accesso alle proprietà **inseriscono \_ CertContext** e **get \_ CertContext** ha esito positivo, restituiscono S \_ OK.

Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Per liberare il contesto, è necessario chiamare il metodo [**FreeContext**](icertcontext-freecontext.md) o la funzione [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) .

Se si imposta la proprietà **CertContext** , lo stato dell'intero oggetto [**certificato**](certificate.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




