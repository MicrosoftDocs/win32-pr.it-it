---
description: Specifica il percorso e il nome file di un file WSDL. Il percorso può essere assoluto o relativo al file, ma non deve essere un URL.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: Elemento path (servizi Web nei dispositivi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48df5a156149f00b8b153ccc0d46d6d2d34a1ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994308"
---
# <a name="path-element"></a>path - elemento

Specifica il percorso e il nome file di un file WSDL. Il percorso può essere assoluto o relativo al file, ma non deve essere un URL.

## <a name="usage"></a>Utilizzo

``` syntax
<path/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | File WSDL da elaborare per le informazioni sul contratto.<br/> <br/> |



## <a name="examples"></a>Esempio

Nel codice XML seguente viene illustrato un elemento **di percorso** valido.

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




