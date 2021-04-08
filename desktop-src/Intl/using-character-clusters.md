---
description: I cluster di caratteri sono sequenze di glifi che non possono essere suddivise tra le linee.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Uso di cluster di caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760487"
---
# <a name="using-character-clusters"></a>Uso di cluster di caratteri

I cluster di caratteri sono sequenze di glifi che non possono essere suddivise tra le linee. Alcuni linguaggi, ad esempio Thai e indiano, limitano il posizionamento del punto di inserimento ai punti tra i cluster. Questa restrizione si applica al movimento del cursore avviato con azioni della tastiera o del mouse (hit testing).

Uniscribe fornisce informazioni sul cluster sia negli attributi visivi contenuti in una struttura di [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) che negli attributi logici contenuti in una struttura [**\_ LOGATTR di script**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Dopo che l'applicazione chiama [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), le informazioni sul cluster vengono rappresentate sia dalle sequenze dello stesso valore nella **matrice \_ LOGATTR dello script** che dal membro **fClusterStart** nella matrice **\_ VISATTR di script** .

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) recupera anche il membro **fCharStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr) per identificare le posizioni del cluster.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



