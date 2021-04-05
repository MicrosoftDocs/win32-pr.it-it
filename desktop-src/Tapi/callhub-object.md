---
description: L'oggetto CallHub rappresenta una visualizzazione di terze parti di una chiamata a più parti.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Oggetto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967858"
---
# <a name="callhub-object"></a>Oggetto CallHub

L'oggetto CallHub rappresenta una visualizzazione di terze parti di una chiamata a più parti. Le interfacce e i metodi associati ottengono e impostano informazioni relative all'hub, ad esempio se è attivo. Utilizzando l'oggetto CallHub, un utente con la sicurezza necessaria può individuare e potenzialmente controllare altri partecipanti in una chiamata.

Un oggetto CallHub non può essere creato direttamente da un'applicazione. Un oggetto CallHub viene creato indirettamente quando viene ricevuta una chiamata in ingresso tramite TAPI 3.

TAPI 3 si basa sui provider di servizi TAPI per fornire le informazioni necessarie sulle chiamate da implementare utilizzando l'oggetto CallHub. Poiché non tutti i provider di servizi forniscono queste informazioni e non tutti i componenti hardware supportano il rilevamento dell'hub delle chiamate, le informazioni disponibili sugli altri utenti della connessione possono essere limitate o inesistenti.

L'esempio di codice per la [creazione di una conferenza semplice](create-a-simple-conference.md) illustra l'uso di un oggetto CallHub.

Per un elenco di tutte le interfacce associate all'oggetto CallHub, vedere [interfacce oggetto CallHub](callhub-object-interfaces.md) .

 

 



