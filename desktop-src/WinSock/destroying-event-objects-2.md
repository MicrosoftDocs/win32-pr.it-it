---
description: Utilizzo di WPUCloseEvent per eliminare definitivamente un oggetto evento (applicazione o provider di servizi) quando l'oggetto evento non è più necessario.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Eliminazione definitiva di oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f0a17f623d0dd9ebceaf76b963ce72306000b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343541"
---
# <a name="destroying-event-objects"></a>Eliminazione definitiva di oggetti evento

L'entità che crea un oggetto evento (applicazione o provider di servizi) è responsabile dell'eliminazione di un oggetto quando non è più necessario. I provider di servizi eseguono questa operazione tramite **WPUCloseEvent**.

 

 



