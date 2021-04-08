---
description: ICE38 verifica che ogni componente installato nel profilo dell'utente corrente specifichi anche una chiave del registro \_ \_ di sistema nella radice utente corrente di HKEY nella colonna percorso chiave della tabella dei componenti.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057807"
---
# <a name="ice38"></a>ICE38

ICE38 verifica che ogni componente installato nel profilo dell'utente corrente specifichi anche una chiave del registro di sistema nella radice **\_ \_ utente corrente di HKEY** nella colonna percorso chiave della tabella dei [componenti](component-table.md).

## <a name="result"></a>Risultato

ICE38 Invia un errore se un componente installato nel profilo dell'utente non specifica una chiave del registro di sistema HKCU.

## <a name="example"></a>Esempio

ICE38 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE38                                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il componente Component1 viene installato nel profilo utente. Deve usare una chiave del registro di sistema in HKCU come percorso di chiave, non come file.                    | Il valore della colonna Attributes di Component1 è 0, il che significa che il componente deve usare un file come percorso di proprietà. Ciò causa problemi quando più utenti installano il componente nello stesso computer. Per correggere l'errore in Component1, impostare il bit RegistryKeyPath nella colonna attributi della tabella dei [componenti](component-table.md) e modificare la voce nella colonna percorso chiave impostando un valore elencato nella colonna Registry della [tabella del registro di sistema](registry-table.md).<br/>                                                                                |
| Il componente Component2 viene installato nel profilo utente. Deve usare una chiave del registro di sistema in HKCU come percorso della chiave. Il percorso della neuropatia è attualmente NULL. | Component2 ha il bit RegistryKeyPath impostato nella colonna Attributes della [tabella Component](component-table.md). Il campo del percorso di chiave deve quindi contenere una chiave per la colonna del registro di sistema della [tabella del registro di sistema](registry-table.md) , ma la colonna del percorso della chiave è null. Per correggere l'errore, modificare il valore del percorso di chiave in una voce valida nella tabella del registro di sistema.<br/>                                                                                                                                                                                                     |
| Il componente Component3 viene installato nel profilo utente. La chiave del registro di sistema del percorso della chiave deve rientrare in HKCU.                                      | Per Component3 è impostato il bit RegistryKeyPath nella colonna attributi della [tabella dei componenti](component-table.md) , ma la radice della voce del registro di sistema specificata nella colonna radice della tabella del registro di sistema specifica **HKEY \_ \_ computer locale** anziché **HKEY \_ \_ utente corrente**. Per correggere l'errore, usare una voce del registro di sistema valida nel **\_ \_ computer locale HKEY** come percorso di chiave per il componente o modificare il valore nella colonna radice della [tabella del registro di sistema](registry-table.md) su-1 o 1.<br/>                                                                  |
| La voce del registro di sistema del percorso di chiave per il componente Component4 non esiste.                                                                 | Component4 ha il bit RegistryKeyPath impostato nella colonna Attributes della [tabella Components](component-table.md) , ma la voce nella colonna del percorso di chiave non esiste nella [tabella del registro di sistema](registry-table.md). Per correggere l'errore, aggiungere una voce per Reg4 alla tabella del registro di sistema che corrisponde a un **\_ \_ utente corrente di HKEY**.<br/>                                                                                                                                                                                                                                      |
| La voce del registro di sistema Reg5 è impostata come percorso della chiave per il componente Component5, ma tale voce del registro di sistema non appartiene a Component5.      | La voce del registro di sistema a cui si fa riferimento nella colonna percorso chiave del componente è stata trovata e si trova sotto l'albero HKCU, ma la colonna componente della voce del registro di sistema \_ non fa riferimento allo stesso componente che lo ha elencato come percorso chiave. Ciò significa che la voce del registro di sistema usata come percorso di chiave del componente verrà creata solo quando è stato installato un altro componente. Per correggere questo errore, modificare il valore del percorso di chiave in modo che faccia riferimento a una voce del registro di sistema che appartiene al componente oppure modificare la voce del registro di sistema in modo che appartenga al componente usandola come percorso di chiave.<br/> |



 

[Tabella directory](directory-table.md) (parziale)



| Directory | \_Padre directory | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | Dei |
| Dir2      |                   | Includevano   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | SubDir          |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | Directory\_ | Attributi | KeyPath |
|------------|-------------|------------|---------|
| Component1 | Dir1        | 0          | File1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Component4 | Dir4        | 4          | Reg4    |
| Component5 | Dir5        | 4          | Reg5    |



 

[Tabella del registro di sistema](registry-table.md) (parziale)



| Registro | Radice | Valore | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




