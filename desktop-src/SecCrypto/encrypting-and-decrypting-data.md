---
description: Quando un documento o un testo deve avere una privacy protetta da un singolo utente o quando il documento deve essere condiviso da un piccolo gruppo di persone che hanno accesso alla stessa password segreta, è possibile eseguire semplici operazioni di crittografia/decrittografia.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Crittografia e decrittografia di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968130"
---
# <a name="encrypting-and-decrypting-data"></a>Crittografia e decrittografia di dati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Quando un documento o un testo deve avere una privacy protetta da un singolo utente o quando il documento deve essere condiviso da un piccolo gruppo di persone che hanno accesso alla stessa password segreta, è possibile eseguire semplici operazioni di crittografia/decrittografia. CAPICOM non supporta il \# tipo di contenuto EncryptedData di PKCS 7, ma usa una struttura ASN non standard per EncryptedData. Pertanto, solo CAPICOM è in grado di decrittografare un oggetto capicot EncryptedData.

Le sezioni seguenti illustrano esempi per le attività di crittografia e decrittografia:

-   [Crittografia di un messaggio in CAPICOM](encrypting-a-message-in-capicom.md)
-   [Decrittografia di un messaggio in CAPICOM](decrypting-a-message-in-capicom.md)

 

 



