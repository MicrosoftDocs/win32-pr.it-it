---
title: Foreste
description: Una foresta è un set di uno o più alberi di dominio che non formano uno spazio dei nomi contiguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- foreste Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956326"
---
# <a name="forests"></a>Foreste

Una [*foresta*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) è un set di uno o più alberi di dominio che non formano uno spazio dei nomi contiguo. Tutti gli alberi di una foresta condividono uno schema comune, una configurazione e un catalogo globale. Tutti gli alberi in una determinata foresta si considerano attendibili in base alle relazioni di trust Kerberos gerarchiche. A differenza degli alberi, una foresta non richiede un nome distinto. Una foresta esiste come un set di oggetti di riferimento incrociato e relazioni di trust Kerberos riconosciute dagli alberi dei membri. Gli alberi di una foresta formano una gerarchia ai fini del trust Kerberos. il nome dell'albero alla radice dell'albero di trust fa riferimento a una foresta specificata.

Nella figura seguente è illustrata una foresta di spazi dei nomi non contigui.

![foresta di spazi dei nomi non contigui](images/forests.png)

 

 