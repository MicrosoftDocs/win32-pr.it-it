---
title: Funzioni Get
description: Le funzioni Get di gestione della rete recuperano le informazioni relative a un dominio. È inoltre possibile chiamare queste funzioni per recuperare informazioni sugli account utente locali, globali, workstation e server.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515853"
---
# <a name="get-functions"></a>Funzioni Get

Le funzioni Get di gestione della rete recuperano le informazioni relative a un dominio. È inoltre possibile chiamare queste funzioni per recuperare informazioni sugli account utente locali, globali, workstation e server.

Le funzioni di Get di gestione della rete sono elencate di seguito.



| Funzione                                                               | Descrizione                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Restituisce il nome di un controller di dominio che è direttamente attendibile da un server specificato.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Restituisce il nome del controller di dominio primario (PDC) per il dominio specificato.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Restituisce l'indice della prima voce di informazioni di visualizzazione il cui nome inizia con una stringa specificata o segue la stringa in ordine alfabetico. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Restituisce le informazioni sull'account utente, computer o gruppo globale.                                                                             |



 

Le informazioni restituite dalla funzione [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) sono disponibili ai livelli seguenti:

-   [**\_gruppo di visualizzazione NET \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**NET \_ display \_ computer**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**NET \_ display \_ User**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




