---
title: Negozi online privati
description: Negozi online privati
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player negozi online, privati
- negozi online, privati
- tipo 1 negozi online, privato
- Negozi online di tipo 2, privati
- negozi online privati
- registro, negozi online privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0667c19ffde3bb3c78b539253650e4f6f0b84cfbfd940f4d06237f987b99efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002931"
---
# <a name="private-online-stores"></a>Negozi online privati

Windows Media Player 10 o versioni successive supporta negozi online privati; in altri casi, archivi visibili solo a determinati utenti. Perché un negozio online privato sia visibile all'utente corrente, deve essere presente una voce che rappresenta il negozio online privato nella chiave del Registro di sistema seguente.

HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ PrivateServices

La voce del Registro di sistema richiesta deve avere il formato seguente.



| Nome                                                         | Type           | valore                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Qualsiasi nome scelto dalla persona che crea la voce del Registro di sistema | **REG \_ DWORD** | Numero, fornito da Microsoft, che identifica il negozio online privato |



 

Il Windows Media Player 10 ActiveX supporta negozi online privati solo se il controllo è in esecuzione in modalità remota. Il Windows Media Player 11 ActiveX supporta negozi online privati indipendentemente dal fatto che il controllo sia in esecuzione in modalità remota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




