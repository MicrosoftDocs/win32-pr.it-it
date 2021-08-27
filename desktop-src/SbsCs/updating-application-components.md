---
description: Gli assembly privati side-by-side possono essere usati per creare componenti che possono essere facilmente aggiornati senza aggiornare anche l'applicazione host.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Aggiornamento dei componenti dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02948355143bc6f08c759ec6c2fe6009399cc6d8ca4b2bbd687e3d206c0e771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101591"
---
# <a name="updating-application-components"></a>Aggiornamento dei componenti dell'applicazione

Gli assembly privati side-by-side possono essere usati per creare componenti che possono essere facilmente aggiornati senza aggiornare anche l'applicazione host. Ciò consente a un servizio di aggiornamento di installare i componenti aggiornati dell'applicazione, riavviare l'applicazione e fare in modo che l'applicazione usi le modifiche. Quando si usano i manifesti dell'applicazione, la funzionalità dei componenti ospitati da un'applicazione può essere aggiornata senza dover modificare il codice dell'applicazione host.

Questo metodo può essere usato per aggiornare la versione delle risorse di un'applicazione. Ad esempio, se un'applicazione contiene un assembly, il manifesto dell'applicazione può specificare una dipendenza da questo assembly. L'applicazione può ottenere l'assembly chiamando [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) per trovare e caricare i file necessari. Uno updater deve semplicemente portare giù i bit più recenti per l'assembly, che possono esistere side-by-side con una versione precedente dell'assembly.

 

 
