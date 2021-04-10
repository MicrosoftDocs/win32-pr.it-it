---
title: File generati per un'interfaccia COM
description: Per le interfacce COM, il compilatore MIDL combina tutti i dati e le routine ausiliarie del client e del server oggetti in un singolo file proxy di interfaccia.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL Compiler MIDL, MIDL e COM
- MIDL COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963007"
---
# <a name="files-generated-for-a-com-interface"></a>File generati per un'interfaccia COM

Per le interfacce COM, il compilatore MIDL combina tutti i dati e le routine ausiliarie del client e del server oggetti in un singolo file proxy di interfaccia. Questo file include i punti di ingresso surrogati per client e server. Il compilatore MIDL genera inoltre un file di intestazione di interfaccia, un file UUID dell'interfaccia e un file di registrazione dell'interfaccia. Si utilizzeranno tutti questi file quando si crea una DLL proxy che contiene il codice per supportare l'utilizzo dell'interfaccia da parte delle applicazioni client e dei server oggetti. Si utilizzeranno anche il file di intestazione dell'interfaccia e il file UUID dell'interfaccia quando si crea il file eseguibile per un'applicazione client che utilizza l'interfaccia.

Negli argomenti seguenti vengono descritti i file generati per un'interfaccia COM personalizzata, che è possibile identificare includendo l' **\[** attributo [**Object**](object.md) **\]** nell'elenco di attributi di interfaccia del file IDL:

-   [File proxy di interfaccia](the-interface-proxy-file.md)
-   [File di intestazione](the-header-files.md)
-   [File UUID dell'interfaccia](the-interface-uuid-file.md)
-   [File di registrazione dell'interfaccia](the-interface-registration-file.md)

Per ulteriori informazioni, vedere il file di [configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md), la [**\_ configurazione di/app**](-app-config.md), il [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)e [la compilazione e la registrazione di una DLL proxy](../com/building-and-registering-a-proxy-dll.md).

 

 