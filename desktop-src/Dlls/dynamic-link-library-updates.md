---
description: A volte è necessario sostituire una DLL con una versione più recente.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Aggiornamenti della libreria di Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f76103ddebc723466fb7e32a216c0c039691d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049653"
---
# <a name="dynamic-link-library-updates"></a>Aggiornamenti della libreria di Dynamic-Link

A volte è necessario sostituire una DLL con una versione più recente. Prima di sostituire una DLL, eseguire un controllo della versione per assicurarsi di sostituire una versione precedente con una versione più recente. È possibile sostituire una DLL in uso. Il metodo utilizzato per sostituire le dll in uso dipende dal sistema operativo in uso. In Windows XP e versioni successive, le applicazioni devono utilizzare [applicazioni isolate e assembly affiancati](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Non è necessario riavviare il computer se si eseguono i passaggi seguenti:

1.  Utilizzare la funzione [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) per rinominare la dll che viene sostituita. Non specificare la \_ copia MOVEFILE \_ consentita e assicurarsi che il file rinominato si trovi nello stesso volume che contiene il file originale. È anche possibile rinominare semplicemente il file nella stessa directory assegnando un'estensione diversa.
2.  Copiare la nuova DLL nella directory che contiene la DLL rinominata. Tutte le applicazioni utilizzeranno ora la nuova DLL.
3.  Usare [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) con \_ ritardo MOVEFILE \_ fino \_ al riavvio per eliminare la dll rinominata.

Prima di eseguire questa sostituzione, le applicazioni utilizzeranno la DLL originale fino a quando non verrà scaricata. Dopo aver effettuato la sostituzione, le applicazioni utilizzeranno la nuova DLL. Quando si scrive una DLL, è necessario assicurarsi che sia preparata per questa situazione, soprattutto se la DLL mantiene le informazioni sullo stato globale o comunica con altri servizi. Se la DLL non è preparata per una modifica nelle informazioni sullo stato globale o nei protocolli di comunicazione, l'aggiornamento della DLL richiede il riavvio del computer per assicurarsi che tutte le applicazioni utilizzino la stessa versione della DLL.

 

 
