---
description: ICE57 convalida che i singoli componenti non combinano i dati per computer e per utente. Questa azione personalizzata ICE controlla le voci del registro di sistema, i file, i percorsi delle chiavi di directory e i collegamenti non annunciati.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232855"
---
# <a name="ice57"></a>ICE57

ICE57 convalida che i singoli componenti non combinano i dati per computer e per utente. Questa azione personalizzata ICE controlla le voci del registro di sistema, i file, i percorsi delle chiavi di directory e i collegamenti non annunciati.

La combinazione di dati per singolo utente e computer nello stesso componente può comportare solo l'installazione parziale del componente per alcuni utenti in un ambiente multiutente.

Vedere la proprietà [**ALLUSERS**](allusers.md) .

## <a name="result"></a>Risultato

ICE57 Invia un errore se trova un componente che contiene le voci del registro di sistema per computer e per utente, i file, i percorsi delle chiavi di directory o i collegamenti non annunciati.

## <a name="example"></a>Esempio

ICE57reports gli errori seguenti per l'esempio illustrato.

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

[Tabella componenti](component-table.md) (parziale)



| Componente  | Directory  | Attributi | KeyPath |
|------------|------------|------------|---------|
| Component1 | Directory | 0          | FileA   |
| Component2 | Directory | 4          | RegKeyB |
| Component3 | Directory | 0          | FileC   |
| Component4 | Directory | 4          | RegKeyD |



 

[Tabella del registro di sistema](registry-table.md) (parziale)



| Registro | Radice | Componente\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Component1  |
| RegKeyB  | 1    | Component2  |
| RegKeyC  | -1   | Component3  |
| RegKeyD  | -1   | Component4  |



 

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ |
|-------|-------------|
| FileA | Component1  |
| FileB | Component2  |
| FileC | Component3  |
| Campo | Component4  |



 

[Tabella directory](directory-table.md)



| Directory  | \_Padre directory | DefaultDir |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| Directory | TARGETDIR         | Directory |



 

Per correggere gli errori, riorganizzare l'applicazione in modo che ogni componente contenga solo risorse per utente o per computer e non entrambi.

Il primo messaggio di errore viene pubblicato perché Component1 contiene Filea (per computer) e la chiave del registro di sistema HKCU RegKeyA (per utente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



