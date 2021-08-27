---
description: Il metodo Step fa avanzare DVD-Video flusso del numero specificato di frame.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Metodo Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5738e8704b24d64a429d8d38f1b9eac2f9b8ff7e22a7e9d1d2a29fb9df4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050311"
---
# <a name="step-method"></a>Metodo Step

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `Step` metodo fa avanzare DVD-Video flusso di dati in base al numero specificato di frame.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframe*
</dt> <dd>

Specifica il numero di fotogrammi di cui eseguire il passaggio come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**CanStep per**](canstep-method.md) determinare se il decodificatore supporta l'esecuzione di istruzioni dei frame.

Se il DVD-Video viene riprodotto in modalità inversa quando viene chiamato questo metodo e il decodificatore supporta l'esecuzione inversa dei fotogrammi, l'esecuzione delle istruzioni del frame viene eseguita in ordine inverso.

 

 



