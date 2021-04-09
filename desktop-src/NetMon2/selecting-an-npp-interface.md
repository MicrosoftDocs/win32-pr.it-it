---
description: I provider di pacchetti di rete (centrali) espongono le interfacce IDelaydC, IESP, IRTC e IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Selezione di un'interfaccia NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880702"
---
# <a name="selecting-an-npp-interface"></a>Selezione di un'interfaccia NPP

I provider di pacchetti di rete (centrali) espongono le interfacce [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md)e [**IStats**](istats.md) . Ognuna di queste interfacce fornisce metodi simili per connettere l'oggetto NPP alla rete, acquisire il traffico di rete e raccogliere informazioni statistiche sui dati acquisiti. Per scegliere l'interfaccia da utilizzare, fare riferimento alla tabella seguente.

> [!Note]  
> Quando si connette un oggetto NPP alla rete con una di queste interfacce, è possibile utilizzare solo i metodi forniti da tale interfaccia. Se ad esempio ci si connette alla rete usando l'interfaccia [**IRTC**](irtc.md) e quindi si prova ad avviare un'acquisizione con [**IDelaydC**](idelaydc.md), la chiamata per avviare l'acquisizione avrà esito negativo e verrà restituito un codice di errore.

 



| Interfaccia                    | Utilizzo                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDelaydC**](idelaydc.md) | Usare per acquisire il traffico di rete e archiviarlo in un file di acquisizione. Questa interfaccia viene utilizzata dall'interfaccia utente di Network Monitor e da altre applicazioni NPP, che richiedono l'archiviazione delle informazioni di rete acquisite.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Utilizzato per fornire statistiche avanzate in un formato di file ESP speciale. Questa interfaccia viene utilizzata dalle applicazioni NPP che richiedono le statistiche avanzate fornite dal formato ESP.<br/>                                                                                                                                                        |
| [**IRTC**](irtc.md)         | Usare per acquisire il traffico di rete in tempo reale e per attivare eventi quando si verificano. Questa interfaccia viene utilizzata dalle applicazioni NPP che richiedono acquisizioni in fase di esecuzione. Si noti che questa interfaccia non fornisce le statistiche fornite dalle altre interfacce di NPP, né consente di inserire frame nel traffico di rete acquisito.<br/> |
| [**IStats**](istats.md)     | Usare per recuperare le statistiche di acquisizione ma non i frame acquisiti.                                                                                                                                                                                                                                                                                 |



 

 

 




