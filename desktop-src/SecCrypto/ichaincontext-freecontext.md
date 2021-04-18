---
description: Rilascia un \_ \_ contesto della catena PCCERT acquisito tramite la proprietà chainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Metodo IChainContext:: FreeContext'
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
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329223"
---
# <a name="ichaincontextfreecontext-method"></a>Metodo IChainContext:: FreeContext

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.\]

Il metodo **FreeContext** rilascia un \_ contesto della catena PCCERT \_ acquisito tramite la proprietà [**chainContext**](ichaincontext-chaincontext.md) .

## <a name="syntax"></a>Sintassi


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pChainContext* \[ in\]
</dt> <dd>

Contesto della \_ catena PCCERT \_ da rilasciare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Un valore di S \_ OK indica l'esito positivo. Qualsiasi altro valore indica che l'operazione non è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo non rilascia il contesto della \_ catena PCCERT \_ contenuto all'interno di un oggetto [**Chain**](chain.md) . Deve essere usato solo per rilasciare un \_ \_ contesto della catena PCCERT acquisito tramite la proprietà [**chainContext**](ichaincontext-chaincontext.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




