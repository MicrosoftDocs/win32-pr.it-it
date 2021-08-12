---
description: Tipi usati nelle interfacce del dispenser di risorse COM+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Tipi usati nelle interfacce del dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e98473ce108ea280532c2188e911b488e42669b98273b14fc229d003905b581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305231"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Tipi usati nelle interfacce del dispenser di risorse COM+

Nelle interfacce del distributore di risorse vengono usati i tipi seguenti.



| Tipo           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | Valore **DWORD** che identifica un tipo di risorsa, non una risorsa specifica. **RestYPID è** in genere un puntatore a una struttura nella memoria del distributore che descrive il tipo di risorsa. Il gestore di dispenser non comprende (e non deve comprendere) questa struttura all'interno della memoria del dispenser di risorse. Il gestore dispenser usa **RESTYPID solo** per fare riferimento a un tipo di risorsa all'interno di un dispenser di risorse.                                                                                                                                   |
| **Resid**      | Valore **DWORD** che identifica una determinata risorsa, anziché un tipo di risorsa. Un **RESID** è in genere un ( void _) che punta a una struttura nella memoria del distributore di risorse **che rappresenta la \* *risorsa. Il gestore di dispenser non deve comprendere questa struttura all'interno della memoria del distributore di risorse. Il gestore dispenser usa _* RESID** per fare riferimento a una determinata risorsa all'interno di un dispenser di risorse.                                                                                                                                 |
| **SRESID**     | Versione di stringa Unicode di **RESID,** usata nei metodi [**IHolder::TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) e [**IHolder::UntrackResourceS.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) Le stringhe sono talvolta utili quando è necessario registrare solo una piccola quantità di informazioni su una risorsa e l'intera descrizione della risorsa può essere contenuta in **SRESID**. In particolare, l'uso **di SRESID** può talvolta eliminare la necessità di una mappa nel distributore di risorse quando la risorsa rappresenta una relazione tra due (o più) elementi. |
| **TRANSID**    | Identifica una transazione. È possibile eseguire il cast di questo tipo **all'interfaccia ITransaction.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Indica per quanto tempo una risorsa può essere inattiva prima di essere distrutta.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi ai distributori di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfacce del distributore di risorse COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



