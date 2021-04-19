---
description: I terminali collegabili sono classificati in superclassi terminal.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Voci del registro di sistema (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319871"
---
# <a name="registry-entries-telephony-api"></a>Voci del registro di sistema (API di telefonia)

I terminali collegabili sono classificati in superclassi terminal. Ogni superclasse terminal include una voce nel registro di sistema con la seguente chiave:

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **telefonia** \\ **TerminalManager**

Sotto la chiave della superclasse terminale sono presenti voci per ogni terminale collegabile all'interno della superclasse terminal.

La voce per ogni superclasse terminal è identificata da un CLSID della superclasse terminale. Si tratta di un identificatore univoco per una classe terminale. La classe terminal ha un attributo facoltativo: Name, che è un nome descrittivo per la classe terminal. Ogni terminale innestabile è identificato da una classe di terminali CLSID; ovvero un GUID. Gli attributi per il terminale collegabile sono archiviati in valori di chiave del terminale di collegamento. Gli attributi per un terminale collegabile sono i seguenti.



| Classe Terminal | Nome della chiave | Identificatore pubblico                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Nome           | REG \_ SZ  | Nome descrittivo del terminale                                                            |
| Company        | REG \_ SZ  | Nome azienda                                                                      |
| Versione        | REG \_ SZ  | Informazioni sulla versione                                                               |
| CLSID          | REG \_ SZ  | CLSID terminale (usato nel metodo COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ) |
| Indicazioni     | DWORD    | Direzione del terminale                                                                |
| MediaTypes     | DWORD    | Tipi di supporti terminali supportati                                                    |



 

Per una classe terminal gli attributi sono i seguenti.



| CLSID | Nome della chiave | Identificatore pubblico            |
|-------|----------|------------------------------|
| Nome  | REG \_ SZ  | Nome descrittivo della classe Terminal |



 

 

 
