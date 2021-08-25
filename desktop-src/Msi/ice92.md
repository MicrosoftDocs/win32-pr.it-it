---
description: ICE92 verifica che un componente senza un GUID id componente non sia specificato anche come componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd96126f9255303bb2d78f39bc6fef4312859533d1298b9a9d30afd1b79575fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894881"
---
# <a name="ice92"></a>ICE92

ICE92 verifica che un componente senza un GUID id componente non sia specificato anche come componente permanente. Questa azione personalizzata [](component-table.md) ICE controlla la tabella dei componenti per i componenti senza un [GUID](guid.md) specificato nel campo ComponentId e verifica che il flag **msidbComponentAttributesPermanent** non sia stato impostato nel campo Attributi. ICE92 verifica anche che nessun componente abbia entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence.**

Se la colonna ComponentId è Null, il programma di installazione non registra il componente e il componente non può essere rimosso o ripristinato dal programma di installazione.

## <a name="result"></a>Risultato

ICE92 pubblica l'errore seguente.



| Errore ICE92                                                          | Descrizione                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il componente ' \[ 1 \] ' non ha ComponentId ed è contrassegnato come permanente. | La voce per questo componente nella tabella Component ha null nella colonna ComponentId e **msidbComponentAttributesPermanent** nella colonna Attributes. |



 

ICE92 pubblica l'avviso seguente.



| Avviso ICE92                                                                                                                                                           | Descrizione                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il componente ' \[ 1 \] ' è contrassegnato come permanente e uninstall-on-supersedence. L'attributo uninstall-on-supersedence verrà ignorato perché il componente è permanente. | La voce per questo componente nella tabella [Component](component-table.md) contiene entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** specificati. |



 

## <a name="example"></a>Esempio

ICE92 segnala l'errore seguente per l'esempio:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Componentid | Directory\_ | Attributi | KeyPath |
|------------|-------------|-------------|------------|---------|
| Componente1 |             | DirectoryA  | 16         | FileA   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



