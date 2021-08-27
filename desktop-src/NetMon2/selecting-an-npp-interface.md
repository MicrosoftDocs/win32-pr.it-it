---
description: I provider di pacchetti di rete espongono le interfacce IDelaydC, IESP, IRTC e IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Selezione di un'interfaccia NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4336c4ff2408aa89d723dd451174ef6dca81eba39c17c52aefdc829018e71483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128851"
---
# <a name="selecting-an-npp-interface"></a>Selezione di un'interfaccia NPP

I provider di pacchetti di rete espongono le interfacce [**IDelaydC,**](idelaydc.md) [**IESP,**](iesp.md) [**IRTC**](irtc.md)e [**IStats.**](istats.md) Ognuna di queste interfacce fornisce metodi simili per connettere NPP alla rete, acquisire il traffico di rete e raccogliere informazioni statistiche sui dati acquisiti. Per scegliere l'interfaccia da usare, vedere la tabella seguente.

> [!Note]  
> Quando si connette un NPP alla rete con una di queste interfacce, è possibile usare solo i metodi forniti da tale interfaccia. Ad esempio, se ci si connette alla rete usando [**l'interfaccia IRTC**](irtc.md) e quindi si tenta di avviare un'acquisizione con [**IDelaydC,**](idelaydc.md)la chiamata per avviare l'acquisizione avrà esito negativo e verrà restituito un codice di errore.

 



| Interfaccia                    | Utilizzo                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDelaydC**](idelaydc.md) | Usare per acquisire il traffico di rete e archiviarlo in un file di acquisizione. Questa interfaccia viene usata dall'interfaccia Network Monitor e da altre applicazioni NPP, che richiedono l'archiviazione delle informazioni di rete acquisite.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Usato per fornire statistiche avanzate in un formato di file ESP speciale. Questa interfaccia viene usata dalle applicazioni NPP che richiedono le statistiche avanzate fornite dal formato ESP.<br/>                                                                                                                                                        |
| [**IRTC**](irtc.md)         | Usare per acquisire il traffico di rete in tempo reale e attivare gli eventi quando si verificano. Questa interfaccia viene usata dalle applicazioni NPP che richiedono acquisizioni in fase di esecuzione. Si noti che questa interfaccia non fornisce le statistiche fornite dalle altre interfacce NPP, né consente di inserire frame nel traffico di rete acquisito.<br/> |
| [**IStats**](istats.md)     | Usare per recuperare le statistiche di acquisizione, ma non i frame acquisiti.                                                                                                                                                                                                                                                                                 |



 

 

 




