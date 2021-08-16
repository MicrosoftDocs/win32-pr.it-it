---
title: Barra della lingua (applicazioni TSF)
description: Un'applicazione non può aggiungere elementi alla barra della lingua. solo un servizio di testo può aggiungere elementi alla barra della lingua.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Framework servizi di testo (TSF), barra della lingua
- TSF (Framework servizi di testo),barra della lingua
- Applicazioni abilitate per TSF, barra della lingua
- barra della lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0adeacdfe105700efba761b0622432f4ac382d147bd82145242be9fdd71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952109"
---
# <a name="language-bar-tsf-applications"></a>Barra della lingua (applicazioni TSF)

Un'applicazione non può aggiungere elementi alla barra della lingua. solo un servizio di testo può aggiungere elementi alla barra della lingua. Un'applicazione può influire sul modo in cui vengono visualizzati determinati elementi sulla barra della lingua.

Il [raggruppamento \_ GUID COMPARTMENT SPEECH \_ \_ DICTATIONSTAT](predefined-compartments.md) viene usato per indicare il tipo di input vocale che l'applicazione può accettare: input di testo diretto (dettatura) e/o comandi vocali. Per impostazione predefinita, la dettatura è abilitata e il comando vocale è disabilitato. Se l'applicazione può accettare comandi vocali, deve impostare il valore [TF \_ COMMANDING \_ ENABLED](speech-recognition-constants.md) nel raggruppamento GUID \_ COMPARTMENT SPEECH \_ \_ DICTATIONSTAT. Se l'applicazione può accettare la dettatura, deve impostare il valore TF DICTATION ENABLED nel raggruppamento \_ \_ GUID COMPARTMENT SPEECH \_ \_ \_ DICTATIONSTAT. Il valore TF DICTATION ON o TF COMMANDING ON di questo raggruppamento determina in quale modalità (dettatura o comando) si trova attualmente \_ \_ \_ l'input \_ vocale.

Se l'applicazione supporta l'archiviazione permanente dei dati delle proprietà, deve impostare il raggruppamento [GUID \_ COMPARTMENT \_ PERSISTMENUENABLED](predefined-compartments.md) su un valore diverso da zero. In questo modo il servizio di testo vocale abiliterà la voce di menu **Salva dati** voce.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come configurare Framework servizi di testo](how-to-set-up-tsf.md)
</dt> <dt>

[Barra della lingua (Servizi di testo)](language-bar.md)
</dt> </dl>

 

 




