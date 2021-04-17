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
# <a name="third-party-security-support-providers-with-credential-guard"></a><span data-ttu-id="0bb2b-103">Provider di supporto per la sicurezza di terze parti con Credential Guard</span><span class="sxs-lookup"><span data-stu-id="0bb2b-103">Third party Security Support Providers with Credential Guard</span></span>

<span data-ttu-id="0bb2b-104">Credential Guard non permette agli SSP di terze parti di richiedere hash delle password alla LSA.</span><span class="sxs-lookup"><span data-stu-id="0bb2b-104">Credential Guard does not allow 3rd party SSPs to ask for password hashes from LSA.</span></span> <span data-ttu-id="0bb2b-105">Tuttavia, gli SSP e I punti di accesso continuano a ricevere notifiche relative alla password quando un utente effettua l'accesso e/o cambia la propria password.</span><span class="sxs-lookup"><span data-stu-id="0bb2b-105">However, SSPs and APs still get notified of the password when a user logs on and/or changes their password.</span></span> <span data-ttu-id="0bb2b-106">Qualsiasi uso di API non documentate all'interno di SSP e punti di accesso personalizzati non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0bb2b-106">Any use of undocumented APIs within custom SSPs and APs are not supported.</span></span>

<span data-ttu-id="0bb2b-107">Poiché la complessità e l'estensione delle funzionalità di protezione fornite da Credential Guard sono maggiori, le versioni successive di Windows 10 che eseguono Credential Guard potrebbero influire negativamente sugli scenari che funzionavano correttamente in passato.</span><span class="sxs-lookup"><span data-stu-id="0bb2b-107">As the depth and breadth of protections provided by Credential Guard are increased, subsequent releases of Windows 10 with Credential Guard running may impact scenarios that were working in the past.</span></span> <span data-ttu-id="0bb2b-108">Ad esempio, Credential Guard può bloccare l'uso di un particolare tipo di credenziale o un particolare componente per impedire al malware di sfruttare le vulnerabilità.</span><span class="sxs-lookup"><span data-stu-id="0bb2b-108">For example, Credential Guard may block the use of a particular type of credential or a particular component to prevent malware from taking advantage of vulnerabilities.</span></span> <span data-ttu-id="0bb2b-109">Di conseguenza, consigliamo che gli scenari necessari per le operazioni in un'organizzazione vengano testati prima di aggiornare un dispositivo che esegue Credential Guard.</span><span class="sxs-lookup"><span data-stu-id="0bb2b-109">Therefore, we recommend that scenarios required for operations in an organization are tested before upgrading a device that has Credential Guard running.</span></span>

<span data-ttu-id="0bb2b-110">Per la descrizione completa e le mitigazioni consigliate, fare riferimento a [questo articolo](/windows/security/identity-protection/credential-guard/credential-guard) .</span><span class="sxs-lookup"><span data-stu-id="0bb2b-110">Please refer to [this article](/windows/security/identity-protection/credential-guard/credential-guard) for the full description and recommended mitigations.</span></span>

 

 