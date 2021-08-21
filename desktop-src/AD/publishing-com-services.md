---
title: Pubblicazione di servizi COM+
description: I servizi basati su COM forniscono un proxy di applicazione sotto forma di pacchetto Windows installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Pubblicazione di servizi COM+
- Active Directory, uso, pubblicazione di un servizio, servizi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91801bbfcbf8efa34ac0b79477dd9d859fc2ed34a8d40bcf0bd829f82cfd571a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025429"
---
# <a name="publishing-com-services"></a>Pubblicazione di servizi COM+

I servizi basati su COM forniscono un proxy di applicazione sotto forma di pacchetto Windows installer (MSI). Questo .msi file contiene il nome del server da usare e altri elementi necessari, ad esempio proxy/stub e librerie dei tipi necessarie per il marshalling. Lo snap-in Servizi componenti genera automaticamente questi proxy di applicazione per le applicazioni server COM+.

I proxy dell'applicazione vengono pubblicati in oggetti criteri in Active Directory usando l Criteri di gruppo Editor. Non è necessario alcun intervento speciale nell'applicazione client. L'account computer/utente nel computer client deve essere in un'unità organizzativa configurata per usare l'oggetto criteri in cui vengono pubblicati i proxy dell'applicazione. Il binder COM individua automaticamente il server tramite la directory quando il client stabilisce un'istanza degli oggetti interessati.

 

 




