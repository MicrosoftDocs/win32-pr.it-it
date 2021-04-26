---
description: Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un elemento wsdl:import in un file WSDL.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: Elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995878"
---
# <a name="excludeimport-element"></a>Elemento excludeImport

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



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




