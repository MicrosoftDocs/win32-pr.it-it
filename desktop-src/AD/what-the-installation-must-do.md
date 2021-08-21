---
title: Cosa deve fare l'installazione
description: I nuovi attributi a cui si fa riferimento nel passaggio 3 devono essere indicati dal relativo OID perché il nuovo nome dell'attributo non è presente nella cache dello schema a questo punto.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Cosa deve fare AD l'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3dcf125a171fba921a5341ad5f3de8bbe5d791d4eb4dc072f551345df3218ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182174"
---
# <a name="what-the-installation-must-do"></a>Cosa deve fare l'installazione

Le applicazioni che estendono lo schema devono applicare gli aggiornamenti come descritto nella procedura seguente.

**Per applicare gli aggiornamenti durante l'estensione dello schema**

1.  Aggiungere i nuovi attributi.
2.  Aggiungere le nuove classi.
3.  Aggiungere i nuovi attributi alle classi.
4.  Attivare un ricaricamento della cache.

I nuovi attributi a cui si fa riferimento nel passaggio 3 devono essere indicati dal relativo OID perché il nuovo nome dell'attributo non è presente nella cache dello schema a questo punto.

Il passaggio 4 non è necessario se le estensioni non verranno usate immediatamente. Le estensioni verranno visualizzate nella cache dello schema in circa 5 minuti, a seconda del carico di sistema. Per altre informazioni sulla cache dello schema e su come attivare un ricaricamento della cache, vedere [Aggiornamento della cache dello schema](updating-the-schema-cache.md).

 

 




