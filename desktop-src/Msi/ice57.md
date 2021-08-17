---
description: ICE57 convalida che i singoli componenti non combinano dati per computer e per utente. Questa azione personalizzata ICE controlla le voci del Registro di sistema, i file, i percorsi delle chiavi di directory e i collegamenti non annunciati.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d875264ed1fbc0f7dedac863c21801e5180ae879c9c255af7cf4b36e5d402970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635162"
---
# <a name="ice57"></a>ICE57

ICE57 convalida che i singoli componenti non combinano dati per computer e per utente. Questa azione personalizzata ICE controlla le voci del Registro di sistema, i file, i percorsi delle chiavi di directory e i collegamenti non annunciati.

La combinazione di dati per utente e per computer nello stesso componente potrebbe comportare solo l'installazione parziale del componente per alcuni utenti in un ambiente multi-utente.

Vedere la [**proprietà ALLUSERS.**](allusers.md)

## <a name="result"></a>Risultato

ICE57 invia un errore se trova un componente che contiene voci del Registro di sistema per computer e per utente, file, percorsi delle chiavi di directory o collegamenti non annunciati.

## <a name="example"></a>Esempio

ICE57reporta gli errori seguenti per l'esempio illustrato.

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Directory  | Attributi | KeyPath |
|------------|------------|------------|---------|
| Componente1 | DirectoryA | 0          | FileA   |
| Componente2 | DirectoryA | 4          | RegKeyB |
| Componente3 | DirectoryA | 0          | FileC   |
| Componente4 | DirectoryA | 4          | RegKeyD |



 

[Tabella del Registro di](registry-table.md) sistema (parziale)



| Registro | Radice | Componente\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Componente1  |
| RegKeyB  | 1    | Componente2  |
| RegKeyC  | -1   | Componente3  |
| RegKeyD  | -1   | Componente4  |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ |
|-------|-------------|
| FileA | Componente1  |
| FileB | Componente2  |
| FileC | Componente3  |
| Archiviato | Componente4  |



 

[Tabella directory](directory-table.md)



| Directory  | Padre \_ della directory | DefaultDir |
|------------|-------------------|------------|
| Targetdir  |                   | SourceDir  |
| DirectoryA | Targetdir         | DirectoryA |



 

Per correggere gli errori, riorganizzare l'applicazione in modo che ogni componente contenga solo risorse per utente o per computer e non per entrambe.

Il primo messaggio di errore viene pubblicato perché Component1 contiene FileA (per computer) e la chiave del Registro di sistema HKCU RegKeyA (per utente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



