---
description: Il \_ \_ mutex MsiPromptForCD esiste quando il programma di installazione richiede all'utente di inserire un CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: Mutex __MsiPromptForCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311120"
---
# <a name="__msipromptforcd-mutex"></a>\_\_Mutex MsiPromptForCD

Il \_ \_ mutex MsiPromptForCD esiste quando il programma di installazione richiede all'utente di inserire un CD-ROM. I programmi AutoPlay devono verificare che il \_ \_ mutex MsiPromptForCD non sia attualmente impostato prima di iniziare. Si noti che è possibile che si verifichi un prompt CD-ROM prima che sia presente la chiave in corso o il \_ mutex MSIExecute.

 

 



