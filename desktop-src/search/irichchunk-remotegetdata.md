---
description: Recupera la stringa di input e PROPVARIANT che rappresenta un blocco di dati. La chiamata a questo metodo equivale alla chiamata a GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Metodo IRichChunk:: RemoteGetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128506"
---
# <a name="irichchunkremotegetdata-method"></a>Metodo IRichChunk:: RemoteGetData

Recupera la stringa di input e [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) che rappresenta un blocco di dati. La chiamata a questo metodo equivale alla chiamata a [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFirstPos* \[ out\]
</dt> <dd>

Riceve la posizione iniziale in base zero dell'intervallo. Questo parametro può essere **NULL**.

</dd> <dt>

*pLength* \[ out\]
</dt> <dd>

Riceve la lunghezza dell'intervallo. Questo parametro può essere **NULL**.

</dd> <dt>

*ppsz* \[ out\]
</dt> <dd>

Riceve il valore stringa Unicode associato oppure **null** se non è disponibile.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Riceve il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) associato oppure **VT \_ vuoto** se non è disponibile. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
