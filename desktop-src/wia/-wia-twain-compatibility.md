---
description: WIA offre un livello di compatibilità TWAIN che consente alle applicazioni compatibili con TWAIN di comunicare con Windows di acquisizione di immagini (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilità con TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3633dfc97a5356f2d63dd2d377e798312a9a2fb10fd03144222e5ed3b4fd0dc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056981"
---
# <a name="twain-compatibility"></a>Compatibilità con TWAIN

WIA offre un livello di compatibilità TWAIN che consente alle applicazioni compatibili con TWAIN di comunicare con Windows di acquisizione di immagini (WIA). Le applicazioni che supportano TWAIN non hanno accesso completo alla funzionalità WIA. Ad esempio, un'applicazione non può eliminare l'interfaccia utente usando il livello di compatibilità TWAIN.

I dispositivi WIA vengono visualizzati due volte in un'applicazione che è in grado di riconoscere sia WIA che TWAIN: una volta tramite la normale comunicazione WIA e una volta tramite il livello di compatibilità TWAIN. Per evitare di elencare due volte un dispositivo WIA, un'applicazione che è in grado di riconoscere sia WIA che TWAIN deve filtrare i dispositivi WIA che passano attraverso il livello di compatibilità TWAIN. Tutti i dispositivi WIA che passano attraverso il livello di compatibilità TWAIN hanno "WIA-" come prefisso, quindi è facile filtrarli.

 

 



