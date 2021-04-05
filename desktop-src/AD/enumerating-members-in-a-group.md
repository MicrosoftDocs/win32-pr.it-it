---
title: Enumerazione dei membri in un gruppo
description: I membri di un gruppo vengono archiviati in un attributo multivalore denominato member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerazione dei membri in un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117562"
---
# <a name="enumerating-members-in-a-group"></a>Enumerazione dei membri in un gruppo

I membri di un gruppo vengono archiviati in un attributo multivalore denominato **member**. Per i gruppi con appartenenza di dimensioni medio-piccole, usare il metodo [**IADsGroup. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) per ottenere un puntatore a un oggetto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) che contiene l'elenco di tutti i membri. Usare quindi [**IADsMembers:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) per ottenere un oggetto enumeratore che può essere usato per enumerare i membri.

Se l'appartenenza al gruppo prevista sarà di 1000 o più membri, utilizzare la funzione che consente di recuperare gli utenti un intervallo alla volta. Per ulteriori informazioni sull'utilizzo di ranging per enumerare i membri, vedere [enumerazione dei gruppi che contengono molti membri](enumerating-groups-that-contain-many-members.md).

 

 