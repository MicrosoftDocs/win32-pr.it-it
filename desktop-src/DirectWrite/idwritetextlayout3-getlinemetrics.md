---
title: Metodo IDWriteTextLayout3 GetLineMetrics
description: Recupera le proprietà di ogni riga.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Scrittura diretta metodo GetLineMetrics
- Metodo GetLineMetrics scrittura diretta, interfaccia IDWriteTextLayout3
- IDWriteTextLayout3 Interface Direct Write, metodo GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477518"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>Metodo IDWriteTextLayout3:: GetLineMetrics

Recupera le proprietà di ogni riga.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lineMetrics* \[ out\]
</dt> <dd>

Matrice da riempire con le informazioni sulla riga.

</dd> <dt>

*maxLineCount* 
</dt> <dd>

Dimensione massima della matrice lineMetrics.

</dd> <dt>

*actualLineCount* \[ out\]
</dt> <dd>

Dimensioni effettive della matrice lineMetrics necessaria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se maxLineCount non è sufficientemente grande E \_ non è \_ sufficiente \_ un buffer, equivalente a HRESULT \_ di \_ Win32 (errore \_ buffer insufficiente \_ ), viene restituito e actualLineCount è impostato sul numero di righe necessarie.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                 |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





