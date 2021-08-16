---
description: Gli assembly side-by-side vengono usati con i tipi di file manifesto e di configurazione seguenti. Manifesti e configurazioni sono file XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: "  File manifest"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87636a8a4e5398cf9bb274d5ea8b9e7620104989322a20138a162ca45d9caf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142064"
---
# <a name="manifest-files-reference"></a>  File manifest

Gli assembly side-by-side vengono usati con i tipi di file manifesto e di configurazione seguenti. Manifesti e configurazioni sono file XML.



| manifesto                                                               | Descrizione                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manifesti dell'assembly](assembly-manifests.md)                           | Descrive i nomi, le versioni, le risorse e le dipendenze degli assembly side-by-side.                                                                                                               |
| [Manifesti dell'applicazione](application-manifests.md)                     | Descrive i nomi e le versioni degli assembly side-by-side condivisi a cui l'applicazione deve eseguire l'associazione in fase di esecuzione e può anche contenere metadati per assembly side-by-side privati usati dall'applicazione. |
| [File di configurazione dell'applicazione](application-configuration-files.md) | Reindirizza le versioni degli assembly delle dipendenze dell'assembly usando [la configurazione per applicazione.](per-application-configuration.md)                                                                            |
| [Publisher File di configurazione](publisher-configuration-files.md)     | Reindirizza le versioni degli assembly delle dipendenze dell'assembly in base all'assembly usando una configurazione [dell'editore.](publisher-configuration.md)                                                              |



 

Per un elenco dello schema del file manifesto, vedere [Schema del file manifesto.](manifest-file-schema.md)

Per un elenco dello schema del file di configurazione dell'applicazione, vedere [Schema del file di configurazione dell'applicazione.](application-configuration-file-schema.md)

Per un elenco dello schema del file di configurazione del server di pubblicazione, [Publisher schema del file di configurazione](publisher-configuration-file-schema.md).

Altre tecnologie estendono il formato usato dai Windows di controllo delle versioni e di configurazione. Gli sviluppatori devono fare riferimento alla documentazione specifica per la tecnologia usata per informazioni sul formato del manifesto. Esempio:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [Controllo dell'account utente](/previous-versions/bb756929(v=msdn.10))

 

 
