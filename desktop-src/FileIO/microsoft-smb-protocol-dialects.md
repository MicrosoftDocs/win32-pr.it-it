---
description: Per stabilire una connessione tra un client e un server utilizzando il protocollo SMB Microsoft, è necessario innanzitutto determinare il dialetto con il livello più elevato di funzionalità supportate dal client e dal server.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialetti del protocollo SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484732"
---
# <a name="microsoft-smb-protocol-dialects"></a>Dialetti del protocollo SMB Microsoft

L'elenco dei pacchetti di messaggi del protocollo SMB Microsoft è cresciuto nel corso degli anni per supportare le funzionalità crescenti del protocollo SMB Microsoft e ora i numeri delle centinaia. Ogni fase della sua crescita è contrassegnata da un set di pacchetti standard o dal dialetto. Ogni dialetto è identificato da una stringa standard, ad esempio "PC NETWORK PROGRAM 1,0", "MICROSOFT NETWORKs 3,0", "DOS LANMAN 2,1" o "NT LM 0,12". La prima stringa identifica il primo dialetto SMB e l'ultima stringa identifica CIFS, il primo dialetto del protocollo SMB Microsoft.

La maggior parte dei client Windows supporta almeno sei dialetti diversi del protocollo SMB Microsoft, quindi uno dei primi passaggi per stabilire una connessione tra un client e un server tramite il protocollo SMB Microsoft consiste nel determinare il dialetto con il massimo livello di funzionalità supportato dal client e dal server. Questo processo è noto come "negoziazione del dialetto". Le stringhe di dialetto indicate in precedenza sono incluse nei pacchetti di richiesta e risposta di negoziazione di dialetto per questo scopo.

 

 



