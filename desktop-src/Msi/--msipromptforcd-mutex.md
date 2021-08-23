---
description: Il \_ \_ mutex MsiPromptForCD esiste quando il programma di installazione richiede all'utente di inserire un CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba2c829cb0102192b4c2bc2670892f8849000a6ed9cad2a88e7f3e3e557b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764291"
---
# <a name="__msipromptforcd-mutex"></a>\_\_MsiPromptForCD Mutex

Il \_ \_ mutex MsiPromptForCD esiste quando il programma di installazione richiede all'utente di inserire un CD-ROM. I programmi di riproduzione automatica devono verificare che il \_ \_ mutex MsiPromptForCD non sia attualmente impostato prima dell'avvio. Si noti che è possibile che venga visualizzata una richiesta CD-ROM prima dell'esistenza della chiave InProgress o del \_ mutex MSIExecute.

 

 



