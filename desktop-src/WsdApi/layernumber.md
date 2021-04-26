---
description: Definisce il numero del livello di codice da generare.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: Elemento layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995488"
---
# <a name="layernumber-element"></a>Elemento layerNumber

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

I numeri di livello vengono usati nelle tabelle di runtime per distinguere un livello di codice per un altro. WSDAPI usa codice generato con un numero di livello 0.

In genere, questo valore sarà 1, a indicare che il codice generato è a livelli su WSDAPI e nessun altro livello. In alcuni casi, è possibile usare numeri più elevati. Ad esempio, se una società produce codice per una classe di dispositivo (livello 1 numerato), un fornitore di hardware specifico potrebbe voler aggiungere un ulteriore livello numerato livello 2.

I valori validi, tranne nel caso di WSDAPI, sono maggiori di 0 e minori di 16.

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




