---
title: Utenti in Active Directory Domain Services
description: Active Directory Domain Services include un servizio directory che archivia i dati di dominio, utente, gruppo utenti e sicurezza.
ms.assetid: 7630fde1-14c0-4518-bb77-813f6913503e
ms.tgt_platform: multiple
keywords:
- Utenti in Active Directory Domain Services Active Directory
- utenti, servizi di dominio Active Directory
- Servizi di dominio Active Directory, utenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10ad85f359cab6baf891df03f368f3e7da5974f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046479"
---
# <a name="users-in-active-directory-domain-services"></a>Utenti in Active Directory Domain Services

Active Directory Domain Services include un servizio directory che archivia i dati di dominio, utente, gruppo utenti e sicurezza.

In Windows NT 4,0 e versioni precedenti, è possibile usare funzioni come [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd), [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum), [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel)e così via, per gestire utenti, gruppi di utenti e altri elementi di rete. In Windows 2000 e versioni successive di Windows, ADSI fornisce un accesso uniforme e sicuro a questi elementi e alle relative proprietà. Tenere presente che ADSI fornisce un provider Windows NT 4,0 che consente di utilizzare ADSI per gestire utenti, gruppi di utenti e computer nei sistemi Windows NT 4,0. Sono inoltre disponibili provider per Windows Server 2008 Enterprise (installazione dei componenti di base del server), Microsoft Exchange 5,5, Microsoft Internet Information Server (IIS), Novell NetWare Directory Services (NDS) e Novell NetWare 3. Ovvero un singolo set di metodi standardizzati per la gestione di utenti e gruppi di utenti per Windows NT, NDS e NetWare 3.

Inoltre, Windows 2000 è una directory multimaster. Ovvero le modifiche apportate a utenti, gruppi di utenti e altri dati archiviati nella directory possono essere eseguite in qualsiasi controller di dominio. In Windows 2000 non è necessario trovare il controller di dominio primario (PDC) e apportare modifiche a utenti e gruppi di utenti nel PDC.

Windows 2000 introduce inoltre un nuovo spazio dei nomi gerarchico all'interno di un dominio denominato unità organizzativa (OU). Un'unità organizzativa può contenere computer, utenti, gruppi di utenti e altri oggetti di rete. In genere, un'unità organizzativa viene utilizzata per raggruppare gli elementi a scopo amministrativo, ad esempio la delega dei diritti amministrativi e l'assegnazione di criteri al gruppo come una singola unità.

Domini, unità organizzative, utenti, gruppi di utenti, computer e altri elementi di rete vengono archiviati come oggetti in Active Directory Domain Services. In Windows 2000 e versioni successive di Windows, è comunque possibile aggiungere utenti, gruppi di utenti e computer a un dominio. Tuttavia, è ora possibile aggiungere questi oggetti a un contenitore OU o a qualsiasi altro tipo di contenitore che l'oggetto si vuole aggiungere definisce nell'attributo **possSuperiors** dell'oggetto **classSchema** . si tratta di un attributo dell'oggetto **classSchema** di un oggetto e questo attributo limita i tipi di oggetti che possono contenere tale oggetto.

 

 