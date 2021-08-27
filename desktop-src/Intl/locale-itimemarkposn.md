---
description: IMPOSTAZIONI \_ LOCALI ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802da8f3d1029dd42c14eb536175d16e897d34a11edbd6be0bfe4f30d44c42db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106460"
---
# <a name="locale_itimemarkposn"></a>IMPOSTAZIONI \_ LOCALI ITIMEMARKPOSN

Identificatore che indica se la stringa del marcatore temporale (AM o PM) precede o segue la stringa di ora. Il valore del Registro di sistema è iTimePrefix per compatibilità con le versioni asiatiche precedenti di Windows. L'identificatore deve avere uno dei valori seguenti. Non sono consentiti valori specificati dall'utente. È preferibile che l'applicazione usi la costante [LOCALE \_ STIMEFORMAT](locale-stime-constants.md) anziché LOCALE \_ ITIMEMARKPOSN.



| Valore | Significato        |
|-------|----------------|
| 0     | Usare come suffisso. |
| 1     | Usare come prefisso. |



 

 

 



