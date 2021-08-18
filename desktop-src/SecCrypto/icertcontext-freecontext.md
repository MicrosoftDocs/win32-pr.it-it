---
description: Rilascia un CONTESTO PCCERT \_ acquisito tramite la proprietà CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: Metodo ICertContext::FreeContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06809d8950d62f1136b8efc25c8e5b4499e020dce956d65f9e0d4a0e349567de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006189"
---
# <a name="icertcontextfreecontext-method"></a>Metodo ICertContext::FreeContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

Il **metodo FreeContext** rilascia un CONTESTO PCCERT \_ acquisito tramite la proprietà [**CertContext.**](icertcontext-certcontext.md)

## <a name="syntax"></a>Sintassi


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCertContext* \[ Pollici\]
</dt> <dd>

CONTESTO PCCERT \_ da rilasciato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica l'esito positivo. Qualsiasi altro valore indica che l'operazione non è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo non rilascia l'oggetto PCCERT \_ CONTEXT contenuto in un [**oggetto**](certificate.md) Certificato. Deve essere usato solo per rilasciare un CONTESTO PCCERT \_ acquisito tramite la proprietà [**CertContext.**](icertcontext-certcontext.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




