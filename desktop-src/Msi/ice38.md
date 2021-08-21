---
description: ICE38 verifica che ogni componente installato nel profilo dell'utente corrente specifichi anche una chiave del Registro di sistema nella radice HKEY CURRENT USER nella colonna KeyPath della \_ \_ tabella Component.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3f90b7f6c0624da266b23dee3a50489f34604d6c99783b337eeca77bb32ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528461"
---
# <a name="ice38"></a>ICE38

ICE38 verifica che ogni componente installato nel profilo dell'utente corrente specifichi anche una chiave del Registro di sistema nella radice **HKEY \_ CURRENT \_ USER** nella colonna KeyPath della tabella [Component](component-table.md).

## <a name="result"></a>Risultato

ICE38 invia un errore se un componente installato nel profilo dell'utente non specifica una chiave del Registro di sistema HKCU.

## <a name="example"></a>Esempio

ICE38 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE38                                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il componente Component1 viene installato nel profilo utente. Deve usare una chiave del Registro di sistema in HKCU come KeyPath, non come file.                    | Il valore della colonna attributes di Component1 è 0, ovvero il componente deve usare un file come KeyPath. Ciò causa difficoltà quando più utenti installano il componente nello stesso computer. Per correggere l'errore in Component1, impostare il bit RegistryKeyPath nella colonna Attributi della tabella [Component](component-table.md) e modificare la voce nella colonna KeyPath su un valore elencato nella colonna Registry della tabella [Registry](registry-table.md).<br/>                                                                                |
| Il componente Component2 viene installato nel profilo utente. Deve usare una chiave del Registro di sistema in HKCU come KeyPath. KeyPath è attualmente NULL. | Component2 ha il bit RegistryKeyPath impostato nella colonna Attributi della [tabella Component](component-table.md). Il campo KeyPath deve pertanto contenere una chiave per la colonna Registry della tabella [del](registry-table.md) Registro di sistema, ma la colonna KeyPath è Null. Per correggere l'errore, modificare il valore KeyPath in una voce valida nella tabella Registry.<br/>                                                                                                                                                                                                     |
| Il componente Component3 viene installato nel profilo utente. La chiave del Registro di sistema KeyPath deve essere in HKCU.                                      | Il bit RegistryKeyPath di Component3 è impostato nella colonna Attributes della tabella [Component,](component-table.md) ma la radice della voce del Registro di sistema specificata nella colonna Radice della tabella Registry specifica **HKEY \_ LOCAL \_ MACHINE** anziché **HKEY \_ CURRENT \_ USER.** Per correggere l'errore, usare una voce del Registro di sistema valida in **HKEY \_ LOCAL \_ MACHINE** come KeyPath per questo componente oppure modificare il valore nella colonna Radice della tabella [Registro](registry-table.md) di sistema in -1 o 1.<br/>                                                                  |
| La voce del Registro di sistema KeyPath per il componente Component4 non esiste.                                                                 | Component4 ha il bit RegistryKeyPath impostato nella colonna Attributes della tabella [Component,](component-table.md) ma la voce nella colonna KeyPath non esiste nella tabella [del Registro di sistema](registry-table.md). Per correggere l'errore, aggiungere alla tabella Del Registro di sistema una voce per Reg4 in **HKEY \_ CURRENT \_ USER**.<br/>                                                                                                                                                                                                                                      |
| La voce del Registro di sistema Reg5 è impostata come KeyPath per il componente Component5, ma tale voce del Registro di sistema non appartiene a Component5.      | La voce del Registro di sistema a cui si fa riferimento nella colonna KeyPath del componente è stata trovata e si trova sotto l'albero HKCU, ma la colonna Component della voce del Registro di sistema non fa riferimento allo stesso componente che lo ha elencato come \_ KeyPath. Ciò significa che la voce del Registro di sistema usata come KeyPath del componente verrà creata solo quando è stato installato un altro componente. Per correggere questo errore, modificare il valore KeyPath in modo che faccia riferimento a una voce del Registro di sistema che appartiene al componente oppure modificare la voce del Registro di sistema in modo che appartenga al componente usandola come KeyPath.<br/> |



 

[Tabella directory](directory-table.md) (parziale)



| Directory | Directory \_ Parent | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | Cartella Desktop   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | Subdir          |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Directory\_ | Attributi | KeyPath |
|------------|-------------|------------|---------|
| Componente1 | Dir1        | 0          | File1   |
| Componente2 | Dir2        | 4          |         |
| Componente3 | Dir3        | 4          | Reg3    |
| Componente4 | Dir4        | 4          | Reg4    |
| Componente5 | Dir5        | 4          | Reg5    |



 

[Tabella del Registro di](registry-table.md) sistema (parziale)



| Registro | Radice | Valore | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Componente3  |
| Reg5     | 0    |       | Componente4  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




