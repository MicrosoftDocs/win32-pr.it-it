---
description: Active Directory è il servizio directory per Windows ed è alla base della Windows distribuite.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Accesso ad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a5e60899e07335795d9728045f1e53876b013bb62c85176479fa7953ac45d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131964"
---
# <a name="accessing-active-directory"></a>Accesso ad Active Directory

Active Directory è il servizio directory per Windows ed è alla base della Windows distribuite. È possibile utilizzare Active Directory per individuare gli oggetti in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse. Il nome Active Directory fa riferimento sia al servizio directory che alla directory stessa.

> [!Note]  
> Per altre informazioni sul supporto e sull'installazione di questo componente in un sistema operativo specifico, vedere Disponibilità del sistema [operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)

 

Windows Active Directory è accessibile tramite WMI creando un set di riferimenti a ogni classe e oggetto contenuto in Active Directory. Accedendo al provider di servizi directory tramite WMI, è possibile creare applicazioni abilitate per WMI in grado di accedere alla grande quantità di informazioni contenute in Active Directory.

Con queste interfacce è possibile:

-   Recuperare classi e istanze.
-   Enumerare classi e istanze.
-   Creare nuove istanze.
-   Modificare le istanze esistenti.
-   Eliminare le istanze esistenti.
-   Query Active Directory.

Gli argomenti seguenti possono essere utili per l'uso di Active Directory con WMI:

-   [Uso della sintassi Active Directory appropriata](using-the-proper-active-directory-syntax.md)
-   [Mapping di Active Directory a WMI](mapping-active-directory-to-wmi.md)

 

 



