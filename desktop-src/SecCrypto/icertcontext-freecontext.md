---
description: Rilascia un \_ contesto PCCERT acquisito tramite la proprietà CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Metodo ICertContext:: FreeContext'
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
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329345"
---
# <a name="icertcontextfreecontext-method"></a>Metodo ICertContext:: FreeContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

Il metodo **FreeContext** rilascia un \_ contesto PCCERT acquisito tramite la proprietà [**CertContext**](icertcontext-certcontext.md) .

## <a name="syntax"></a>Sintassi


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCertContext* \[ in\]
</dt> <dd>

Contesto PCCERT \_ da rilasciare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Un valore di S \_ OK indica l'esito positivo. Qualsiasi altro valore indica che l'operazione non è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo non rilascia il contesto PCCERT \_ contenuto all'interno di un oggetto [**Certificate**](certificate.md) . Deve essere usato solo per rilasciare un contesto PCCERT \_ acquisito tramite la proprietà [**CertContext**](icertcontext-certcontext.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




