---
title: Cosa deve fare l'installazione
description: I nuovi attributi a cui si fa riferimento nel passaggio 3 devono essere indicati dal relativo OID perché il nuovo nome dell'attributo non è presente nella cache dello schema a questo punto.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Cosa deve fare l'installazione di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955125"
---
# <a name="what-the-installation-must-do"></a>Cosa deve fare l'installazione

Le applicazioni che estendono lo schema devono applicare gli aggiornamenti come descritto nella procedura seguente.

**Per applicare gli aggiornamenti quando si estende lo schema**

1.  Aggiungere i nuovi attributi.
2.  Aggiungere le nuove classi.
3.  Aggiungere i nuovi attributi alle classi.
4.  Attivare un ricaricamento della cache.

I nuovi attributi a cui si fa riferimento nel passaggio 3 devono essere indicati dal relativo OID perché il nuovo nome dell'attributo non è presente nella cache dello schema a questo punto.

Il passaggio 4 non è necessario se le estensioni non verranno utilizzate immediatamente; le estensioni verranno visualizzate nella cache dello schema in circa 5 minuti, a seconda del carico di sistema. Per ulteriori informazioni sulla cache degli schemi e su come attivare un ricaricamento della cache, vedere [aggiornamento della cache dello schema](updating-the-schema-cache.md).

 

 




