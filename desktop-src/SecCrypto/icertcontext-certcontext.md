---
description: Imposta o recupera l'elemento PCCERT \_ CONTEXT di un certificato.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: Proprietà ICertContext::CertContext
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
ms.openlocfilehash: 5c517384bdffd8723c1e9e0d96683cc4bd4918361acdf19df77286bfbac962b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006369"
---
# <a name="icertcontextcertcontext-property"></a>Proprietà ICertContext::CertContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

La **proprietà CertContext** imposta o recupera il CONTESTO PCCERT \_ di un certificato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Valore proprietà

CONTESTO PCCERT \_ del certificato.

## <a name="error-codes"></a>Codici di errore

Se i metodi di accesso alle **proprietà \_ put CertContext** e **get \_ CertContext** hanno esito positivo, restituiscono S \_ OK.

Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

È necessario chiamare il [**metodo FreeContext**](icertcontext-freecontext.md) o la [**funzione CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) per liberare il contesto.

Se si imposta la **proprietà CertContext,** lo stato dell'intero [**oggetto Certificate**](certificate.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




