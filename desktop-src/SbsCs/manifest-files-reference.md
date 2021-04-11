---
description: Gli assembly affiancati vengono utilizzati con i tipi di file manifesto e di configurazione seguenti. I manifesti e le configurazioni sono file XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: "  File manifest"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128819"
---
# <a name="manifest-files-reference"></a>  File manifest

Gli assembly affiancati vengono utilizzati con i tipi di file manifesto e di configurazione seguenti. I manifesti e le configurazioni sono file XML.



| manifesto                                                               | Descrizione                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manifesti dell'assembly](assembly-manifests.md)                           | Descrive i nomi, le versioni, le risorse e le dipendenze degli assembly degli assembly affiancati.                                                                                                               |
| [Manifesti dell'applicazione](application-manifests.md)                     | Vengono descritti i nomi e le versioni degli assembly affiancati condivisi a cui l'applicazione deve essere associata in fase di esecuzione e possono inoltre contenere metadati per gli assembly side-by-side privati utilizzati dall'applicazione. |
| [File di configurazione dell'applicazione](application-configuration-files.md) | Reindirizza le versioni degli assembly delle dipendenze degli assembly usando la [configurazione per ogni applicazione](per-application-configuration.md).                                                                            |
| [File di configurazione del server di pubblicazione](publisher-configuration-files.md)     | Reindirizza le versioni degli assembly delle dipendenze degli assembly per ogni assembly utilizzando una configurazione del [server di pubblicazione](publisher-configuration.md).                                                              |



 

Per un elenco dello schema del file manifesto, vedere [schema del file manifesto](manifest-file-schema.md).

Per un elenco dello schema del file di configurazione dell'applicazione, vedere [schema del file di configurazione dell'applicazione](application-configuration-file-schema.md).

Per un elenco dello schema del file di configurazione dell'editore, vedere [schema del file di configurazione del server di pubblicazione](publisher-configuration-file-schema.md).

Altre tecnologie estendono il formato utilizzato dai manifesti di configurazione e controllo delle versioni di Windows. Gli sviluppatori devono fare riferimento alla documentazione specifica per la tecnologia usata per informazioni sul formato del manifesto. Ad esempio:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [Controllo dell'account utente](/previous-versions/bb756929(v=msdn.10))

 

 
