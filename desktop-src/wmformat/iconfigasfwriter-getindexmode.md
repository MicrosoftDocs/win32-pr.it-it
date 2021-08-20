---
title: Metodo IConfigAsfWriter GetIndexMode
description: Il metodo GetIndexMode recupera la modalità di indice temporale corrente.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Metodo GetIndexMode windows Media Format
- Metodo GetIndexMode windows Media Format , interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter windows Media Format , metodo GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95eb0e037bbebf62b710317b6e4b9b1224f9d2429712ffaec88dd1703a1c667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655463"
---
# <a name="iconfigasfwritergetindexmode-method"></a>Metodo IConfigAsfWriter::GetIndexMode

Il **metodo GetIndexMode** recupera la modalità di indice temporale corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbIndexFile* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile di tipo **BOOL** che riceve l'impostazione della modalità di indice temporale. Il valore **TRUE** indica che WM ASF Writer è configurato per scrivere file indicizzati a livello temporale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se non riesce, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usare questo metodo per determinare se [WM ASF Writer](wm-asf-writer-filter.md) è attualmente configurato per scrivere file ASF indicizzati a livello temporale. Per altre informazioni sui file con indicizzazione temporale e con frame, vedere Note per [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 