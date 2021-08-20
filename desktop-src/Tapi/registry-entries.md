---
description: I terminali collegabili sono classificati in superclassi del terminale.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Voci del Registro di sistema (API Di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd6e4e4d91b65e3ef886fd4d2d44b571f4ac4696697aef8b8d8b2715e273e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761168"
---
# <a name="registry-entries-telephony-api"></a>Voci del Registro di sistema (API Di telefonia)

I terminali collegabili sono classificati in superclassi del terminale. Ogni superclasse terminale ha una voce nel Registro di sistema nella chiave seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telefonia** \\ **TerminalManager**

Sotto la chiave Terminal Superclass (Superclasse terminale) sono presenti voci per ogni terminale collegabile all'interno della Superclasse terminale.

La voce per ogni Superclasse terminale è identificata da un CLSID della superclasse terminale. Si tratta di un identificatore univoco per una classe terminale. La classe terminale ha un attributo facoltativo: name, ovvero un nome descrittivo per la classe terminale. Ogni terminale collegabile è identificato da una classe terminale CLSID. ad esempio un GUID. Gli attributi per il terminale collegabile vengono archiviati in valori di chiave del terminale collegabile. Gli attributi per un terminale collegabile sono i seguenti.



| Classe Terminal | Nome della chiave | Identificatore pubblico                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Nome           | REG \_ SZ  | Nome descrittivo del terminale                                                            |
| Company        | REG \_ SZ  | Nome azienda                                                                      |
| Versione        | REG \_ SZ  | Informazioni sulla versione                                                               |
| CLSID          | REG \_ SZ  | CLSID del terminale (usato nel metodo [**Com CoCreateInstance)**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) |
| Indicazioni     | DWORD    | Direzione del terminale                                                                |
| MediaTypes     | DWORD    | Tipi di supporti terminali supportati                                                    |



 

Per una classe terminale, gli attributi sono i seguenti.



| CLSID | Nome della chiave | Identificatore pubblico            |
|-------|----------|------------------------------|
| Nome  | REG \_ SZ  | Nome descrittivo della classe terminale |



 

 

 
