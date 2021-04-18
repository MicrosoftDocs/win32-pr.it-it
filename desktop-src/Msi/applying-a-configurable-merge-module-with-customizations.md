---
description: Seguire le linee guida generali per l'applicazione dei moduli di merge descritti in applicazione di moduli di Unione.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Applicazione di un modulo merge configurabile con personalizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311057"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Applicazione di un modulo merge configurabile con personalizzazioni

Seguire le linee guida generali per l'applicazione dei moduli di merge descritti in [applicazione di moduli di Unione](applying-merge-modules.md). Per configurare un modulo merge al momento dell'installazione, inoltre, gli utenti del modulo merge devono eseguire le operazioni seguenti:

-   Utilizzare un modulo merge creato per avere impostazioni configurabili. Per ulteriori informazioni, vedere [creazione di un modulo merge che può essere configurato dall'utente finale](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)
-   Usare uno strumento di merge e configurazione che chiama Mergemod.dll versione 2,0 o successiva. Nelle versioni precedenti di Mergmod.dll non è possibile configurare le impostazioni del modulo merge. Gli autori devono creare moduli unione che forniscano valori predefiniti e siano compatibili con le versioni precedenti di Mergmod.dll.
-   Fornire le informazioni di personalizzazione quando richiesto dallo strumento client di configurazione. Gli autori devono creare moduli merge che utilizzano valori predefiniti quando un utente rifiuta di fornire informazioni.

 

 



