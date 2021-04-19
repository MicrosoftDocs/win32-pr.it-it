---
description: "Prima di inserire i dati nel registro di sistema, un'applicazione deve suddividere i dati in due categorie: dati specifici del computer e dati specifici dell'utente."
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorie di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319906"
---
# <a name="categories-of-data"></a>Categorie di dati

Prima di inserire i dati nel registro di sistema, un'applicazione deve suddividere i dati in due categorie: dati specifici del computer e dati specifici dell'utente. Con questa distinzione, un'applicazione può supportare più utenti e individuare i dati specifici dell'utente in una rete e usarli in posizioni diverse, permettendo dati di profilo utente indipendenti dalla posizione. Un profilo utente è un set di dati di configurazione salvati per ogni utente.

Quando l'applicazione viene installata, deve registrare i dati specifici del computer sotto la chiave del computer **\_ \_ locale HKEY** . In particolare, deve creare chiavi per il nome della società, il nome del prodotto e il numero di versione, come illustrato nell'esempio seguente:

**HKEY \_ \_Computer locale \\ software \\**_MyCompany MyCompany \\ \\ 1,0_

Se l'applicazione supporta COM, deve registrare i dati nelle **\_ \_ \\ \\ classi del software del computer locale HKEY**.

Un'applicazione deve registrare i dati specifici dell'utente con la chiave **\_ \_ utente corrente di HKEY** , come illustrato nell'esempio seguente:

**HKEY \_ \_ \\ Software \\ utente corrente**_produttore MyCompany \\ \\ 1,0_

 

 



