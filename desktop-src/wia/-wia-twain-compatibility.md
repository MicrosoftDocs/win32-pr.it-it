---
description: WIA fornisce un livello di compatibilità TWAIN che consente alle applicazioni compatibili con TWAIN di comunicare con i dispositivi Windows Image Acquisition (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilità con TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307327"
---
# <a name="twain-compatibility"></a>Compatibilità con TWAIN

WIA fornisce un livello di compatibilità TWAIN che consente alle applicazioni compatibili con TWAIN di comunicare con i dispositivi Windows Image Acquisition (WIA). Le applicazioni compatibili con TWAIN non dispongono dell'accesso completo alla funzionalità WIA. Ad esempio, un'applicazione non può escludere l'interfaccia utente utilizzando il livello di compatibilità TWAIN.

I dispositivi WIA vengono visualizzati due volte in un'applicazione che è in grado di riconoscere sia WIA che TWAIN: una volta tramite la comunicazione WIA normale e una volta tramite il livello di compatibilità TWAIN. Per evitare l'inserimento di un dispositivo WIA due volte, un'applicazione che è a conoscenza di WIA e TWAIN deve filtrare i dispositivi WIA che passano attraverso il livello di compatibilità TWAIN. Tutti i dispositivi WIA che passano attraverso il livello di compatibilità TWAIN hanno "WIA-" come prefisso, quindi è facile filtrarli.

 

 



