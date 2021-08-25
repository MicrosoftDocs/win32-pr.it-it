---
description: Come ottenere più spazio libero su disco dopo il superamento del limite di quota.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Amministrazione a livello utente delle quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214f1fb915d199ff6db3a6b3084c5c0f6f2df5c9737290fbdaa0e977a1163f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914361"
---
# <a name="user-level-administration-of-disk-quotas"></a>Amministrazione a livello utente delle quote disco

Le quote disco sono trasparenti per l'utente. Quando un utente chiede quanto spazio è disponibile su un disco, il sistema segnala solo la quota disponibile disponibile per l'utente. Se l'utente supera questa soglia, il sistema restituisce l'errore **ERROR \_ DISK \_ FULL,** esattamente come per indicare che il disco era pieno.

Per ottenere più spazio libero su disco dopo il superamento del limite di quota, l'utente deve eseguire una delle operazioni seguenti:

-   Eliminare alcuni file.
-   Chiedere a un altro utente di richiedere la proprietà di alcuni file.
-   Fare in modo che l'amministratore aumenti il limite di quota.

I programmi che devono recuperare la quantità effettiva di spazio libero su disco possono chiamare la [**funzione GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) ed esaminare il *parametro TotalNumberOfFreeBytes.*

 

 



