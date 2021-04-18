---
description: Ottiene un IMemoryBuffer come matrice di byte.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Metodo IMemoryBufferByteAccess:: GetBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307076"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>Metodo IMemoryBufferByteAccess:: GetBuffer

Ottiene un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) come matrice di byte.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Puntatore a una matrice di byte contenente i dati del buffer.

</dd> <dt>

*capacità* \[ di out\]
</dt> <dd>

Numero di byte nella matrice restituita

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Quando viene chiamato [**MemoryBuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) , il codice che utilizza questo buffer deve impostare il puntatore del *valore* su null.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 
