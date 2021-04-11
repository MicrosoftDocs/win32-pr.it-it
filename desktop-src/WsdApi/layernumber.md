---
description: Definisce il numero del livello di codice da generare.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231815"
---
# <a name="layernumber-element"></a>elemento layerNumber

Definisce il numero del livello di codice da generare.

## <a name="usage"></a>Utilizzo

``` syntax
<layerNumber/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

I numeri di livello vengono usati nelle tabelle di runtime per distinguere un livello di codice per un altro. WSDAPI usa il codice generato con un numero di livello pari a 0.

In genere, questo valore sarà 1, a indicare che il codice generato è sovrapposto a WSDAPI e a nessun altro livello. In alcuni casi, è possibile usare numeri più alti. Se, ad esempio, un'azienda produce codice per una classe di dispositivi (livello 1), è possibile che un particolare fornitore di hardware desideri aggiungere un livello aggiuntivo con numero 2.

I valori validi, tranne nel caso di WSDAPI, sono maggiori di 0 e minori di 16.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




