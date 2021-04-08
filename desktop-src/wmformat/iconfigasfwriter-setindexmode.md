---
title: Metodo IConfigAsfWriter SetIndexMode
description: Il metodo SetIndexMode consente all'applicazione di controllare se il file verrà indicizzato temporaneamente.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Metodo SetIndexMode Windows Media Format
- Metodo SetIndexMode Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046790"
---
# <a name="iconfigasfwritersetindexmode-method"></a>Metodo IConfigAsfWriter:: SetIndexMode

Il metodo **SetIndexMode** consente all'applicazione di controllare se il file verrà indicizzato temporaneamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIndexFile* \[ in\]
</dt> <dd>

Variabile di tipo **bool**; **True** indica che il file verrà indicizzato temporaneamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il [writer ASF WM](wm-asf-writer-filter.md) crea file ASF indicizzati temporaneamente. Esegue l'indicizzazione quando il grafico si arresta. È possibile disabilitare questo comportamento se si vuole eseguire l'indicizzazione basata su frame come passaggio di post-elaborazione. Per creare un file indicizzato con frame, chiamare **SetIndexMode**(false), creare il file e quindi usare direttamente i metodi Windows Media Format SDK per creare un indice basato su frame per il file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 