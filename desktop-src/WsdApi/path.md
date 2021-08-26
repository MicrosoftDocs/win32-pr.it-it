---
description: Specifica il percorso e il nome file di un file WSDL. Il percorso può essere un percorso assoluto o relativo del file, ma non deve essere un URL.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: Elemento path (Servizi Web nei dispositivi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597248a2cbead5afdeb2fd1cd41613e1c4617b7be1ea636abb3ddbd2cdc92be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071421"
---
# <a name="path-element"></a>elemento path

Specifica il percorso e il nome file di un file WSDL. Il percorso può essere un percorso assoluto o relativo del file, ma non deve essere un URL.

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

Il codice XML seguente mostra un elemento **path** valido.

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




