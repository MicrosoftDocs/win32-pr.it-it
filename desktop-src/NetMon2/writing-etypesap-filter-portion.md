---
description: La parte ETYPE/SAP del filtro di acquisizione notifica al driver Network Monitor di accettare i frame con una combinazione specifica di ETYPE del e punti di accesso al servizio (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Scrittura della parte di filtro ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968093"
---
# <a name="writing-etypesap-filter-portion"></a>Scrittura della parte di filtro ETYPE/SAP

La parte ETYPE/SAP del filtro di acquisizione notifica al driver Network Monitor di accettare i frame con una combinazione specifica di ETYPE del e [*punti di accesso al servizio*](s.md) (SAP). ETYPE del e SAP sono entrambi modi che i protocolli di basso livello, ad esempio Ethernet, LLC e snap, indicano il protocollo che li segue. In particolare:

-   Ethernet specifica un etype
-   LLC specifica un SAP
-   Snap specifica un etype

## <a name="etypesap-capture-filter-flags"></a>Flag di filtro di acquisizione ETYPE/SAP

Usare le informazioni seguenti per impostare i flag nel membro **FilterFlags** della struttura [**capturefilter**](capturefilter.md) .



| Contrassegno                                         | Significato                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_i flag capturefilter \_ includono \_ tutti i \_ succhi   | Passa tutti i valori SAP e notifica al driver che tutti i valori SAP sono validi. Se combinato con qualsiasi valore nel membro **lpSapTable** , questo flag notifica al driver che tutti i valori SAP ad eccezione di quelli presenti in **lpSapTable** sono validi.<br/>           |
| \_i flag capturefilter \_ includono \_ tutti \_ etype del | Passa tutti i valori di etype e notifica al driver che tutti i valori di ETYPE sono validi. Se combinato con qualsiasi valore nel membro **lpEtypeTable** , questo flag notifica al driver che tutti i valori ETYPE ad eccezione di quelli nel **lpEtypeTable** sono validi.<br/> |
| \_flag capturefilter \_ \_ solo locale           | Se si imposta questo flag, una scheda di interfaccia di rete non verrà impostata su P-mode. Viene visualizzato solo il traffico locale (tutti i frame nel computer locale).                                                                                                                                          |
| \_flag capturefilter \_ Keep \_ RAW             | Mantiene i frame MAC SMT e token ring.                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>Impostazioni del filtro di acquisizione di ETYPE/SAP

Usare le informazioni seguenti per impostare i membri **lpSapTable** e **LpEtypeTable** della struttura [**capturefilter**](capturefilter.md) .



| Impostazione          | Significato                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpSapTable**   | Elenca i valori SAP che si desidera vengano passati dal driver. Questo elenco indica al driver Network Monitor di convalidare tutti i frame che contengono una corrispondenza. Se \_ i flag capturefilter \_ includono \_ tutti i \_ succhi sono impostati, questo diventa un elenco di eccezioni (se trovato, non passare).           |
| **lpEtypeTable** | Elenca i valori ETYPE che si desidera vengano passati dal driver Network Monitor. Questo elenco indica solo al driver di convalidare i frame che contengono una corrispondenza. Se \_ i flag capturefilter \_ includono \_ tutti i \_ etype del impostati, questo diventa un elenco di eccezioni (se trovato, non passare). |



 

 

 




