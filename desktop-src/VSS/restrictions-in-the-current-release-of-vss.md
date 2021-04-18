---
description: 'Alcune funzionalità pianificate per la versione 2003 di VSS di Windows Server non sono completamente supportate:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Limitazioni in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198e4ce79da4665bf712a64a466691041d452d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310673"
---
# <a name="restrictions-in-windows-server-2003"></a>Limitazioni in Windows Server 2003

Alcune funzionalità pianificate per la versione 2003 di VSS di Windows Server non sono completamente supportate:

-   Durante le operazioni di backup, sono consentite più istanze di una determinata classe Writer solo se solo una di queste istanze ha uno stato di ripristino del writer (vedere l' [**\_ \_ enumerazione VSS WRITERRESTORE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) diversa da VSS \_ WRE \_ Never. Se questa condizione viene soddisfatta, tutte le istanze del writer parteciperanno completamente durante il backup, generando documenti di metadati del writer e partecipando alla gestione degli eventi.
-   Durante le operazioni di ripristino, un solo Writer riceverà gli eventi di ripristino generati dal richiedente. Se più istanze di una classe Writer hanno uno stato di ripristino del writer impostato su un valore diverso da VSS \_ WRE \_ mai, solo un'istanza riceverà gli eventi di ripristino. L'istanza che li riceverà è indeterminata.

 

 



