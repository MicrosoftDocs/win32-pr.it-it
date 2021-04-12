---
description: Quando si installa un assembly in un percorso isolato per un'applicazione specifica, è necessario specificare l'applicazione nella \_ colonna file Application della tabella MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installazione e rimozione di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234043"
---
# <a name="installing-and-removing-assemblies"></a>Installazione e rimozione di assembly

Quando si installa un assembly in un percorso isolato per un'applicazione specifica, è necessario specificare l'applicazione nella \_ colonna file Application della [tabella MsiAssembly](msiassembly-table.md). Questo campo è una chiave nella [tabella file](file-table.md). Il programma di installazione utilizza la struttura di directory specificata nella [tabella di directory](directory-table.md) per installare l'assembly nella stessa directory del componente che contiene il file.

Quando si installa un assembly nella Global Assembly Cache, il valore nella \_ colonna applicazione file della [tabella MsiAssembly](msiassembly-table.md) deve essere null.

Le sezioni seguenti descrivono l'installazione di assembly Win32 e Common Language Runtime:

-   [Installazione degli assembly Win32](installation-of-win32-assemblies.md)
-   [Installazione degli assembly di Common Language Runtime](installation-of-common-language-runtime-assemblies.md)

 

 



