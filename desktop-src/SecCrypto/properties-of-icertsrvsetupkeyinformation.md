---
description: Le proprietà seguenti sono definite dall'interfaccia ICertSrvSetupKeyInformation.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Proprietà di ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882098"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a>Proprietà di ICertSrvSetupKeyInformation

Le proprietà seguenti sono definite dall'interfaccia [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .



| Proprietà                                                                           | Descrizione                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContainerName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | Ottiene o imposta il nome utilizzato dal [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per generare, archiviare o accedere alla chiave.                                                                       |
| [**Existing**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | Ottiene o imposta un valore che indica se la chiave privata esiste già.                                                                                                                                                                                                                       |
| [**ExistingCACertificate**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | Ottiene o imposta il valore binario che è stato codificato tramite [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) e che è il valore binario del certificato della CA che corrisponde a una chiave esistente. |
| [**HashAlgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | Ottiene o imposta il nome dell'algoritmo hash utilizzato per firmare o verificare il certificato della CA per la chiave.                                                                                                                                                                                                |
| [**Lunghezza**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | Ottiene o imposta il livello di attendibilità della chiave per uno dei valori supportati dal CSP.                                                                                                                                                                                                                   |
| [**ProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | Ottiene o imposta il nome del CSP utilizzato per generare o archiviare la chiave privata.                                                                                                                                                                                                               |



 

 

 
