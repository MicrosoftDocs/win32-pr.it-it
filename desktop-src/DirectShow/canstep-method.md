---
description: Il metodo CanStep determina se il decodificatore MPEG-2 nel sistema locale può eseguire lo stepping del frame in una direzione specificata.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Metodo CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048913"
---
# <a name="canstep-method"></a>Metodo CanStep

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `CanStep` metodo determina se il decodificatore MPEG-2 nel sistema locale può eseguire lo stepping del frame in una direzione specificata.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Valore booleano usato come flag per specificare la direzione, avanti o indietro, della capacità di esecuzione dei frame del decodificatore.



| Valore | Descrizione                                          |
|-------|------------------------------------------------------|
| true  | È possibile eseguire il passaggio del decodificatore indietro?                           |
| false | Il decodificatore può andare avanti? Si tratta del valore predefinito. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano true se il decodificatore può eseguire un'istruzione nella direzione specificata e false in caso contrario.

## <a name="remarks"></a>Commenti

Non tutti i decodificatori MPEG-2 hardware supportano le nuove funzionalità di avanzamento dei frame in DirectShow® 8,0. Questo metodo esegue una query sul decodificatore per le funzionalità di avanzamento dei frame. Se il decodificatore è in grado di eseguire l'esecuzione dei frame, un'applicazione può usare il metodo [**Step**](step-method.md) per scorrere i frame. Questo metodo restituirà sempre **true** se viene usato un decodificatore software.

 

 



