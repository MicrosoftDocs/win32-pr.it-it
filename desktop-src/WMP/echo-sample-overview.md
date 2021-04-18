---
title: Panoramica dell'esempio Echo
description: Panoramica dell'esempio Echo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Plug-in di Windows Media Player, panoramica dell'esempio Echo
- plug-in, Panoramica di esempio Echo
- plug-in di elaborazione dei segnali digitali, panoramica dell'esempio Echo
- Plug-in DSP, panoramica dell'esempio Echo
- Esempio di plug-in Echo DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298558"
---
# <a name="echo-sample-overview"></a>Panoramica dell'esempio Echo

Questa guida compila un plug-in Windows Media Player DSP che crea un effetto eco nell'audio PCM durante la riproduzione. Gli obiettivi per il plug-in sono i seguenti:

-   Il plug-in elabora solo l'audio PCM a 8 bit o a 16 bit.
-   Supporta un tempo di ritardo compreso tra 10 millisecondi (MS) e 2000 ms (2 secondi). Rappresenta un intervallo pratico per la maggior parte delle applicazioni.
-   Supporta la combinazione del segnale originale con il segnale di ritardo.
-   Fornisce un'implementazione della pagina delle proprietà che consente all'utente di fornire un valore per il tempo di ritardo e un valore per la percentuale del segnale di ritardo rispetto al livello di segnale audio complessivo.
-   Il codice viene creato modificando l'esempio di plug-in di Windows Media Player Wizard audio DSP.

L'esempio Echo non è incluso in Windows Media Player SDK. si tratta di un esempio creato dall'utente. Per creare l'esempio Echo, è necessario iniziare con il progetto predefinito dalla procedura guidata plug-in di Windows Media Player. È possibile assegnare il nome desiderato al progetto. in questa documentazione si presuppone che il progetto sia denominato Echo. Per informazioni dettagliate sull'uso della procedura guidata, vedere [compilazione di un plug-in DSP](building-a-dsp-plug-in.md).

Nella sezione seguente viene fornita una panoramica del modo in cui l'esempio crea un effetto eco:

-   [Funzionamento del campione Echo](how-the-echo-sample-works.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio Echo**](the-echo-sample.md)
</dt> </dl>

 

 




