---
description: Rilascia un contesto PCCERT \_ CHAIN acquisito tramite la proprietà \_ ChainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: Metodo IChainContext::FreeContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 10a6d0576cefd1c28e8f05fe455b89be90dcd36386b4312ef1921511616bce2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005489"
---
# <a name="ichaincontextfreecontext-method"></a>Metodo IChainContext::FreeContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

Il **metodo FreeContext** rilascia un CONTESTO PCCERT \_ CHAIN acquisito tramite la proprietà \_ [**ChainContext.**](ichaincontext-chaincontext.md)

## <a name="syntax"></a>Sintassi


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pChainContext* \[ Pollici\]
</dt> <dd>

CONTESTO DELLA CATENA PCCERT \_ \_ da rilasciata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica l'esito positivo. Qualsiasi altro valore indica che l'operazione non è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo non rilascia l'oggetto PCCERT \_ CHAIN CONTEXT contenuto in un oggetto \_ [**Chain.**](chain.md) Deve essere usato solo per rilasciare un CONTESTO CHAIN PCCERT \_ acquisito tramite la proprietà \_ [**ChainContext.**](ichaincontext-chaincontext.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




