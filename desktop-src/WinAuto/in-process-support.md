---
title: In-Process supporto
description: L'implementazione corrente dell'annotazione dinamica è interamente in-process e di conseguenza consente solo agli elementi dell'interfaccia utente di essere annotati dal processo proprietario di tali elementi dell'interfaccia utente.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82deaa2edd9a5df9fd36bed745d1c07a5542e12837cd3fc97c3ac0bdeab098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614741"
---
# <a name="in-process-support"></a>In-Process supporto

L'implementazione corrente dell'annotazione dinamica è interamente in-process e di conseguenza consente solo agli elementi dell'interfaccia utente di essere annotati dal processo proprietario di tali elementi dell'interfaccia utente. Non è possibile per un processo annotare gli elementi dell'interfaccia utente di un altro processo.

Si noti che ciò influisce solo sull'azione di impostazione di un'annotazione. non interferisce con la capacità dei client di accedere alle proprietà (annotate o meno) degli elementi dell'interfaccia utente in altri processi.

 

 




