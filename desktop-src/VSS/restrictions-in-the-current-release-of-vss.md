---
description: 'Alcune funzionalità pianificate per la Windows Server 2003 di VSS non sono completamente supportate:'
ms.assetid: 10e05d0d-3fce-4f19-bf83-f72f52f4098e
title: Restrizioni in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7353b2d52a7222015f051e15ba07830b81d6aedda6323bca4378f459eb602ba8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124511"
---
# <a name="restrictions-in-windows-server-2003"></a>Restrizioni in Windows Server 2003

Alcune funzionalità pianificate per la Windows Server 2003 di VSS non sono completamente supportate:

-   Durante le operazioni di backup, più istanze di una determinata classe writer sono consentite solo se solo una di queste istanze ha uno stato di ripristino del writer (vedere [**VSS \_ WRITERRESTORE \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)) diversa da VSS \_ WRE \_ NEVER. Se questa condizione viene soddisfatta, tutte le istanze del writer parteciperanno completamente durante il backup, generando documenti di metadati del writer e partecipando alla gestione degli eventi.
-   Durante le operazioni di ripristino, solo un writer riceverà gli eventi di ripristino generati dal richiedente. Se più istanze di una classe writer hanno uno stato di ripristino del writer impostato su un valore diverso da VSS WRE NEVER, solo un'istanza \_ \_ riceverà gli eventi di ripristino. L'istanza che le riceverà è indeterminata.

 

 



