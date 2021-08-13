---
description: ICE43 verifica che i collegamenti che non fanno riferimento a una funzionalità come destinazione (collegamenti non annunciati) siano presenti in componenti con una voce del Registro di sistema HKCU come percorso della chiave.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69af661b22d851b50a74bdffb9534b1e269dde4e428440882ee2d52813a68c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635207"
---
# <a name="ice43"></a>ICE43

ICE43 verifica che i collegamenti che non fanno riferimento a una funzionalità come destinazione (collegamenti non annunciati) siano presenti in componenti con una voce del Registro di sistema HKCU come percorso della chiave.

## <a name="result"></a>Risultato

ICE43 invia un messaggio di errore se un collegamento non annunciato si trova in un componente che non dispone di una voce del Registro di sistema HKCU come percorso della chiave.

## <a name="example"></a>Esempio

ICE43 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE43                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Component Component1 include collegamenti non annunciati. Deve usare una chiave del Registro di sistema in HKCU come KeyPath, non come file.                    | La colonna attributes di Component1 è 0, vale a dire che il componente usa un file come KeyPath. In questo modo i collegamenti non annunciati in questo componente vengono installati solo per il primo utente nel computer. Gli utenti che installano il componente in un secondo momento non visualizzano i collegamenti perché il componente viene visualizzato nel programma di installazione come già esistente nel computer. Per correggere l'errore, impostare il bit RegistryKeyPath degli attributi per impostare Component su una voce del Registro di sistema, quindi modificare il valore KeyPath in una voce valida nella tabella Registry.<br/> |
| Component Component2 include collegamenti non annunciati. Deve usare una chiave del Registro di sistema in HKCU come KeyPath. KeyPath è attualmente Null. | La colonna Attributes è impostata per l'uso del Registro di sistema, ma KeyPath è Null. KeyPath deve fare riferimento a una voce nella tabella del Registro di sistema. Per correggere l'errore, modificare il valore KeyPath in una voce valida nella tabella Registry.<br/>                                                                                                                                                                                                                                                                                                                               |
| Component Component3 include collegamenti non annunciati. La chiave del Registro di sistema KeyPath deve essere in HKCU.                                       | La colonna Attributi è impostata per l'uso del Registro di sistema, ma la voce del Registro di sistema a cui si fa riferimento non si trova in HKCU. Per correggere l'errore, passare a una voce del Registro di sistema diversa da KeyPath per questo componente oppure modificare il valore Radice della voce del Registro di sistema in -1 o 1.<br/>                                                                                                                                                                                                                                                                             |
| La voce del Registro di sistema KeyPath per il componente Component4 non esiste.                                                                     | La voce del Registro di sistema a cui si fa riferimento nella colonna KeyPath del componente non si trova nella tabella del Registro di sistema. Per correggere l'errore, creare una voce.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| La voce del Registro di sistema Reg5 è impostata come KeyPath per il componente Component5, ma tale voce del Registro di sistema non appartiene a Component5.          | È presente una voce del Registro di sistema a cui si fa riferimento nella colonna KeyPath del componente che si trova sotto l'albero HKCU, ma la colonna Component della voce del Registro di sistema non fa riferimento allo stesso componente che lo ha elencato come \_ KeyPath. Ciò significa che la voce del Registro di sistema usata come KeyPath del componente viene creata solo se è stato installato un altro componente. Per correggere l'errore, modificare il valore KeyPath in modo che faccia riferimento a una voce del Registro di sistema che appartiene al componente o modificare la voce del Registro di sistema in modo che appartenga al componente usandola come KeyPath.<br/>   |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Attributi | KeyPath |
|------------|------------|---------|
| Componente1 | 0          | File1   |
| Componente2 | 4          |         |
| Componente3 | 4          | Reg3    |
| Componente4 | 4          | Reg4    |
| Componente5 | 4          | Reg5    |



 

[Tabella del Registro di](registry-table.md) sistema (parziale)



| Registro | Radice | Valore | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Componente3  |
| Reg5     | 0    |       | Componente4  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




