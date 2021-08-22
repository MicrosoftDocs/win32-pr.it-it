---
description: I dati protetti vengono archiviati come BLOB con codifica ASN.1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato dei dati protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b4985fee02b5c40b9ad51a6645c4e0d9894a358a871c2067e44dd5f90da26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907408"
---
# <a name="protected-data-format"></a>Formato dei dati protetti

I dati protetti vengono archiviati come BLOB con codifica ASN.1. I dati vengono formattati come contenuto in busta CMS (certificate message syntax). La busta digitale contiene contenuto crittografato, informazioni sul destinatario che contiene una chiave CEK (Content Encryption Key) crittografata e un'intestazione che contiene informazioni sul contenuto, inclusa la stringa della regola del descrittore di protezione non crittografata. Come illustrato nel diagramma seguente.

![dati in busta protetta](images/protecteddatablob.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Descrittori di protezione](protection-descriptors.md)
</dt> <dt>

[Provider di protezione](protection-providers.md)
</dt> </dl>

 

 



