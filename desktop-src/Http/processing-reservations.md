---
title: Elaborazione delle prenotazioni
description: Le prenotazioni per parti dello spazio dei nomi URL vengono effettuate dall'amministratore di sistema e inserite nell'archivio prenotazioni permanente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399898"
---
# <a name="processing-reservations"></a>Elaborazione delle prenotazioni

Le prenotazioni per parti dello spazio dei nomi URL vengono effettuate dall'amministratore di sistema e inserite nell'archivio prenotazioni permanente. La radice dello spazio dei nomi URL per HTTP è di proprietà dell'amministratore di sistema. Per tutti i valori host e porta, le due prenotazioni seguenti vengono sempre presupposte nella radice dello spazio dei nomi **relativeUri** .



| Spazio dei nomi riservato                 | Riservato per              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | Amministratore LocalSystem |
| https:// <host> :<port>/ | Amministratore LocalSystem |



 

Non è possibile rimuovere queste prenotazioni implicite. Tuttavia, è possibile delegare le prenotazioni radice esplicite ad altri utenti. Le prenotazioni come quelle riportate di seguito creeranno tali deleghe:



| Spazio dei nomi riservato        | Riservato per |
|---------------------------|--------------|
| `https://+:80/`           | UtenteA, l'utente c |
| `https://adatum.com:443/` | UtenteB        |



 

Se queste prenotazioni delegate vengono rimosse dall'amministratore di sistema, la proprietà dello spazio dei nomi ripristina la prenotazione implicita per i valori host e porta corrispondenti.

 

 




