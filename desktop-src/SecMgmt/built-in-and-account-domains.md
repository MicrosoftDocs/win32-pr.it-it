---
description: Vengono illustrati i domini predefiniti e di account nei sistemi basati su Windows.
ms.assetid: 306c258b-950e-4506-99e2-67a3714285ff
title: Domini predefiniti e account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d2d4bb18e1ac2ea33aaff008475a44515d9231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315359"
---
# <a name="built-in-and-account-domains"></a>Domini predefiniti e account

I domini in un sistema basato su Windows rientrano nelle due categorie seguenti:

-   [Computer che non sono controller di dominio](#computers-that-are-not-domain-controllers)
-   [Computer che sono controller di dominio](#computers-that-are-domain-controllers)

## <a name="computers-that-are-not-domain-controllers"></a>Computer che non sono controller di dominio

Il database di gestione degli account di sicurezza (SAM) si trova in ogni computer e gestisce gli account per il dominio predefinito e per il dominio dell'account.



| Dominio          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dominio predefinito | Questo dominio contiene gruppi locali predefiniti, ad esempio i gruppi Administrators e Users, che vengono stabiliti quando viene installato il sistema operativo. Il nome di questo dominio è una versione localizzata di BUILTin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Dominio account  | Il dominio dell'account può contenere utenti, gruppi e account di gruppo locali. L'account Administrator si trova in questo dominio. Gli account definiti nel dominio dell'account di una workstation o di un server membro sono limitati all'accesso alle risorse che si trovano nel computer fisico in cui risiede l'account. In un sistema che non fa parte di una rete e pertanto non ha un [dominio primario](primary-and-trusted-domains.md), il dominio dell'account viene usato per ospitare tutti gli account che forniscono l'accesso al computer. In un sistema che fa parte di una rete, il dominio dell'account del computer viene usato per ospitare gli account che non accedono alle risorse di rete. Gli account che richiedono l'accesso alla rete devono essere definiti nel dominio dell'account di un controller di dominio.<br/> Il nome di questo dominio viene assegnato al momento dell'installazione del sistema ed è determinato dal nome del computer. Se il nome del computer viene modificato, il nome di dominio dell'account non verrà aggiornato fino al riavvio del computer.<br/> |



 

## <a name="computers-that-are-domain-controllers"></a>Computer che sono controller di dominio

I controller di dominio non dispongono di domini di account predefiniti o. Inoltre, invece di un database SAM, questi sistemi usano il servizio directory Microsoft Active Directory per archiviare le informazioni di accesso all'account. Per ulteriori informazioni, vedere [Active Directory](/windows/desktop/AD/active-directory-domain-services).

 

