---
description: impostazioni locali \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0182235754d8f5b6b95bad6c58b4fee87d394d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319985"
---
# <a name="locale_itimemarkposn"></a>impostazioni locali \_ ITIMEMARKPOSN

Identificatore che indica se la stringa del marcatore temporale (AM o PM) precede o segue la stringa dell'ora. Il valore del registro di sistema è iTimePrefix per la compatibilità con le versioni asiatiche precedenti di Windows. L'identificatore deve avere uno dei valori seguenti. Non sono consentiti valori specificati dall'utente. È preferibile che l'applicazione usi la costante [ \_ STIMEFORMAT delle impostazioni locali](locale-stime-constants.md) anziché ITIMEMARKPOSN delle impostazioni locali \_ .



| Valore | Significato        |
|-------|----------------|
| 0     | Utilizzare come suffisso. |
| 1     | Usare come prefisso. |



 

 

 



