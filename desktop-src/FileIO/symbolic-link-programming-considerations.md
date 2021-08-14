---
description: Considerazioni sulla programmazione per l'utilizzo di collegamenti simbolici.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considerazioni sulla programmazione (file system locali)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a98c244dac3fb4a9f6b73d11067af64512e0cfd54e58078bd87a2582b0c2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981881"
---
# <a name="programming-considerations-local-file-systems"></a>Considerazioni sulla programmazione (file system locali)

Quando si lavora con i collegamenti simbolici, tenere presenti le considerazioni di programmazione seguenti:

-   I collegamenti simbolici possono puntare a una destinazione inesistente.
-   Quando si crea un collegamento simbolico, il sistema operativo non verifica se la destinazione esiste.
-   Se un'applicazione tenta di aprire una destinazione inesistente, **viene restituito ERROR \_ FILE NOT \_ \_ FOUND** .
-   I collegamenti simbolici sono reparse point. Per altre informazioni, vedere [Determinare se una directory è una cartella montata.](determining-whether-a-directory-is-a-volume-mount-point.md)
-   È consentito un massimo di 63 reparse point (e pertanto collegamenti simbolici) in un percorso specifico.

    **Windows Server 2003 e Windows XP:** È previsto un limite di 31 reparse point in qualsiasi percorso specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[Collegamenti rigidi e giunzioni](hard-links-and-junctions.md)
</dt> </dl>

 

 



