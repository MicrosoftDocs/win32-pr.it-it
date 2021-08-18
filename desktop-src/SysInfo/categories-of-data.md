---
description: "Prima di inserire i dati nel Registro di sistema, un'applicazione deve dividere i dati in due categorie: dati specifici del computer e dati specifici dell'utente."
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorie di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4bf4abb7af2abf723aa42f3426c58230083d8e575dda176b8eeda0daecb36d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885852"
---
# <a name="categories-of-data"></a>Categorie di dati

Prima di inserire i dati nel Registro di sistema, un'applicazione deve dividere i dati in due categorie: dati specifici del computer e dati specifici dell'utente. Grazie a questa distinzione, un'applicazione può supportare più utenti e tuttavia individuare dati specifici dell'utente in una rete e usarli in posizioni diverse, consentendo i dati del profilo utente indipendenti dalla posizione. Un profilo utente è un set di dati di configurazione salvati per ogni utente.

Quando l'applicazione viene installata, deve registrare i dati specifici del computer nella **chiave HKEY \_ LOCAL \_ MACHINE.** In particolare, deve creare chiavi per il nome della società, il nome del prodotto e il numero di versione, come illustrato nell'esempio seguente:

**HKEY \_ LOCAL \_ MACHINE \\ \\ Software**_MyCompany \\ MyProduct \\ 1.0_

Se l'applicazione supporta COM, è necessario registrare i dati in **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**.

Un'applicazione deve registrare dati specifici dell'utente nella **chiave HKEY \_ CURRENT \_ USER,** come illustrato nell'esempio seguente:

**HKEY \_ CURRENT \_ USER \\ \\ Software**_MyCompany \\ MyProduct \\ 1.0_

 

 



