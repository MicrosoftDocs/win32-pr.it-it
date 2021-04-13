---
title: Metodo IConfigAsfWriter GetIndexMode
description: Il metodo GetIndexMode recupera la modalità di indice temporale corrente.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Metodo GetIndexMode Windows Media Format
- Metodo GetIndexMode Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399280"
---
# <a name="iconfigasfwritergetindexmode-method"></a>Metodo IConfigAsfWriter:: GetIndexMode

Il metodo **GetIndexMode** recupera la modalità di indice temporale corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbIndexFile* \[ out\]
</dt> <dd>

Puntatore a una variabile di tipo **bool** che riceve l'impostazione della modalità di indice temporale. Il valore **true** indica che il writer ASF WM è configurato per la scrittura di file indicizzati temporaneamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Usare questo metodo per determinare se il [writer ASF WM](wm-asf-writer-filter.md) è attualmente configurato per la scrittura di file ASF indicizzati temporaneamente. Per ulteriori informazioni sui file indicizzati e indicizzati temporalmente, vedere la sezione Note per [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 