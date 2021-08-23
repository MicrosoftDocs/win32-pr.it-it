---
description: Il metodo CanStep determina se il decodificatore MPEG-2 nel sistema locale può eseguire l'esecuzione delle istruzioni dei fotogrammi in una direzione specificata.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Metodo CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6ca29443e059cd5ebfbbb553f67cf50b1cb13e1bc8d7199ac6cfae704cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017589"
---
# <a name="canstep-method"></a>Metodo CanStep

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `CanStep` metodo determina se il decodificatore MPEG-2 nel sistema locale può eseguire l'esecuzione delle istruzioni dei fotogrammi in una direzione specificata.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Valore booleano usato come flag per specificare la direzione, in avanti o indietro, della capacità di avanzamento del fotogramma del decodificatore.



| Valore | Descrizione                                          |
|-------|------------------------------------------------------|
| true  | Il decodificatore può tornare indietro?                           |
| false | Il decodificatore può procedere? Si tratta del valore predefinito. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano true se il decodificatore può eseguire un'istruzione nella direzione specificata e false in caso contrario.

## <a name="remarks"></a>Commenti

Non tutti i decodificatori MPEG-2 hardware supportano le nuove funzionalità di esecuzione dei fotogrammi in DirectShow® 8.0. Questo metodo esegue una query sul decodificatore per le funzionalità di esecuzione delle istruzioni dei frame. Se il decodificatore può eseguire l'esecuzione passo a passo dei fotogrammi, un'applicazione può usare il [**metodo Step**](step-method.md) per scorrere i fotogrammi. Questo metodo restituirà sempre **true se** viene usato un decodificatore software.

 

 



