---
description: Ogni assembly side-by-side deve avere una versione.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Versioni degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757316"
---
# <a name="assembly-versions"></a>Versioni degli assembly

Ogni assembly side-by-side deve avere una versione. Ogni versione dell'assembly è associata a un numero di versione con quattro parti separate da punti: *Major. minor. Build. Revision*. Se viene apportata una modifica a un assembly rendendola incompatibile con le versioni esistenti, è necessario modificare le parti *principali* o *secondarie* del numero di versione. Un numero di versione che viene modificato solo nelle parti di *compilazione* o *Revisione* indica che l'assembly è compatibile con le versioni precedenti.

La versione deve essere specificata negli elementi **assemblyIdentity** dei [manifesti](manifests.md). Usare il formato di versione in quattro parti: mmmm. NNNNN. ooooo. ppppp. Ognuna delle parti separate da punti può essere 0-65535 inclusi.

 

 



