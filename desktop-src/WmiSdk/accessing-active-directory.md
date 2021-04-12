---
description: Active Directory è il servizio directory per Windows ed è la base di reti distribuite di Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Accesso a Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233473"
---
# <a name="accessing-active-directory"></a>Accesso a Active Directory

Active Directory è il servizio directory per Windows ed è la base di reti distribuite di Windows. È possibile utilizzare Active Directory per individuare gli oggetti in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse. Il nome Active Directory si riferisce sia al servizio directory che alla directory stessa.

> [!Note]  
> Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).

 

Windows rende Active Directory accessibili tramite WMI creando un set di riferimenti a ogni classe e oggetto contenuto in Active Directory. Accedendo al provider di servizi directory tramite WMI, è possibile creare applicazioni abilitate per WMI in grado di accedere alle numerose informazioni contenute in Active Directory.

Con queste interfacce è possibile:

-   Recuperare classi e istanze.
-   Enumerare classi e istanze.
-   Creare nuove istanze.
-   Modificare le istanze esistenti.
-   Elimina le istanze esistenti.
-   Active Directory query.

Gli argomenti seguenti possono risultare utili per l'utilizzo di Active Directory con WMI:

-   [Uso della sintassi di Active Directory appropriata](using-the-proper-active-directory-syntax.md)
-   [Mapping di Active Directory a WMI](mapping-active-directory-to-wmi.md)

 

 



