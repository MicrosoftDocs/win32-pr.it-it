---
title: Funzionalità del modello di replica per Active Directory Domain Services
description: Il modello di replica usato in Active Directory Domain Services è detto coerenza generale multi-master con convergenza.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modello di replica
- Funzionalità del modello di replica di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd113ffe4182be47c9e8c84404fc748e417e78c866e41298ad19d8e7a0dec555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189532"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Funzionalità del modello di replica per Active Directory Domain Services

Il modello di replica usato in Active Directory Domain Services è denominato *coerenza loose multi-master con convergenza.* In questo modello la directory può avere molte repliche. Un sistema di replica propaga le modifiche apportate in una determinata replica a tutte le altre repliche. Non è garantito che le repliche siano coerenti tra loro in un determinato momento ("coerenza loose"), perché le modifiche possono essere applicate a qualsiasi replica in qualsiasi momento ("multi-master"). Se il sistema è autorizzato a raggiungere uno stato stabile, in cui non sono in esecuzione nuovi aggiornamenti e tutti gli aggiornamenti precedenti sono stati completamente replicati, è garantita la convergenza di tutte le repliche sullo stesso set di valori ("convergenza").

 

 




