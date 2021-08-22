---
title: Credential Guard e app di terze parti
description: Credential Guard non permette agli SSP di terze parti di richiedere hash delle password alla LSA.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5c773379e3b7fa52e2095d8db676dddc081e51806fd8f615d2b3a4b744fea95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706751"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Provider di supporto per la sicurezza di terze parti con Credential Guard

Credential Guard non permette agli SSP di terze parti di richiedere hash delle password alla LSA. Tuttavia, gli SSP e I punti di accesso continuano a ricevere notifiche relative alla password quando un utente effettua l'accesso e/o cambia la propria password. Qualsiasi uso di API non documentate all'interno di SSP e punti di accesso personalizzati non è supportato.

Poiché la complessità e l'estensione delle funzionalità di protezione fornite da Credential Guard sono maggiori, le versioni successive di Windows 10 che eseguono Credential Guard potrebbero influire negativamente sugli scenari che funzionavano correttamente in passato. Ad esempio, Credential Guard può bloccare l'uso di un particolare tipo di credenziale o di un particolare componente per impedire al malware di sfruttare le vulnerabilità. Di conseguenza, consigliamo che gli scenari necessari per le operazioni in un'organizzazione vengano testati prima di aggiornare un dispositivo che esegue Credential Guard.

Fare riferimento a [questo articolo per](/windows/security/identity-protection/credential-guard/credential-guard) la descrizione completa e le mitigazioni consigliate.

 

 