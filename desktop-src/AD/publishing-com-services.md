---
title: Pubblicazione di servizi COM+
description: I servizi basati su COM forniscono un proxy di applicazione sotto forma di pacchetto di Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Pubblicazione di servizi COM+
- Active Directory, utilizzo, pubblicazione di un servizio, servizi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044100"
---
# <a name="publishing-com-services"></a>Pubblicazione di servizi COM+

I servizi basati su COM forniscono un proxy di applicazione sotto forma di pacchetto di Windows Installer (MSI). Il file con estensione msi contiene il nome del server da utilizzare e altri elementi necessari, ad esempio proxy/stub e librerie dei tipi necessari per il marshalling. Lo snap-in Servizi componenti genera automaticamente questi proxy di applicazione per le applicazioni server COM+.

I proxy dell'applicazione vengono pubblicati in oggetti criteri in Active Directory usando l'editor di Criteri di gruppo. Nell'applicazione client non è richiesto alcun intervento specifico. L'account computer/utente nel computer client deve trovarsi in un'unità organizzativa configurata per l'utilizzo dell'oggetto criterio in cui vengono pubblicati i proxy dell'applicazione. Il Binder COM individua automaticamente il server per mezzo della directory quando il client stabilisce un'istanza degli oggetti interessati.

 

 




