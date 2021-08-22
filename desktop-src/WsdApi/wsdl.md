---
description: Specifica un file WSDL da elaborare per le informazioni sul contratto.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: Elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158141fb8afdc216c47639f6bbb50c1d399e25f202ebbdd2f0a2c045859bffb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049519"
---
# <a name="wsdl-element"></a>Elemento wsdl

Specifica un file WSDL da elaborare per le informazioni sul contratto.

## <a name="usage"></a>Utilizzo

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                           | Descrizione                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeImport**](excludeimport.md)<br/> | Impedisce la generazione di istruzioni import per destinazioni specificate denominate in un \<wsdl:import> elemento in un file WSDL. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Specifica il percorso di download per una \<wsdl:import> direttiva che non specifica in modo esplicito un percorso.<br/> <br/>           |
| [**Percorso**](path.md)<br/>                   | File e percorso del file di input WSDL.<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

Tutti [**gli elementi importHint**](importhint.md) [**o excludeImport**](excludeimport.md) visualizzati dopo l'elemento [**path**](path.md) in un file di configurazione XML verranno ignorati.

## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




