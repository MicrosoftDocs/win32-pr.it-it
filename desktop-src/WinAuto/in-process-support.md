---
title: Supporto In-Process
description: L'implementazione corrente dell'annotazione dinamica è interamente in-process e di conseguenza consente solo agli elementi dell'interfaccia utente di essere annotati dal processo che possiede gli elementi dell'interfaccia utente.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328948"
---
# <a name="in-process-support"></a>Supporto In-Process

L'implementazione corrente dell'annotazione dinamica è interamente in-process e di conseguenza consente solo agli elementi dell'interfaccia utente di essere annotati dal processo che possiede gli elementi dell'interfaccia utente. Non è possibile che un processo annotare gli elementi dell'interfaccia utente di un altro processo.

Si noti che questa operazione influisca solo sull'impostazione di un'annotazione. non interferisce con la capacità dei client di accedere alle proprietà (annotate o in altro modo) degli elementi dell'interfaccia utente in altri processi.

 

 




