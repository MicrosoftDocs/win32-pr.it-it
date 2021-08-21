---
title: Rimozione di membri dai gruppi in un dominio
description: È possibile rimuovere utenti, gruppi o contatti dai gruppi.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- groups AD , rimozione dei membri dai gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282cf2938996059ad13fe74bc9818e984967d1c8f3a4dbfffae7b505cbe1b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025159"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Rimozione di membri dai gruppi in un dominio

È possibile rimuovere utenti, gruppi o contatti dai gruppi. **L'attributo** member **dell'oggetto group** contiene tutti i membri diretti del gruppo.

Il modo più semplice per rimuovere un membro da un gruppo è chiamare il metodo [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) [**nell'interfaccia IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) dell'oggetto gruppo da cui si vogliono rimuovere i membri.

 

 