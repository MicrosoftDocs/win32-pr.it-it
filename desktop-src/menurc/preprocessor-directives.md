---
title: Direttive per il preprocessore (menu e altre risorse)
description: È possibile usare le direttive descritte nella tabella seguente in base alle esigenze nello script della risorsa. Indicano a RC di eseguire azioni o di assegnare valori ai nomi.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilatore di risorse, direttive per il preprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340242"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a>Direttive per il preprocessore (menu e altre risorse)

È possibile usare le direttive descritte nella tabella seguente in base alle esigenze nello script della risorsa. Indicano a RC di eseguire azioni o di assegnare valori ai nomi.



| Direttiva                     | Descrizione                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [**\#definire**](-define.md)   | Definisce un nome specificato assegnando a esso un valore specificato.               |
| [**\#elif**](-elif.md)       | Contrassegna una clausola facoltativa di un blocco di compilazione condizionale.          |
| [**\#else**](-else.md)       | Contrassegna l'ultima clausola facoltativa di un blocco di compilazione condizionale.    |
| [**\#endif**](-endif.md)     | Contrassegna la fine di un blocco di compilazione condizionale.                     |
| [**\#if**](-if.md)           | Compila in modo condizionale lo script se un'espressione specificata è true.  |
| [**\#ifdef**](-ifdef.md)     | Compila in modo condizionale lo script se è stato definito un nome specificato.     |
| [**\#ifndef**](-ifndef.md)   | Compila in modo condizionale lo script se non è definito un nome specificato. |
| [**\#includere**](-include.md) | Copia il contenuto di un file nel file di definizione delle risorse.      |
| [**\#undef**](-undef.md)     | Rimuove la definizione del nome specificato.                         |



 

Per definire i simboli per gli identificatori di risorsa, usare la direttiva **\# define** per definirli in un file di intestazione. Includere questa intestazione sia nello script di risorsa che nel codice sorgente dell'applicazione. Analogamente, è possibile definire i valori per gli attributi e gli stili delle risorse includendo Windows. h nello script della risorsa.

RC considera i file con le estensioni. c e. h in modo speciale. Si presuppone che un file con una di queste estensioni non contenga risorse. Se un file ha l'estensione di file. c o. h, RC ignora tutte le righe nel file tranne le direttive del preprocessore. Pertanto, per includere un file che contiene risorse in un altro script di risorsa, assegnare al file un'estensione diversa da. c o. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pragma (direttive)](pragma-directives.md)
</dt> </dl>

 

 




