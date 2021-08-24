---
title: oggetti Internet-Aware
description: oggetti Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280141d4bc9cb1a6a6c685c4badde0b24609996683e73c74f69637440b39ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756151"
---
# <a name="internet-aware-objects"></a>oggetti Internet-Aware

Esistono alcune categorie identificate per coprire le interfacce di persistenza. Questi sono stati identificati come risultato della definizione del funzionamento dei controlli in Internet. Un contenitore che non supporta l'intera gamma di interfacce di persistenza deve garantire che non ospita un controllo che richiede una combinazione di interfacce non supportate.

Le tabelle seguenti descrivono il significato per le varie categorie sia come categorie implementate che come categorie obbligatorie.



| Categorie obbligatorie                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PersistsToStreamInit, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Ognuna di queste categorie si escludono a vicenda e viene usata solo quando un oggetto supporta un solo meccanismo di persistenza(da qui l'esclusione reciproca). I contenitori che non supportano il meccanismo di persistenza descritto da una di queste categorie devono impedire a se stessi di creare oggetti di classi così contrassegnati.<br/> |
| CATID \_ RequiresDataPathHost<br/>                                                                                                                                                             | L'oggetto richiede la possibilità di salvare i dati in uno o più percorsi e richiede il coinvolgimento del contenitore, quindi richiede il supporto del contenitore [**per IBindHost.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85))<br/>                                                                                                                                  |



 



| Categorie implementate                                                                                                                                                                            | Descrizione                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PersistsToStreamInit, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATID \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | L'oggetto supporta il meccanismo IPersist \* corrispondente per la categoria.<br/> |



 

La tabella seguente fornisce i CATID esatti assegnati a ogni categoria:



| Category                                | Catid                                           |
|-----------------------------------------|-------------------------------------------------|
| CATID \_ RequiresDataPathHost<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMoniker <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStorage <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStreamInit <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStream <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMemory <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToFile <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToPropertyBag<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

