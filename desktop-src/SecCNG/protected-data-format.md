---
description: I dati protetti vengono archiviati come BLOB con codifica ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato dati protetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131299"
---
# <a name="protected-data-format"></a>Formato dati protetto

I dati protetti vengono archiviati come BLOB con codifica ASN. 1. I dati vengono formattati come contenuti in busta CMS (certificate Message Syntax). La busta digitale contiene contenuto crittografato, informazioni sui destinatari contenenti una chiave di crittografia del contenuto crittografata (CEK) e un'intestazione che contiene informazioni sul contenuto, inclusa la stringa della regola descrittore di protezione non crittografata. Questa operazione viene illustrata nel diagramma seguente.

![dati busta protetti](images/protecteddatablob.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[Descrittori di protezione](protection-descriptors.md)
</dt> <dt>

[Provider di protezione](protection-providers.md)
</dt> </dl>

 

 



