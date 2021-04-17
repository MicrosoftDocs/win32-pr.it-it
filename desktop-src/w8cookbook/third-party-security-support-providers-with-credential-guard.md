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
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473139"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Provider di supporto per la sicurezza di terze parti con Credential Guard

Credential Guard non permette agli SSP di terze parti di richiedere hash delle password alla LSA. Tuttavia, gli SSP e I punti di accesso continuano a ricevere notifiche relative alla password quando un utente effettua l'accesso e/o cambia la propria password. Qualsiasi uso di API non documentate all'interno di SSP e punti di accesso personalizzati non è supportato.

Poiché la complessità e l'estensione delle funzionalità di protezione fornite da Credential Guard sono maggiori, le versioni successive di Windows 10 che eseguono Credential Guard potrebbero influire negativamente sugli scenari che funzionavano correttamente in passato. Ad esempio, Credential Guard può bloccare l'uso di un particolare tipo di credenziale o un particolare componente per impedire al malware di sfruttare le vulnerabilità. Di conseguenza, consigliamo che gli scenari necessari per le operazioni in un'organizzazione vengano testati prima di aggiornare un dispositivo che esegue Credential Guard.

Per la descrizione completa e le mitigazioni consigliate, fare riferimento a [questo articolo](/windows/security/identity-protection/credential-guard/credential-guard) .

 

 