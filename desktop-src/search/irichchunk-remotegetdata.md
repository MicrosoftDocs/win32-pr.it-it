---
description: Recupera l'oggetto PROPVARIANT e la stringa di input che rappresenta un blocco di dati. La chiamata a questo metodo è uguale alla chiamata a GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: Metodo IRichChunk::RemoteGetData
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
ms.openlocfilehash: caaa4ab9688ab8169bd0955c8abb1e976e7eb318e94875be1486e61b32e13207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862797"
---
# <a name="irichchunkremotegetdata-method"></a>Metodo IRichChunk::RemoteGetData

Recupera [l'oggetto PROPVARIANT e](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) la stringa di input che rappresenta un blocco di dati. La chiamata a questo metodo è uguale alla chiamata [**a GetData.**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata)

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

*pFirstPos* \[ Cambio\]
</dt> <dd>

Riceve la posizione iniziale in base zero dell'intervallo. Questo parametro può essere **NULL**.

</dd> <dt>

*pLength* \[ Cambio\]
</dt> <dd>

Riceve la lunghezza dell'intervallo. Questo parametro può essere **NULL**.

</dd> <dt>

*ppsz* \[ Cambio\]
</dt> <dd>

Riceve il valore stringa Unicode associato o **NULL** se non disponibile.

</dd> <dt>

*pValue* \[ Cambio\]
</dt> <dd>

Riceve il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) associato o **VT \_ EMPTY** se non disponibile. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
