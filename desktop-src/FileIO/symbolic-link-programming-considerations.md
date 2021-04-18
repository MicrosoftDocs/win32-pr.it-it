---
description: Considerazioni sulla programmazione per l'utilizzo di collegamenti simbolici.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Considerazioni sulla programmazione (file system locali)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320824"
---
# <a name="programming-considerations-local-file-systems"></a>Considerazioni sulla programmazione (file system locali)

Quando si utilizzano i collegamenti simbolici, tenere presenti le considerazioni di programmazione seguenti:

-   I collegamenti simbolici possono puntare a una destinazione inesistente.
-   Quando si crea un collegamento simbolico, il sistema operativo non verifica se la destinazione esiste.
-   Se un'applicazione tenta di aprire una destinazione inesistente, viene restituito il **file di errore \_ \_ non \_ trovato** .
-   I collegamenti simbolici sono reparse point. Per ulteriori informazioni, vedere [determinare se una directory è una cartella montata](determining-whether-a-directory-is-a-volume-mount-point.md).
-   È consentito un massimo di 63 punti di analisi (e pertanto collegamenti simbolici) in un percorso specifico.

    **Windows Server 2003 e Windows XP:** È previsto un limite di 31 punti di analisi in un percorso specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[Collegamenti reali e giunzioni](hard-links-and-junctions.md)
</dt> </dl>

 

 



