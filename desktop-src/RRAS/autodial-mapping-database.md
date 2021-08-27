---
title: AutoDial Mapping Database
description: Il database di mapping AutoDial esegue il mapping degli indirizzi di rete alle voci della rubrica RAS.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e89bd065a136492281adb3424636a8820c76c76bf6867e70db75aecfa0f345d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036721"
---
# <a name="autodial-mapping-database"></a>AutoDial Mapping Database

Il database di mapping AutoDial esegue il mapping degli indirizzi di rete alle voci della rubrica RAS. Il database può includere indirizzi IP (ad esempio, "172.21.167.35"), nomi host Internet (ad esempio, "www.microsoft.com") o nomi NetBIOS (ad esempio, "products1"). Associato a ogni indirizzo nel database AutoDial è un set di una o più [**voci RASAUTODIALENTRY.**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) Ognuna di queste voci specifica una voce della rubrica che RAS può comporre per connettersi all'indirizzo da una particolare località di composizione TAPI (Telefonia Application Programming Interface). Per altre informazioni sulle località di composizione TAPI, vedere la documentazione di TAPI.

AutoDial crea automaticamente voci nel database di mapping AutoDial in due situazioni:

-   Quando un tentativo di connessione a un indirizzo di rete non riesce

    Se non è presente alcuna voce per l'indirizzo nel database di mapping e il computer non è connesso a una rete, direttamente o tramite RAS, AutoDial richiede all'utente di specificare le informazioni necessarie per stabilire una connessione remota. Se l'utente fornisce le informazioni e l'operazione di connessione remota ha esito positivo, AutoDial archivia le informazioni nel database di mapping.

-   Quando il computer è connesso a una rete tramite RAS

    Ogni volta che l'utente si connette a un indirizzo di rete, AutoDial crea una voce nel database. La voce esegue il mapping dell'indirizzo di rete alla voce della rubrica usata per stabilire la connessione RAS.

È possibile usare la funzione [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) per aggiungere un indirizzo al database di mapping AutoDial, eliminare un indirizzo dal database o modificare le voci AutoDial associate a un indirizzo esistente nel database. È possibile usare la [**funzione RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) per recuperare le voci AutoDial associate a un indirizzo di rete specificato nel database di mapping AutoDial. La [**funzione RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) restituisce un elenco di tutti gli indirizzi nel database di mapping AutoDial.

 

 