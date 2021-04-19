---
description: Il metodo Step sposta il flusso DVD-Video in base al numero di frame specificato.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Metodo Step
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316307"
---
# <a name="step-method"></a>Metodo Step

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `Step` metodo fa avanzare il flusso DVD-Video in base al numero di frame specificato.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Specifica il numero di frame da scorrere come Integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, chiamare [**CanStep**](canstep-method.md) per determinare se il decodificatore supporta l'esecuzione del frame.

Se il DVD-Video viene riprodotto in modalità inversa quando viene chiamato questo metodo e il decodificatore supporta l'esecuzione di un frame inverso, l'esecuzione del frame viene eseguita in ordine inverso.

 

 



