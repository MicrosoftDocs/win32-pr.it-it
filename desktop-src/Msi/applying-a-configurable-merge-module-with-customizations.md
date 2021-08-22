---
description: Seguire le linee guida generali per l'applicazione di moduli unione descritti in Applicazione di moduli unione.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Applicazione di un modulo unione configurabile con personalizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9c771493a7a8e854472d840ffc21358c9741d8b3a8ea9876251456b6badf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829201"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Applicazione di un modulo unione configurabile con personalizzazioni

Seguire le linee guida generali per l'applicazione di moduli unione descritti in [Applicazione di moduli unione](applying-merge-modules.md). Inoltre, i consumer di moduli unione devono eseguire le operazioni seguenti per configurare un modulo unione al momento dell'installazione:

-   Usare un modulo unione creato per avere impostazioni configurabili. Per altre informazioni, vedere [Creazione di un modulo unione che può essere configurato dall'utente finale](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)
-   Usare uno strumento di unione e configurazione che chiama Mergemod.dll versione 2.0 o successiva. Le versioni precedenti di Mergmod.dll possono configurare le impostazioni del modulo unione. Gli autori devono creare moduli unione che forniscono valori predefiniti e sono compatibili con le versioni precedenti di Mergmod.dll.
-   Specificare le informazioni di personalizzazione quando richiesto dallo strumento client di configurazione. Gli autori devono creare moduli unione che usano valori predefiniti quando un utente rifiuta di fornire informazioni.

 

 



