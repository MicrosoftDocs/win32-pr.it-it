---
description: Gli assembly privati affiancati possono essere usati per creare componenti che possono essere facilmente aggiornati senza aggiornare anche l'applicazione host.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Aggiornamento dei componenti dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966598"
---
# <a name="updating-application-components"></a>Aggiornamento dei componenti dell'applicazione

Gli assembly privati affiancati possono essere usati per creare componenti che possono essere facilmente aggiornati senza aggiornare anche l'applicazione host. Questo consente a un servizio di aggiornamento di installare i componenti aggiornati dell'applicazione, riavviare l'applicazione e fare in modo che l'applicazione usi le modifiche. Quando si utilizzano manifesti dell'applicazione, la funzionalità dei componenti ospitati da un'applicazione può essere aggiornata senza dover modificare il codice dell'applicazione host.

Questo metodo può essere utilizzato per aggiornare la versione delle risorse di un'applicazione. Se, ad esempio, un'applicazione contiene un assembly, il manifesto dell'applicazione può specificare una dipendenza da questo assembly. L'applicazione può ottenere l'assembly chiamando [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) per trovare e caricare i file necessari. Un aggiornamento deve semplicemente arrestare i bit più recenti per l'assembly, che possono esistere side-by-side con una versione precedente dell'assembly.

 

 
