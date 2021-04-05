---
description: ICE43 verifica che i collegamenti che non fanno riferimento a una funzionalità come destinazione (collegamenti non annunciati) si trovino in componenti con una voce del registro di sistema HKCU come percorso della chiave.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9df4a6051557fca3e185f56ca3ad7978c2c0b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131870"
---
# <a name="ice43"></a>ICE43

ICE43 verifica che i collegamenti che non fanno riferimento a una funzionalità come destinazione (collegamenti non annunciati) si trovino in componenti con una voce del registro di sistema HKCU come percorso della chiave.

## <a name="result"></a>Risultato

ICE43 Invia un messaggio di errore se un collegamento non annunciato si trova in un componente che non ha una voce del registro di sistema HKCU come percorso della chiave.

## <a name="example"></a>Esempio

ICE43 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE43                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il componente Component1 include collegamenti non annunciati. Deve usare una chiave del registro di sistema in HKCU come percorso di chiave, non come file.                    | La colonna Attributes di Component1 è 0, il che significa che il componente utilizza un file come percorso di proprietà. In questo modo, i collegamenti non annunciati in questo componente verranno installati solo per il primo utente nel computer. Gli utenti che installano il componente in un secondo momento non vedranno i collegamenti perché il componente viene visualizzato nel programma di installazione come già esistente nel computer. Per correggere l'errore, impostare il bit RegistryKeyPath degli attributi per passare il componente a una voce del registro di sistema, quindi modificare il valore del percorso di chiave in una voce valida nella tabella del registro di sistema.<br/> |
| Il componente Component2 include collegamenti non annunciati. Deve usare una chiave del registro di sistema in HKCU come percorso della chiave. Il percorso della neuropatia è attualmente null. | La colonna Attributes è impostata in modo da usare il registro di sistema, ma il percorso della chiave è null. Il percorso della chiave deve fare riferimento a una voce nella tabella del registro di sistema. Per correggere l'errore, modificare il valore del percorso di chiave in una voce valida nella tabella del registro di sistema.<br/>                                                                                                                                                                                                                                                                                                                               |
| Il componente Component3 include collegamenti non annunciati. La chiave del registro di sistema del percorso della chiave deve rientrare in HKCU.                                       | La colonna attributi viene impostata in modo da utilizzare il registro di sistema, ma la voce del registro di sistema a cui si fa riferimento non è in HKCU. Per correggere l'errore, passare a un'altra voce del registro di sistema come percorso di chiave per il componente o modificare il valore radice della voce del registro di sistema in-1 o 1.<br/>                                                                                                                                                                                                                                                                             |
| La voce del registro di sistema del percorso di chiave per il componente Component4 non esiste.                                                                     | La voce del registro di sistema a cui si fa riferimento nella colonna percorso chiave del componente non è presente nella tabella del registro di sistema. Per correggere l'errore, creare una voce.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La voce del registro di sistema Reg5 è impostata come percorso della chiave per il componente Component5, ma tale voce del registro di sistema non appartiene a Component5.          | È presente una voce del registro di sistema a cui si fa riferimento nella colonna percorso chiave del componente che si trova sotto l'albero HKCU, ma la colonna componente della voce del registro di sistema \_ non si riferisce allo stesso componente che lo ha elencato come percorso chiave. Ciò significa che la voce del registro di sistema usata come percorso di chiave del componente viene creata solo se è stato installato un altro componente. Per correggere l'errore, modificare il valore del percorso di chiave in modo che faccia riferimento a una voce del registro di sistema che appartiene al componente o modificare la voce del registro di sistema in modo che appartenga al componente usandola come percorso di chiave.<br/>   |



 

[Tabella componenti](component-table.md) (parziale)



| Componente  | Attributi | KeyPath |
|------------|------------|---------|
| Component1 | 0          | File1   |
| Component2 | 4          |         |
| Component3 | 4          | Reg3    |
| Component4 | 4          | Reg4    |
| Component5 | 4          | Reg5    |



 

[Tabella del registro di sistema](registry-table.md) (parziale)



| Registro | Radice | Valore | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




