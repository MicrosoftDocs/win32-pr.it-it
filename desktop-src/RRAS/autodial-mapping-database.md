---
title: Database di mapping di Autodial
description: Il database di mapping della connessione automatica esegue il mapping degli indirizzi di rete alle voci del libro telefonico RAS.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511f15f98848559a892e8c20e766d47a07780fbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872601"
---
# <a name="autodial-mapping-database"></a>Database di mapping di Autodial

Il database di mapping della connessione automatica esegue il mapping degli indirizzi di rete alle voci del libro telefonico RAS. Il database può includere indirizzi IP (ad esempio, "172.21.167.35"), nomi host Internet (ad esempio, "www.microsoft.com") o nomi NetBIOS (ad esempio, "Products1"). Associato a ogni indirizzo nel database Autodial è un set di una o più voci [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) . Ognuna di queste voci specifica una voce della rubrica telefonica che RAS può comporre per connettersi all'indirizzo da una particolare posizione di connessione TAPI (Telephony Application Programming Interface). Per ulteriori informazioni sui percorsi di composizione TAPI, vedere la documentazione di TAPI.

Autodial crea automaticamente le voci nel database di mapping della connessione automatica in due situazioni:

-   Quando un tentativo di connessione a un indirizzo di rete ha esito negativo

    Se non è presente alcuna voce per l'indirizzo nel database di mapping e il computer non è connesso a una rete, direttamente o tramite RAS, la connessione automatica richiede all'utente di specificare le informazioni necessarie per stabilire una connessione remota. Se l'utente fornisce le informazioni e l'operazione di connessione remota ha esito positivo, Autodial archivia le informazioni nel database di mapping.

-   Quando il computer è connesso a una rete tramite RAS

    Ogni volta che l'utente si connette a un indirizzo di rete, Autodial crea una voce nel database. La voce esegue il mapping dell'indirizzo di rete alla voce della Rubrica utilizzata per stabilire la connessione RAS.

È possibile utilizzare la funzione [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) per aggiungere un indirizzo al database di mapping della connessione automatica, eliminare un indirizzo dal database o modificare le voci di composizione automatica associate a un indirizzo esistente nel database. È possibile utilizzare la funzione [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) per recuperare le voci di composizione automatica associate a un indirizzo di rete specificato nel database di mapping della connessione automatica. La funzione [**RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) restituisce un elenco di tutti gli indirizzi nel database di mapping della connessione automatica.

 

 