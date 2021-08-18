---
description: Le applicazioni devono usare il carattere separatore di riga (0x2028) e il carattere separatore di paragrafo (0x2029) per dividere il testo normale. Viene iniziata una nuova riga dopo ogni separatore di riga. Viene iniziato un nuovo paragrafo dopo ogni separatore di paragrafo.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Uso dei separatori di riga e paragrafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d7cae4dc7bd720ca94e9780bcb83588650b3df578cd0216e2424c1b28d5af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764631"
---
# <a name="using-line-and-paragraph-separators"></a>Uso dei separatori di riga e paragrafo

Le applicazioni devono usare il carattere separatore di riga (0x2028) e il carattere separatore di paragrafo (0x2029) per dividere il testo normale. Viene iniziata una nuova riga dopo ogni separatore di riga. Viene iniziato un nuovo paragrafo dopo ogni separatore di paragrafo.

Non è necessario iniziare la prima riga o paragrafo in un file con questi caratteri o terminare l'ultima riga o paragrafo con tali caratteri. In questo modo si indica che in tale posizione è presente una riga o un paragrafo vuoto.

L'applicazione può usare il separatore di riga per indicare una fine della riga non condizionale. I separatori di riga, tuttavia, non corrispondono a una sequenza separata di caratteri di ritorno a capo e avanzamento di riga o a una combinazione di questi caratteri. I separatori di riga devono essere elaborati separatamente dai caratteri di ritorno a capo e avanzamento di riga.

L'applicazione può inserire un separatore di paragrafo tra paragrafi di testo. L'uso di questo separatore consente la creazione di file di testo normale che possono essere formattati con larghezze di riga diverse su sistemi operativi diversi. Il sistema di destinazione può ignorare eventuali separatori di riga e interrompere i paragrafi solo in corrispondenza di separatori di paragrafo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di caratteri speciali in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



