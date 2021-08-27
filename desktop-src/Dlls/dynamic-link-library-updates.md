---
description: A volte è necessario sostituire una DLL con una versione più recente.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Dynamic-Link della libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f294e16efac60da843c14d200aaa768d4fc78ce8a922cb0aa6958756a9903be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075541"
---
# <a name="dynamic-link-library-updates"></a>Dynamic-Link della libreria

A volte è necessario sostituire una DLL con una versione più recente. Prima di sostituire una DLL, eseguire un controllo della versione per assicurarsi di sostituire una versione precedente con una versione più recente. È possibile sostituire una DLL in uso. Il metodo utilizzato per sostituire le DLL in uso dipende dal sistema operativo in uso. In Windows XP e versioni successive, le applicazioni devono usare applicazioni isolate e assembly [side-by-side](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Non è necessario riavviare il computer se si esegue la procedura seguente:

1.  Usare la [**funzione MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) per rinominare la DLL da sostituire. Non specificare MOVEFILE COPY ALLOWED e assicurarsi che il file rinominato si trova nello stesso \_ volume che contiene il file \_ originale. È anche possibile rinominare semplicemente il file nella stessa directory con un'estensione diversa.
2.  Copiare la nuova DLL nella directory che contiene la DLL rinominata. Tutte le applicazioni useranno ora la nuova DLL.
3.  Usare [**MoveFileEx con**](/windows/desktop/api/winbase/nf-winbase-movefileexa) MOVEFILE \_ DELAY UNTIL REBOOT per eliminare la DLL \_ \_ rinominata.

Prima di eseguire questa sostituzione, le applicazioni useranno la DLL originale fino a quando non viene scaricata. Dopo aver apportato la sostituzione, le applicazioni useranno la nuova DLL. Quando si scrive una DLL, è necessario assicurarsi che sia preparata per questa situazione, soprattutto se la DLL mantiene informazioni sullo stato globale o comunica con altri servizi. Se la DLL non è preparata per una modifica nelle informazioni sullo stato globale o nei protocolli di comunicazione, l'aggiornamento della DLL richiederà il riavvio del computer per garantire che tutte le applicazioni utilizzino la stessa versione della DLL.

 

 
