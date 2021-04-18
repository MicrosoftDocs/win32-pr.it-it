---
description: Recupera un numero specificato di byte casuali dal generatore di numeri casuali di sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng (funzione)
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
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306473"
---
# <a name="systemprng-function"></a>SystemPrng (funzione)

\[**SystemPrng** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

La funzione **SystemPrng** recupera un numero specificato di byte casuali dal generatore di numeri casuali di sistema.

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

*pbRandomData* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve i byte recuperati.

</dd> <dt>

*cbRandomData* \[ in\]
</dt> <dd>

Numero di byte da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows Vista con SP1 \[\]<br/>                                                                                                                                                                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys in Windows Server 2008 e Windows Vista con SP1; </dt> <dt>Cng.sys in Windows 7 e Windows Server 2008 R2</dt> </dl> |



 

 




