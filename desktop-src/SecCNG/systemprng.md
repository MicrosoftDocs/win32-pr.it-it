---
description: Recupera un numero specificato di byte casuali dal generatore di numeri casuali di sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Funzione SystemPrng
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: eae1a46b43278c836ff6ce318dfdce7302bb0e052664a7326f9043a60eec72d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905630"
---
# <a name="systemprng-function"></a>Funzione SystemPrng

\[**SystemPrng** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

La **funzione SystemPrng** recupera un numero specificato di byte casuali dal generatore di numeri casuali di sistema.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbRandomData* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve i byte recuperati.

</dd> <dt>

*cbRandomData* \[ Pollici\]
</dt> <dd>

Numero di byte da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista solo con app desktop SP1 \[\]<br/>                                                                                                                                                                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys in Windows Server 2008 e Windows Vista con SP1;</dt> <dt>Cng.sys in Windows 7 e Windows Server 2008 R2</dt> </dl> |



 

 




