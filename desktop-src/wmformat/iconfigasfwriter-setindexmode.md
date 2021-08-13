---
title: Metodo IConfigAsfWriter SetIndexMode
description: Il metodo SetIndexMode consente all'applicazione di controllare se il file verrà indicizzato a livello temporale.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Metodo SetIndexMode windows Media Format
- Metodo SetIndexMode windows Media Format , interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter windows Media Format, metodo SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b65fbd3d279b8a66c132d24476b09b0f897c5993ea9a97d86096cf856832f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433613"
---
# <a name="iconfigasfwritersetindexmode-method"></a>Metodo IConfigAsfWriter::SetIndexMode

Il **metodo SetIndexMode** consente all'applicazione di controllare se il file verrà indicizzato a livello temporale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIndexFile* \[ Pollici\]
</dt> <dd>

Variabile di tipo **BOOL**; **TRUE** specifica che il file verrà indicizzato a livello temporale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, [WM ASF Writer](wm-asf-writer-filter.md) crea file ASF con indicizzazione temporale. Esegue l'indicizzazione all'arresto del grafo. È possibile disabilitare questo comportamento se si vuole eseguire un'indicizzazione basata su frame come passaggio di post-elaborazione. Per creare un file indicizzato con frame, chiamare **SetIndexMode**(FALSE), creare il file e quindi usare direttamente i metodi sdk di Windows Media Format per creare un indice basato su frame per il file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 