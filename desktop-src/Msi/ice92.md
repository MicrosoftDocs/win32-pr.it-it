---
description: ICE92 verifica che un componente senza un GUID ID componente non sia specificato anche come componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882733"
---
# <a name="ice92"></a>ICE92

ICE92 verifica che un componente senza un GUID ID componente non sia specificato anche come componente permanente. Questa azione personalizzata ICE controlla la [tabella](component-table.md) dei componenti senza un [GUID](guid.md) specificato nel campo ComponentID e verifica che il flag **msidbComponentAttributesPermanent** non sia stato impostato nel campo attributi. ICE92 verifica anche che nessun componente abbia entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** .

Se la colonna ComponentId è null, il programma di installazione non registra il componente e il componente non può essere rimosso o ripristinato dal programma di installazione.

## <a name="result"></a>Risultato

ICE92 invia il seguente errore.



| Errore ICE92                                                          | Descrizione                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il componente ' \[ 1 \] ' non contiene ComponentID ed è contrassegnato come permanente. | La voce per questo componente nella tabella dei componenti presenta un valore null nella colonna ComponentId e include **msidbComponentAttributesPermanent** nella colonna Attributes. |



 

ICE92 invia il seguente avviso.



| Avviso di ICE92                                                                                                                                                           | Descrizione                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il componente ' \[ 1 \] ' è contrassegnato come Permanent e Uninstall-on-sostituzione. L'attributo Uninstall-on-sostituzione verrà ignorato perché il componente è permanente. | Per la voce per questo componente nella [tabella dei componenti](component-table.md) sono specificati entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** . |



 

## <a name="example"></a>Esempio

ICE92 segnala l'errore seguente per l'esempio:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Tabella componenti](component-table.md) (parziale)



| Componente  | ComponentId | Directory\_ | Attributi | KeyPath |
|------------|-------------|-------------|------------|---------|
| Component1 |             | Directory  | 16         | FileA   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



