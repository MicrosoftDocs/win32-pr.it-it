---
title: Funzioni utente workstation e workstation
description: Le funzioni di workstation di gestione di rete eseguono attività amministrative su una workstation locale o remota.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300282"
---
# <a name="workstation-and-workstation-user-functions"></a>Funzioni utente workstation e workstation

Le funzioni di workstation di gestione di rete eseguono attività amministrative su una workstation locale o remota. Solo un utente o un'applicazione con appartenenza a un gruppo di amministratori, in un server locale o remoto, può eseguire attività amministrative su una workstation per controllarne il funzionamento, l'accesso degli utenti e la condivisione delle risorse. Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

Le funzioni workstation sono elencate di seguito.



| Funzione                                   | Descrizione                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | Restituisce informazioni sugli elementi di configurazione per una workstation. |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | Configura una workstation.                                               |



 

Le funzioni workstation consentono l'accesso a due tipi discreti di informazioni sulle workstation:

-   Informazioni di sistema
-   Informazioni specifiche della piattaforma

All'interno di ogni tipo i dati vengono classificati in base all'accesso di sicurezza. I dati accessibili dal Guest sono un subset dei dati accessibili dagli utenti, che a sua volta costituisce un subset dei dati accessibili dall'amministratore.

Le informazioni sulla workstation sono disponibili ai livelli seguenti:

-   [**WKSTA \_ INFO \_ 100**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [**WKSTA \_ INFO \_ 101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [**WKSTA \_ INFO \_ 102**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

Le funzioni utente della workstation di gestione di rete consentono l'accesso a informazioni specifiche dell'utente. Le informazioni specifiche dell'utente sono separate dalle informazioni della workstation perché possono essere presenti più utenti su una workstation.

Le funzioni utente della workstation sono elencate di seguito.



| Funzione                                           | Descrizione                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Elenca le informazioni su tutti gli utenti attualmente connessi alla workstation.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Restituisce informazioni su un utente attualmente connesso.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Imposta le informazioni specifiche dell'utente per gli elementi di configurazione di una workstation. |



 

Le informazioni sull'utente della workstation sono disponibili ai livelli seguenti:

-   [**\_Informazioni utente \_ WKSTA \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [**\_Informazioni utente \_ WKSTA \_ 1**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [**\_Informazioni utente \_ WKSTA \_ 1101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 