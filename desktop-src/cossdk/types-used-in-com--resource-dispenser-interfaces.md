---
description: Tipi utilizzati nelle interfacce del dispenser di risorse COM+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Tipi utilizzati nelle interfacce del dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c4d0f62ec7c61a9bc0f189c1ee02d1868a3242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748642"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Tipi utilizzati nelle interfacce del dispenser di risorse COM+

I tipi seguenti vengono usati nelle interfacce del dispenser di risorse.



| Tipo           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | **DWORD** che identifica un tipo di risorsa, non una risorsa specifica. Un **RESTYPID** è in genere un puntatore a una struttura nella memoria del dispenser che descrive il tipo di risorsa. Il responsabile del dispenser non riconosce (e non deve comprendere) questa struttura nella memoria del dispenser di risorse. Il gestore di dispenser USA **RESTYPID** solo per fare riferimento a un tipo di risorsa all'interno di un dispenser di risorse.                                                                                                                                   |
| **DA un Resid**      | **Valore DWORD** che identifica una determinata risorsa, anziché un tipo di risorsa. Un **da un Resid** è in genere un (**void \* *_) che punta a una struttura nella memoria del dispenser di risorse che rappresenta la risorsa. Il responsabile del dispenser non deve comprendere questa struttura nella memoria del dispenser di risorse. Il gestore di dispenser USA _* da un Resid** per fare riferimento a una determinata risorsa all'interno di un dispenser di risorse.                                                                                                                                 |
| **SRESID**     | Versione di stringa Unicode di **da un Resid**, usata nei metodi [**IHolder:: TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) e [**IHolder:: UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) . Le stringhe sono talvolta utili quando è necessario registrare solo una piccola quantità di informazioni su una risorsa e l'intera descrizione della risorsa può essere contenuta in **SRESID**. In particolare, l'uso di **SRESID** può talvolta eliminare la necessità di una mappa nel dispenser di risorse quando la risorsa rappresenta una relazione tra due o più elementi. |
| **TRANSID**    | Identifica una transazione. È possibile eseguire il cast di questo tipo nell'interfaccia **ITransaction** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Indica per quanto tempo una risorsa può rimanere inattiva prima di essere eliminata definitivamente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfacce del dispenser di risorse COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



