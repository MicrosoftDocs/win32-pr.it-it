---
description: Il materiale seguente è valido solo quando il digest viene usato come meccanismo SASL. Le crittografie e la crittografia non sono disponibili per l'autenticazione HTTP con Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226853"
---
# <a name="ciphers"></a>Ciphers

Il materiale seguente è valido solo quando il digest viene usato come meccanismo SASL. Le crittografie e la crittografia non sono disponibili per l'autenticazione HTTP con Microsoft Digest.

La direttiva di crittografia di una richiesta digest SASL contiene un elenco delle crittografie supportate da un server che richiede comunicazioni riservate. La direttiva di crittografia può essere inclusa solo se la direttiva qop è impostata su "auth-conf". Le crittografie riconosciute da Microsoft Digest sono elencate nella tabella seguente, in ordine dal più forte al più debole.



| Valore di crittografia | Descrizione                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RC4        | Crittografia RC4 con una chiave a 128 bit.                                                                                                                                                                                                                                                             |
| 3DES       | La crittografia [*triple des*](/windows/desktop/SecGloss/t-gly) in modalità [*CBC*](/windows/desktop/SecGloss/c-gly) con Ede con la stessa chiave per ogni fase E (modalità a due chiavi). La lunghezza totale della chiave è 112 bit. |
| "RC4-56"     | Crittografia RC4 con una chiave a 56 bit.                                                                                                                                                                                                                                                              |
| "RC4-40"     | Crittografia RC4 con una chiave a 40 bit.                                                                                                                                                                                                                                                              |
| des        | Crittografia DES ( [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) ) in modalità CBC ( [*Cipher Block Chaining*](/windows/desktop/SecGloss/c-gly) ) con una chiave a 56 bit. |



 

Quando un'applicazione server richiede la riservatezza (qop = "auth-conf") Microsoft Digest genererà una richiesta di verifica che offre al client tutte le crittografie installate nel server e supportate da digest. Il client digest selezionerà la crittografia più sicura disponibile. Per informazioni dettagliate su come specificare la riservatezza, vedere [generazione della richiesta digest](generating-the-digest-challenge.md).

 

 
