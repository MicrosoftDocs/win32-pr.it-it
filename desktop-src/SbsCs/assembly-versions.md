---
description: Ogni assembly side-by-side deve avere una versione.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versioni degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e555035bf7b43f53d3a68f249005928867f453b78522f70dd45f3b5379c75e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885571"
---
# <a name="assembly-versions"></a>Versioni degli assembly

Ogni assembly side-by-side deve avere una versione. Ogni versione dell'assembly è associata a un numero di versione con quattro parti separate da punti: *major.minor.build.revision*. Se viene apportata una modifica a un assembly  che  lo rende incompatibile con le versioni esistenti, è necessario modificare le parti principali o secondarie del numero di versione. Un numero di versione che cambia solo nelle parti *della build* o *della revisione* indica che l'assembly è compatibile con le versioni precedenti.

La versione deve essere specificata negli **elementi assemblyIdentity** dei [manifesti](manifests.md). Usare il formato di versione in quattro parti: mmmmm.nnnnn.ooooo.ppppp. Ognuna delle parti separate da punti può essere compresa tra 0 e 65535 inclusi.

 

 



