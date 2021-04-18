---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Istanze di proprietà importanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320972"
---
# <a name="important-property-instances"></a>Istanze di proprietà importanti

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Affinché un client PrintCapabilities sia in grado di costruire un oggetto PrintTicket ragionevole, è necessario che il documento PrintCapabilities fornisca determinate proprietà delle istanze delle funzionalità, nonché le istanze delle opzioni all'interno della funzionalità. Un modulo dell'interfaccia utente generico richiede tali informazioni per costruire un'interfaccia utente. Questa operazione richiede a sua volta che le parole chiave dello schema di stampa definiscano alcune istanze di proprietà che vengono visualizzate come elementi figlio degli elementi Feature e Option.

Gli elementi Feature possono contenere la proprietà seguente.



| Proprietà                  | Valori                                 | Scopo                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SelectionType <br/> | PickOne<br/> PickMany<br/> | Specifica il numero di opzioni che è possibile selezionare per questa funzionalità in un determinato momento, ovvero una (PickOne) o più di una (PickMany). Il client può utilizzare queste informazioni per costruire un oggetto PrintTicket. Queste informazioni influiscono sul comportamento dell'interfaccia utente e sulla convalida PrintTicket da parte del provider.<br/> |



 

Gli elementi option possono contenere la proprietà seguente.



| Proprietà                   | Valori                           | Scopo                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | Vero<br/> Falso<br/> | La selezione della proprietà IdentityOption viene interpretata in modo da indicare che la funzionalità è disabilitata. Una funzionalità che contiene una proprietà SelectionType il cui valore è PickMany deve contenere anche un'opzione con una proprietà IdentityOption. Il codice dell'interfaccia utente (o il client che costruisce un oggetto PrintTicket) deve deselezionare qualsiasi altra opzione se è selezionata la proprietà IdentityOption.<br/> |



 

Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.



| Proprietà              | Valori                          | Scopo                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Mostra<br/> Nascondi<br/> | Specifica se l'elemento padre deve essere visualizzato nell'interfaccia utente. Mostra indica che l'elemento deve essere visualizzato nell'interfaccia utente. Hide indica che l'elemento non deve essere visualizzato nell'interfaccia utente. Se questa proprietà non è definita per un elemento, l'interpretazione predefinita è Show, ovvero viene visualizzato l'elemento.<br/> |



 

Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.



| Proprietà                | valore             | Scopo                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | string<br/> | Specifica la stringa di visualizzazione per l'elemento padre, eseguendo l'override del nome visualizzato predefinito. Può essere utilizzato dai provider PrintCapabilities per presentare un nome visualizzato localizzato e descrittivo dall'utente. Il valore predefinito del nome visualizzato è l'attributo Name dell'elemento padre. <br/> Nel caso di elementi option, se l'attributo name non viene specificato, è necessario che la proprietà DisplayName sia presente.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




