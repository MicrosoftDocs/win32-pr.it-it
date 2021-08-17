---
description: Servizi certificati supporta le gerarchie dell'autorità di certificazione (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Gerarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240f2f2fc2920db1a67adb18281ad5c1d67fabdb2996ae3aae8342f96b1810c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006299"
---
# <a name="hierarchies"></a>Gerarchie

Servizi certificati supporta le [*gerarchie dell'autorità*](../secgloss/c-gly.md) di certificazione (CA). Una [*gerarchia di*](../secgloss/c-gly.md) CA è costituita da una CA di primo livello (denominata CA radice) con una o più CA subordinate che sono state rilasciate certificati dalla CA radice. Un possibile scenario di gerarchia di CA sarebbe in un'organizzazione con una CA radice, usata per rilasciare certificati a diverse CA subordinate. Le AUTORITÀ di certificazione subordinate possono quindi rilasciare certificati di entità finali, ad esempio certificati rilasciati a un utente. Il certificato dell'utente conterrà un percorso di attendibilità per la gerarchia della CA, in questo caso, incluso il certificato sia per la CA subordinata emittente che per la CA radice.

 

 
