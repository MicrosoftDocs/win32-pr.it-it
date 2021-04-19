---
description: Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un elemento wsdl:import in un file WSDL.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: ExcludeImport - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380775"
---
# <a name="excludeimport-element"></a>ExcludeImport - elemento

Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un \<wsdl:import> elemento in un file WSDL. Può essere usato per evitare che WsdCodeGen importi destinazioni note, ad esempio le specifiche WS-Addressing e WS-Eventing, anche se si fa riferimento a queste destinazioni nel wsdl.

Il valore di questo elemento deve essere impostato nello spazio dei nomi denominato \<wsdl:import> nell'elemento da escludere.

## <a name="usage"></a>Utilizzo

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | Specifica un file WSDL da elaborare per le informazioni sul contratto.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




