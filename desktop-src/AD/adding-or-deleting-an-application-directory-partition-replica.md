---
title: Aggiunta o eliminazione di una replica della partizione di directory applicativa
description: La prima replica di una partizione di directory applicativa viene creata sul controller di dominio associato al momento della creazione.
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- Aggiunta o eliminazione di un annuncio della replica della partizione di directory applicativa
- Directory dell'applicazione partizioni di Active Directory, aggiunta o eliminazione di una replica di partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c84b19e64f6abfc5e63d6e0e3d1b3a192da3e38
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117574"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>Aggiunta o eliminazione di una replica della partizione di directory applicativa

La prima replica di una partizione di directory applicativa viene creata sul controller di dominio associato al momento della creazione. È possibile creare repliche aggiuntive in qualsiasi controller di dominio della foresta, non necessariamente nello stesso dominio del controller di dominio iniziale. Una replica della partizione di directory applicativa può esistere solo in un controller di dominio che esegue Windows Server 2003 o versione successiva. Per ulteriori informazioni, vedere questo articolo di TechNet sulla [gestione delle partizioni](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10)).

**Per aggiungere una replica per una partizione di directory applicativa, seguire questa procedura.**

1.  Cercare nel contenitore partizioni un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con un valore di attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) uguale al nome distinto della partizione di directory applicativa.
2.  Eseguire l'associazione all'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con la delega abilitata. Questa operazione è necessaria perché l'oggetto **crossRef** può essere modificato solo nel titolare del ruolo FSMO Domain-Naming. Con la delega abilitata, il controller di dominio può contattare il titolare del ruolo FSMO Domain-Naming usando le stesse credenziali.
3.  Aggiungere il nome distinto dell'oggetto [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) per il controller di dominio che ospiterà la nuova replica all'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Quando il nuovo valore dell'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) viene replicato nel nuovo controller di dominio che ospita una replica della partizione di directory applicativa, verrà attivato KCC per replicare la partizione di directory applicativa nel controller di dominio di destinazione.

Per rimuovere una replica per una partizione di directory applicativa, eseguire gli stessi passaggi descritti in precedenza per individuare l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta la partizione di directory applicativa e rimuovere il valore che corrisponde al controller di dominio dall'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) dell'oggetto **crossRef** .

Quando il nuovo valore dell'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) viene replicato nel controller di dominio che non ospita più una replica della partizione di directory applicativa, verrà attivato KCC per rimuovere la replica della partizione di directory applicativa sul controller di dominio di destinazione.

Se un controller di dominio che ospita una replica della partizione di directory applicativa viene rimosso o abbassato di grado, il server Active Directory rimuoverà automaticamente il valore corrispondente al controller di dominio dall'attributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) di tutti gli oggetti [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

 

 