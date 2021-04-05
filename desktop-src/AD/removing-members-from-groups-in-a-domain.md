---
title: Rimozione di membri da gruppi in un dominio
description: È possibile rimuovere utenti, gruppi o contatti dai gruppi.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- gruppi AD, rimozione di membri da gruppi in un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724447"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Rimozione di membri da gruppi in un dominio

È possibile rimuovere utenti, gruppi o contatti dai gruppi. L'attributo **member** dell'oggetto **Group** contiene tutti i membri diretti del gruppo.

Il modo più semplice per rimuovere un membro da un gruppo consiste nel chiamare il metodo [**IADsGroup. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) sull'interfaccia [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) dell'oggetto gruppo da cui si vogliono rimuovere i membri.

 

 