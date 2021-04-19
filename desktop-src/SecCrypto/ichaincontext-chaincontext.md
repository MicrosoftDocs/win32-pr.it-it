---
description: Imposta o Recupera il \_ \_ contesto della catena PCCERT di un certificato.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Proprietà IChainContext:: ChainContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324764"
---
# <a name="ichaincontextchaincontext-property"></a>Proprietà IChainContext:: ChainContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

La proprietà **chainContext** imposta o Recupera il \_ contesto della catena PCCERT \_ di un certificato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Valore proprietà

\_ \_ Contesto della catena PCCERT del certificato.

## <a name="error-codes"></a>Codici di errore

Se i metodi di accesso alle proprietà **inseriscono \_ chainContext** e **get \_ chainContext** ha esito positivo, restituiscono S \_ OK.

Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Per liberare il contesto, è necessario chiamare il metodo [**FreeContext**](ichaincontext-freecontext.md) o la funzione [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) .

Se si imposta la proprietà **chainContext** , lo stato dell'intero oggetto [**Chain**](chain.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




