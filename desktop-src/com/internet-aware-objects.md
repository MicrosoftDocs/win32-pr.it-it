---
title: Oggetti Internet-Aware
description: Oggetti Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963503"
---
# <a name="internet-aware-objects"></a>Oggetti Internet-Aware

Sono state identificate determinate categorie per coprire le interfacce persistenza. Questi sono stati identificati come risultato della definizione del modo in cui i controlli funzionano in Internet. Un contenitore che non supporta l'intera gamma di interfacce persistenza deve garantire che non venga ospitato un controllo che richiede una combinazione di interfacce che non supporta.

Le tabelle seguenti descrivono il significato per le varie categorie sia come implementate che come categorie obbligatorie.



| Categorie obbligatorie                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Ognuna di queste categorie si escludono a vicenda e viene usata solo quando un oggetto supporta solo un meccanismo di persistenza, da cui l'esclusione reciproca. I contenitori che non supportano il meccanismo di persistenza descritto da una di queste categorie devono impedire la creazione di oggetti di classi così contrassegnati.<br/> |
| RequiresDataPathHost CATId \_<br/>                                                                                                                                                             | L'oggetto richiede la possibilità di salvare i dati in uno o più percorsi e richiede il coinvolgimento del contenitore e pertanto richiede il supporto dei contenitori per [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).<br/>                                                                                                                                  |



 



| Categorie implementate                                                                                                                                                                            | Descrizione                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | L'oggetto supporta il meccanismo IPersist corrispondente \* per la categoria.<br/> |



 

La tabella seguente fornisce il CATID esatto assegnato a ogni categoria:



| Category                                | CATID                                           |
|-----------------------------------------|-------------------------------------------------|
| RequiresDataPathHost CATId \_<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToMoniker CATId \_ <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStorage CATId \_ <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStreamInit CATId \_ <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStream CATId \_ <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToMemory CATId \_ <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToFile CATId \_ <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToPropertyBag CATId \_<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

