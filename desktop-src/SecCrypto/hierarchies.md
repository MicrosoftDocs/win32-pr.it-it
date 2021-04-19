---
description: Servizi certificati supporta le gerarchie di autorità di certificazione (CA).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Gerarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316152"
---
# <a name="hierarchies"></a>Gerarchie

Servizi certificati supporta le gerarchie di [*autorità di certificazione*](../secgloss/c-gly.md) (CA). Una [*gerarchia di CA*](../secgloss/c-gly.md) è costituita da una CA di primo livello (denominata CA radice) con una o più CA subordinate che sono state rilasciate certificati dalla CA radice. Un possibile scenario della gerarchia CA si trova in un'organizzazione con una CA radice, che è stata usata per emettere certificati per diverse CA subordinate. Le CA subordinate possono quindi rilasciare i certificati dell'entità finale, ad esempio i certificati emessi a un utente. Il certificato dell'utente conterrà un percorso di trust per la gerarchia di CA, in questo caso, incluso il certificato per la CA subordinata emittente e la CA radice.

 

 
