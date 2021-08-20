---
title: File generati per un'interfaccia COM
description: Per le interfacce COM, il compilatore MIDL combina tutti i dati e le routine ausiliarie del client e del server oggetti in un unico file proxy di interfaccia.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL compiler MIDL , MIDL and COM
- COM MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efed184c8fe241a0028b210a33f695bec197a4a6591e8837e0e2e0343ee4ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991339"
---
# <a name="files-generated-for-a-com-interface"></a>File generati per un'interfaccia COM

Per le interfacce COM, il compilatore MIDL combina tutti i dati e le routine ausiliarie del client e del server oggetti in un unico file proxy di interfaccia. Questo file include i punti di ingresso surrogati per client e server. Inoltre, il compilatore MIDL genera un file di intestazione dell'interfaccia, un file UUID di interfaccia e un file di registrazione dell'interfaccia. Tutti questi file verranno utilizzati durante la creazione di una DLL proxy contenente il codice per supportare l'uso dell'interfaccia da parte di applicazioni client e server oggetti. Si useranno anche il file di intestazione dell'interfaccia e il file UUID dell'interfaccia durante la creazione del file eseguibile per un'applicazione client che usa l'interfaccia .

Gli argomenti seguenti descrivono ognuno dei file generati per un'interfaccia COM personalizzata, identificata includendo l'attributo object nell'elenco degli attributi dell'interfaccia **\[** [](object.md) **\]** del file IDL:

-   [File del proxy di interfaccia](the-interface-proxy-file.md)
-   [File di intestazione](the-header-files.md)
-   [File UUID dell'interfaccia](the-interface-uuid-file.md)
-   [File di registrazione dell'interfaccia](the-interface-registration-file.md)

Per altre informazioni, vedere File di configurazione [dell'applicazione (ACF),](application-configuration-file-acf-.md) [**/app \_ config**](-app-config.md), File di definizione dell'interfaccia [(IDL)](interface-definition-idl-file.md)e Compilazione e registrazione [di una DLL proxy.](../com/building-and-registering-a-proxy-dll.md)

 

 