---
title: Che cos'è il modello a oggetti del punto di controllo
description: Nella figura seguente viene illustrato il modello a oggetti control point di base.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06fa7e9cd8fa2bd2e038002414260bf2468f8d951c24da42bdd7a687af06bc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007966"
---
# <a name="what-is-the-control-point-object-model"></a>Che cos'è il modello a oggetti del punto di controllo?

Nella figura seguente viene illustrato il modello a oggetti control point di base.

![modello a oggetti del punto di controllo](images/upnp-object-model.png)

La ricerca di dispositivi con l'interfaccia device finder crea una raccolta Dispositivi. Una raccolta Devices contiene zero o più oggetti Device. Le applicazioni possono usare i vari metodi di raccolta Dispositivi per accedere ai singoli oggetti Device.

Gli oggetti dispositivo contengono sempre una raccolta Services che contiene uno o più oggetti Service. Questi oggetti servizio vengono usati dalle applicazioni per comunicare con e controllare i dispositivi.

 

 




