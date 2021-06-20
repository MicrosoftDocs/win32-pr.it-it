---
title: Enumerazione dei membri in un gruppo
description: Informazioni sull'enumerazione dei membri in un Azure Active Directory gruppo. I membri di un gruppo vengono archiviati in un attributo multivalore denominato member.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerazione dei membri in un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407424"
---
# <a name="enumerating-members-in-a-group"></a>Enumerazione dei membri in un gruppo

I membri di un gruppo vengono archiviati in un attributo multivalore denominato **membro**. Per i gruppi con appartenenza da piccola a media, usare il metodo [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) per ottenere un puntatore a un oggetto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) che contiene l'elenco di tutti i membri. Usare quindi [**IADsMembers::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) per ottenere un oggetto enumeratore che è possibile usare per enumerare i membri.

Se l'appartenenza al gruppo prevista sarà di 1000 o più membri, usare ranging per recuperare gli utenti un intervallo alla volta. Per altre informazioni sull'uso di ranging per enumerare i membri, vedere [Enumerazione di gruppi che contengono molti membri.](enumerating-groups-that-contain-many-members.md)

 

 