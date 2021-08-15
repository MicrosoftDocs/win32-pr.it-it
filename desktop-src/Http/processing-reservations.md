---
title: Elaborazione delle prenotazioni
description: Le prenotazioni per parti dello spazio dei nomi URL vengono effettuate dall'amministratore di sistema e inserite nell'archivio prenotazioni permanente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f0e38f5994687bfe26d1334300c0aa7fbbd3f8096abcf60e6c523e7d030a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393763"
---
# <a name="processing-reservations"></a>Elaborazione delle prenotazioni

Le prenotazioni per parti dello spazio dei nomi URL vengono effettuate dall'amministratore di sistema e inserite nell'archivio prenotazioni permanente. La radice dello spazio dei nomi URL per HTTP è di proprietà dell'amministratore di sistema. Per tutti i valori di host e porta, le due prenotazioni seguenti vengono sempre presupposte nella radice dello spazio dei **nomi relativeUri.**



| Spazio dei nomi riservato                 | Riservato per              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | Amministratore localsystem |
| https:// <host> :<port>/ | Amministratore localsystem |



 

Queste prenotazioni implicite non possono essere rimosse. Tuttavia, è possibile delegare prenotazioni radice esplicite ad altri utenti. Prenotazioni come le seguenti creerebbe tali deleghe:



| Spazio dei nomi riservato        | Riservato per |
|---------------------------|--------------|
| `https://+:80/`           | UserA, UserC |
| `https://adatum.com:443/` | Utenteb        |



 

Se queste prenotazioni delegate vengono rimosse dall'amministratore di sistema, la proprietà dello spazio dei nomi ripristina la prenotazione implicita per i valori di host e porta corrispondenti.

 

 




