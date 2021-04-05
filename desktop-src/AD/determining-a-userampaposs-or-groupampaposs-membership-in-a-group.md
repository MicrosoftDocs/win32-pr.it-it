---
title: Determinazione dell'appartenenza di un utente o di un gruppo a un gruppo
description: Il metodo IADsGroup. IsValid può essere utilizzato per determinare se un oggetto è un membro di un gruppo.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Determinazione dell'appartenenza di un utente o di un gruppo a un gruppo AD
- gruppi di Active Directory, determinazione dell'appartenenza di un utente o di un gruppo a un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046523"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a>Determinazione dell'appartenenza di un utente o di un gruppo a un gruppo

Il metodo [**IADsGroup.**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) IsValid può essere utilizzato per determinare se un oggetto è un membro di un gruppo. Questo metodo restituisce **true** se l'oggetto specificato è un membro diretto del gruppo, ovvero la proprietà del membro del gruppo contiene l'oggetto specificato.

Un gruppo può contenere altri gruppi. Il metodo [**IADsGroup.**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) IsValid non verifica in modo ricorsivo i membri dei gruppi nella proprietà del membro, i gruppi all'interno di tali gruppi e così via. Per verificare in modo ricorsivo che un oggetto sia membro di un gruppo, enumerare i gruppi nella proprietà del membro, verificare i membri di tali gruppi per verificare se l'oggetto è un membro e se tali gruppi contengono altri gruppi, verificarne i membri e così via.

> [!Note]  
> Poiché i gruppi possono essere annidati, l'appartenenza al gruppo può avere cicli. Qualsiasi script che enumera in molti gruppi deve tenere un elenco interno di gruppi per terminare la ricorsione se è già stato visitato un gruppo.

 

 

 