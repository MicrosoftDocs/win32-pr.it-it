---
description: Vengono illustrati i domini predefiniti e account nei Windows basati su computer.
ms.assetid: 306c258b-950e-4506-99e2-67a3714285ff
title: Domini predefiniti e account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc85b7bba215e501ec1693eb0dd44a4c7649d411b462cee2ef2ac8f1a818fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894997"
---
# <a name="built-in-and-account-domains"></a>Domini predefiniti e account

I domini in Windows sistema basato su Windows rientrano nelle due categorie seguenti:

-   [Computer che non sono controller di dominio](#computers-that-are-not-domain-controllers)
-   [Computer che sono controller di dominio](#computers-that-are-domain-controllers)

## <a name="computers-that-are-not-domain-controllers"></a>Computer che non sono controller di dominio

Il database di Gestione account di sicurezza (SAM) si trova in ogni computer e gestisce gli account per il dominio predefinito e il dominio dell'account.



| Dominio          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dominio predefinito | Questo dominio contiene gruppi locali predefiniti, ad esempio i gruppi Administrators e Users, che vengono stabiliti al momento dell'installazione del sistema operativo. Il nome di questo dominio è una versione localizzata di BUILTIN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Dominio account  | Il dominio dell'account può contenere account utente, gruppo e gruppo locale. L'account Amministratore si trova in questo dominio. Gli account definiti nel dominio dell'account di una workstation o di un server membro sono limitati all'accesso alle risorse presenti nel computer fisico in cui risiede l'account. In un sistema che non fa parte di una rete e pertanto non ha un dominio [primario,](primary-and-trusted-domains.md)il dominio dell'account viene usato per ospitare tutti gli account che forniscono l'accesso al computer. In un sistema che fa parte di una rete, il dominio dell'account del computer viene usato per ospitare gli account che non accedono alle risorse di rete. Gli account che richiedono l'accesso alla rete devono essere definiti nel dominio dell'account di un controller di dominio.<br/> Il nome di questo dominio viene assegnato al momento dell'installazione del sistema ed è determinato dal nome del computer. Se il nome del computer viene modificato, il nome di dominio dell'account non verrà aggiornato fino al riavvio del computer.<br/> |



 

## <a name="computers-that-are-domain-controllers"></a>Computer che sono controller di dominio

I controller di dominio non dispongono di domini di account o predefiniti. Inoltre, anziché un database SAM, questi sistemi usano il servizio directory Microsoft Active Directory per archiviare le informazioni di accesso all'account. Per altre informazioni, vedere [Active Directory](/windows/desktop/AD/active-directory-domain-services).

 

