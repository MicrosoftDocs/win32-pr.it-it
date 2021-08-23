---
description: I cluster di caratteri sono sequenze di glifi che non possono essere suddivise tra righe.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Uso di cluster di caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7a48dc8ec1b6fa3ea28cd116f275b1f410b8abd7e232442cff430ab843765f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631821"
---
# <a name="using-character-clusters"></a>Uso di cluster di caratteri

I cluster di caratteri sono sequenze di glifi che non possono essere suddivise tra righe. Alcune lingue, ad esempio thai e indic, limitano il posizionamento del punto di inserimento ai punti tra i cluster. Questa restrizione si applica al movimento del cursore avviato con azioni della tastiera o del mouse (hit testing).

Uniscribe fornisce informazioni sul cluster sia negli attributi visivi contenuti in una struttura [**\_ SCRIPT VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) che negli attributi logici contenuti in una [**struttura SCRIPT \_ LOGATTR.**](/windows/win32/api/usp10/ns-usp10-script_logattr) Dopo che l'applicazione ha chiamato [**ScriptShape,**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)le informazioni sul cluster sono rappresentate sia da sequenze dello stesso valore nella matrice **SCRIPT \_ LOGATTR** che dal membro **fClusterStart** nella matrice **SCRIPT \_ VISATTR.**

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) recupera anche il membro **fCharStop** della struttura [**SCRIPT \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) per identificare le posizioni del cluster.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



