---
description: Recupero automatico delle risorse
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recupero automatico delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342291"
---
# <a name="automatic-resource-reclamation"></a>Recupero automatico delle risorse

COM+ invia una notifica al Manager di dispenser ogni volta che termina la durata di un oggetto. Il responsabile del dispenser invia quindi una notifica a ogni titolare del dispenser di risorse registrate per verificare se sono presenti risorse ancora utilizzate da questo oggetto. In tal caso, tali risorse vengono liberate, impedendo la possibilità di perdite di risorse da parte di componenti che ottengono risorse tramite un dispenser di risorse.

La funzionalità di recupero automatico è un'opzione che è disattivata per impostazione predefinita. Un dispenser di risorse può scegliere di abilitare questa opzione e, in questo modo, garantisce che un riferimento a una risorsa distribuita a un oggetto non venga mai restituito dai metodi dell'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



