---
description: La classe CMSPThread implementa il thread di lavoro MSPs.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317650"
---
# <a name="cmspthread"></a>CMSPThread

La classe **CMSPThread** implementa il thread di lavoro di msp. Le classi base usano questo thread di lavoro per diversi scopi. Viene fornito un meccanismo di elemento di lavoro generico e leggero che consente all'MSP derivato di utilizzare questo thread per i propri elementi di lavoro sincroni o asincroni, indipendentemente dal fatto che si verifichino. Il thread pompa inoltre i messaggi e supporta la gestione di APC (anche se non vengono utilizzati APC nelle classi base).

Quando sono presenti più indirizzi like, ovvero quando viene creata più volte la stessa implementazione di MSP della stessa DLL, la classe thread garantisce la scalabilità utilizzando automaticamente un singolo thread per tutti gli indirizzi. L'interfaccia alla classe thread è tale che l'implementazione MSP può considerare la classe thread come un thread privato e non deve preoccuparsi degli altri indirizzi che potrebbero condividerla.

Definito in MSPthrd. h.

 

 



