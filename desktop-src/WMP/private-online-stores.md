---
title: Negozi online privati
description: Negozi online privati
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player Online Stores, privato
- negozi online, privati
- digitare 1 negozi online, privato
- digitare 2 archivi online, privato
- negozi online privati
- Registro di sistema, archivi online privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396358"
---
# <a name="private-online-stores"></a>Negozi online privati

Windows Media Player 10 o versioni successive supporta i negozi online privati; ovvero archivi visibili solo a determinati utenti. Perché un archivio online privato sia visibile all'utente corrente, è necessario che sia presente una voce che rappresenta l'archivio online privato nella seguente chiave del registro di sistema.

HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ PrivateServices

La voce del registro di sistema obbligatoria deve avere il formato seguente.



| Nome                                                         | Type           | valore                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Qualsiasi nome scelto dall'utente che crea la voce del registro di sistema | **REG \_ DWORD** | Un numero, fornito da Microsoft, che identifica lo Store online privato |



 

Il controllo ActiveX di Windows Media Player 10 supporta i negozi online privati solo se il controllo è in esecuzione in modalità remota. Il controllo ActiveX di Windows Media Player 11 supporta i negozi online privati indipendentemente dal fatto che il controllo sia in esecuzione in modalità remota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




