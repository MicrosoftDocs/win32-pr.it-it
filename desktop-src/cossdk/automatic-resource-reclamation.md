---
description: Recupero automatico delle risorse
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recupero automatico delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec280c0b0ae222cf0c63e136b7643bbd05c1fffa5589ccc4b736dd247a43b1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730671"
---
# <a name="automatic-resource-reclamation"></a>Recupero automatico delle risorse

COM+ invia una notifica al gestore di dispenser ogni volta che termina la durata di un oggetto. Il gestore del dispenser invia quindi una notifica al titolare di ogni dispenser di risorse registrato per verificare se l'oggetto dispone ancora di risorse. In tal caso, tali risorse vengono liberate, impedendo la possibilità di perdite di risorse da parte dei componenti che ottengono le risorse tramite un dispenser di risorse.

La funzionalità di recupero automatico è un'opzione disattivata per impostazione predefinita. Un dispenser di risorse può scegliere di abilitare questa opzione e, in questo modo, garantisce che un riferimento a qualsiasi risorsa a un oggetto non sia mai restituito dai metodi dell'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti del dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



