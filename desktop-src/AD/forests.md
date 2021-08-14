---
title: Foreste
description: Una foresta è un set di uno o più alberi di dominio che non formano uno spazio dei nomi contiguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- foreste Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ccccbce1c660c3f1e185e75971aa71d613c2db012ce42979cfaee7cd9c2b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189206"
---
# <a name="forests"></a>Foreste

Una [*foresta*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) è un set di uno o più alberi di dominio che non formano uno spazio dei nomi contiguo. Tutti gli alberi in una foresta condividono uno schema, una configurazione e un catalogo globale comuni. Tutti gli alberi in una determinata foresta scambiano trust in base a relazioni di trust Kerberos gerarchiche transitive. A differenza degli alberi, una foresta non richiede un nome distinto. Una foresta esiste come set di oggetti tra riferimenti e relazioni di trust Kerberos riconosciute dagli alberi dei membri. Gli alberi in una foresta formano una gerarchia ai fini del trust Kerberos; Il nome dell'albero alla radice dell'albero di trust fa riferimento a una foresta specificata.

Nella figura seguente viene illustrata una foresta di spazi dei nomi non contigui.

![foresta di spazi dei nomi non contigui](images/forests.png)

 

 