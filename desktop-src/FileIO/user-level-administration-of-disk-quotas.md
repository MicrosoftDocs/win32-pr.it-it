---
description: Come ottenere maggiore spazio libero su disco dopo il superamento della quota di quote.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Amministrazione a livello di utente di quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316761"
---
# <a name="user-level-administration-of-disk-quotas"></a>Amministrazione a livello di utente di quote disco

Le quote disco sono trasparenti per l'utente. Quando un utente chiede la quantità di spazio disponibile su un disco, il sistema segnala solo la quota disponibile disponibile per l'utente. Se l'utente supera questo limite, il sistema restituisce l' **errore \_ \_ completo del disco di errore** , come per indicare che il disco è pieno.

Per ottenere maggiore spazio su disco dopo il superamento della quota di quote, l'utente deve eseguire una delle operazioni seguenti:

-   Eliminare alcuni file.
-   Chiedere a un altro utente di ottenere la proprietà di alcuni file.
-   Chiedere all'amministratore di aumentare la quota di quote.

I programmi che devono recuperare la quantità effettiva di spazio libero su disco possono chiamare la funzione [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) ed esaminare il parametro *TotalNumberOfFreeBytes* .

 

 



