---
description: Imposta o recupera l'oggetto PCCERT \_ CHAIN CONTEXT di un \_ certificato.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: Proprietà IChainContext::ChainContext
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
ms.openlocfilehash: d5e7bc92aa798766538af19cae440542705a859040aed7fc8d9510e3724051f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005499"
---
# <a name="ichaincontextchaincontext-property"></a>Proprietà IChainContext::ChainContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

La **proprietà ChainContext** imposta o recupera l'oggetto PCCERT \_ CHAIN CONTEXT di un \_ certificato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Valore proprietà

CONTESTO PCCERT \_ CHAIN \_ del certificato.

## <a name="error-codes"></a>Codici di errore

Se i metodi di accesso alle **proprietà put \_ ChainContext** **e get \_ ChainContext** hanno esito positivo, restituiscono S \_ OK.

Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

È necessario chiamare il [**metodo FreeContext**](ichaincontext-freecontext.md) o la [**funzione CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) per liberare il contesto.

Se si imposta la **proprietà ChainContext,** lo stato dell'intero [**oggetto Chain**](chain.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




