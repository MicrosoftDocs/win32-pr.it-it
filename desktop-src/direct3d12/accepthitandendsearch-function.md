---
description: Usato in un hit shader per eseguire il commit dell'hit corrente e quindi interrompere la ricerca di altri riscontri per il raggio.
ms.assetid: ''
title: Funzione AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 35073145a9b9a4788c6aed3bbae0633f0a9f5b85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813040"
---
# <a name="accepthitandendsearch-function"></a>Funzione AcceptHitAndEndSearch

Usato in un [hit shader per](any-hit-shader.md) eseguire il commit dell'hit corrente e quindi interrompere la ricerca di altri riscontri per il raggio. Se è in esecuzione uno shader di intersezione, l'esecuzione viene arrestata.  L'esecuzione passa [all'hit shader più vicino,](closest-hit-shader.md)se abilitato, con l'hit più vicino registrato fino a questo momento.

## <a name="syntax"></a>Sintassi

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Valore restituito

**void**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Shader chiamabile**](callable-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Miss Shader**](miss-shader.md)
* [**Ray Generation Shader**](ray-generation-shader.md)



## <a name="see-also"></a>Vedi anche

* [Informazioni di riferimento su HLSL di raytracing Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
