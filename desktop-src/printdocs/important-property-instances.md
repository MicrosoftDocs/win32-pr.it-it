---
description: Per consentire a un client di costruire un PrintTicket, il documento PrintCapabilities deve fornire le proprietà delle istanze feature e option nella funzionalità.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Istanze di proprietà importanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409124"
---
# <a name="important-property-instances"></a>Istanze di proprietà importanti

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Per consentire a un client PrintCapabilities di costruire un PrintTicket ragionevole, il documento PrintCapabilities deve fornire determinate proprietà delle istanze di Feature e delle istanze Option all'interno di Feature. Un modulo di interfaccia utente generica richiede tali informazioni per costruire un'interfaccia utente. A sua volta, è necessario che le parole chiave dello schema di stampa definiranno alcune istanze di Proprietà che vengono visualizzate come elementi figlio degli elementi Feature e Option.

Gli elementi della funzionalità possono contenere la proprietà seguente.



| Proprietà                  | Valori                                 | Scopo                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di selezione <br/> | PickOne<br/> PickMany<br/> | Specifica il numero di opzioni che è possibile selezionare per questa funzionalità in un determinato momento, una (PickOne) o più di una (PickMany). Il client può usare queste informazioni per costruire un PrintTicket. Queste informazioni influiscono sul comportamento dell'interfaccia utente e sulla convalida PrintTicket da parte del provider.<br/> |



 

Gli elementi Option possono contenere la proprietà seguente.



| Proprietà                   | Valori                           | Scopo                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IdentityOption <br/> | Vero<br/> Falso<br/> | La selezione della proprietà IdentityOption viene interpretata come "disabilita questa funzionalità". Un elemento Feature che contiene una proprietà SelectionType il cui valore è PickMany deve contenere anche un elemento Option con una proprietà IdentityOption. Il codice dell'interfaccia utente (o il client che costruisce un PrintTicket) deve deselezionare qualsiasi altra opzione se è selezionata la proprietà IdentityOption.<br/> |



 

Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.



| Proprietà              | Valori                          | Scopo                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayUI <br/> | Mostra<br/> Nascondi<br/> | Specifica se l'elemento padre deve essere visualizzato nell'interfaccia utente. Show indica che l'elemento deve essere visualizzato nell'interfaccia utente. Nascondi indica che l'elemento non deve essere visualizzato nell'interfaccia utente. Se questa proprietà non è definita per un elemento, l'interpretazione predefinita è Show, ovvero l'elemento viene visualizzato.<br/> |



 

Gli elementi Feature, Option e ParameterDef possono contenere la proprietà seguente.



| Proprietà                | valore             | Scopo                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName <br/> | Stringa<br/> | Specifica la stringa di visualizzazione per l'elemento padre, eseguendo l'override del nome visualizzato predefinito. Può essere usato dai provider PrintCapabilities per presentare un nome visualizzato localizzato e descrittivo. Il valore predefinito del nome visualizzato è l'attributo name per l'elemento padre. <br/> Nel caso degli elementi Option, se non viene specificato l'attributo name, la proprietà DisplayName deve essere presente.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




