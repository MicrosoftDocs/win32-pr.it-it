---
description: Quando si installa un assembly in un percorso isolato per un'applicazione specifica, l'applicazione deve essere specificata nella colonna Applicazione file \_ della tabella MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installazione e rimozione di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0117c29a9bcc49a549529a6e05f1124236cb845d9b7792d7bcbda143fd6d08e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043431"
---
# <a name="installing-and-removing-assemblies"></a>Installazione e rimozione di assembly

Quando si installa un assembly in un percorso isolato per un'applicazione specifica, l'applicazione deve essere specificata nella colonna Applicazione file \_ della [tabella MsiAssembly](msiassembly-table.md). Questo campo è una chiave nella [tabella File](file-table.md). Il programma di installazione usa la struttura di directory specificata nella tabella [Directory](directory-table.md) per installare l'assembly nella stessa directory del componente che contiene questo file.

Quando si installa un assembly nella Global Assembly Cache, il valore nella colonna Applicazione file della tabella \_ [MsiAssembly](msiassembly-table.md) deve essere Null.

Le sezioni seguenti descrivono l'installazione di assembly Win32 e Common Language Runtime:

-   [Installazione di assembly Win32](installation-of-win32-assemblies.md)
-   [Installazione di assembly Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



